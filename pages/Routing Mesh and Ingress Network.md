# **Routing Mesh (Default)**
	- **How it works**
		- When you publish a port for a service (e.g., -p 80:80), any manager node in the Swarm can receive external traffic on that port. The swarm's internal routing mesh then forwards the traffic to an available replica of the service, regardless of which node the replica is running on.
	- **Benefits**
		- `Simplicity`: Easy to set up. Publishing a port is all it takes.
		- `Loading Balancing`: Built-int load balancing across all replicas of the service.
	- **Limitations**
		- Manager nodes become entry points: This can create a potential bottleneck or single point of failure if 
		  manager nodes aren't highly available.
		- Not ideal for complex routing: Limited control over traffic routing.
- # **Ingress Network (Recommended for Production)**
	- **How it works**
		- You create a dedicated overlay network called an ***ingress network***. Services that need to be externally accessible are attached to this network. You then deploy a load balancer or reverse proxy (Like Traefik, Nginx, or HAProxy) as a service within the Swarm and also attach it to the ingress network. External traffic directed to the load balancer, which then distributes it to the aappropirate services on the ingress network.
	- **Benefits**
		- Decoupled entry point: Separates the entry point for external traffic from the manager nodes, improving scalability, and resilience.
		- Advanced routing: Allows for more complex routing scenarios, such as path based routing, TLS termination, and other load-balancing strategies.
		- High Availability: Can be combined with highly available load balancers to eliminate single points of failure.
	- **Slightly more complex setup**
		- Requires creating an ingress network and deploying a load balancer service.
- # **Key Differences Summarized**
	- |**Feature**|**Routing Mesh**|**Ingress Network**|
	  |Entry Point|Any manager node|Dedicated load balancer|
	  |Load Balancing|Built-in|Provided by load balancer|
	  |Complexity|Simpler|More complex|
	  |Scalability|Limited|Highly scalable|
	  |Resilience|Dependent on manager nodes|More resilient|
	  |Advanced Routing|Limited|Flexible and powerful|
	-
- **Which to Use?**
	- **Routing mesh:** Suitable for simple deployments and testing where high availability and complex routing are not critical.
	- **Ingress network:** Strongly recommended for production environments. Provides greater scalability, resilience, and flexibility in managing external access to your services. While slightly more complex to set up initially, it offers significant advantages in the long run.
- # Sample setup
- ```
  version: "3.9"  # Use a compatible Docker Compose version
  
  services:
    nginx:
      image: nginx:latest
      ports:
        - "80:80" # Publish port 80 on the host to port 80 on the Nginx container
        - "443:443" # Publish port 443 for HTTPS (if using TLS)
      networks:
        - ingress
      volumes:
        - nginx_config:/etc/nginx/conf.d # Mount a volume for Nginx configuration
      deploy:
        mode: replicated
        replicas: 1 # Start with one replica, scale as needed
        placement:
          constraints: [node.role == manager] # Run Nginx on a manager node for simplicity (optional)
        update_config:
          parallelism: 1
          delay: 10s
        restart_policy:
          condition: on-failure
  
  
    my-web-app: # Your web application service
      image: <your_web_app_image>
      networks:
        - ingress
      deploy:
        mode: replicated
        replicas: 3 # Or however many replicas you need
        update_config:
          parallelism: 1
          delay: 10s
        restart_policy:
          condition: on-failure
  
  
  
  networks:
    ingress:
      external: false # Important: do not set external: true for an overlay network used for ingress
      driver: overlay
  
  volumes:
    nginx_config:
    
  #Nginx config
  server {
    listen 80;
    server_name example.com; # Replace with your domain or IP
  
    location / {
      proxy_pass http://my-web-app:8080; # Replace with your web app's port
      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
    }
  }
    
  ```
-