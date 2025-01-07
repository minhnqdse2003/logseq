- ![How Kubernetes works | CNCF](https://www.cncf.io/wp-content/uploads/2020/08/Kubernetes-architecture-diagram-1-1.png)
- # What is kubernetes
	- Definition
	  logseq.order-list-type:: number
	  collapsed:: true
		- Open source `container orchestration tool`
		- Develop by `Google`
		- Help manage `containerized applications` in `different development environments`
	- What `problem` does kubernertes solve
	  logseq.order-list-type:: number
	  collapsed:: true
		- Trend from `Monolith` to `Microservices`
		- Increased usage of `containers`.
		- Deman for a proper way of `managing` those hundreds of containers.
	- What features do orchestration tools offer?
	  logseq.order-list-type:: number
		- `High Availability` or no downtime
		- `Scalability` or high performance
		- `Disaster recovery` - backup and restore.
	- Kubernetes Basic Architecture 
	  logseq.order-list-type:: number
		- A kubernetes cluster is made up with at least one `master node` and then connect it to each `worker node`. Each `worker node` has a kubelet (Using for communicate between cluster and exec some task for example running application), each `worker node` has `docker containers` of different application deploy on top of it, depending on how `workload` is `distributed` we will have `different` numbers of docker containers running on `worker node`.
		- `Master node` will run several kubenetes process that are absolutely neccessary to run and manage cluster properly includes:
			- `API Server` to handle request from -> `UI` for kubernetes dashboard for interact, `API` for using script, `CLI`. Serve as an `entrypoint` to `K8S cluster`.
			- `Controller Manager` keeps track of whats happening in the cluster (repair, container died -> restart)
			- `Schedule` ensure Pods placement based on workload and available resources on each node.
			- `Key-Value Store Etcd` hold all status of `node` and `container` in each node also all the configuration data inside. We can recovery the whole cluster state using `etcd snapshot`
		- `Virtual network` enable `master node` and `work node` talk to each other and help Pod running on different node can communicate with each other via unique ip addresses.
		  id:: 6752bf84-a269-4d81-bf28-37d2b2ad1cf2
		  collapsed:: true
			- **Inter-node Communication**: The virtual network ensures that communication between the master node and worker nodes is seamless. It provides a consistent IP space that allows pods on different nodes to communicate as if they were on the same local network.
			- **Pod-to-Pod Communication**: Pods running on different nodes can communicate with each other via their unique IP addresses, thanks to the virtual network.
			- **API Server Communication**: Worker nodes communicate with the Kubernetes API server on the master node to fetch configuration data, report status, and receive instructions for managing pods.
			- **Communication Flow**:
				- **Master to Worker Nodes**: The master node communicates with worker nodes via the Kubernetes API server, using the virtual network to send instructions (e.g., pod scheduling, configuration updates).
				- **Worker Nodes to Master**: Worker nodes use the virtual network to send status updates, metrics, and other information back to the master node.
				  id:: 6752c33f-56aa-4a5a-806c-9c86b73c7bcd
				- **Pod Communication**: Pods can reach out to each other across different worker nodes by using the IP address assigned to each pod and the virtual network routing.
		- **NOTE**: If the `master node` fails, control of the cluster is lost.
	- Kubernetes Basic Concepts
	  logseq.order-list-type:: number
		- Pod/Container
		  logseq.order-list-type:: number
			- Pod is the smallest unit that user will interact with.
			  logseq.order-list-type:: number
			- Pod is a `warpper` of a `container`. Each `worker node` will have multiple Pods and one pod can have multiple containers.
			  logseq.order-list-type:: number
			- In kubernetes has `Virtual network` it will assign each pod its own IP address and they using `Internal IP address`
			  logseq.order-list-type:: number
			- Pod can `die` very frequently, when pod die -> new pod was created -> assign `NEW` IP Address -> Different IP address when compare with the old one.
			  logseq.order-list-type:: number
				- That raise a new issue for maintaining connectivity, so that we will have `Kubernetes Services` place as an `abstract layer` to `communicate` with other services of Pod. Its a `stable endpoint` and provides a `DNS name` that remains `constant`, allowing other services of the application to connect to it without worrying about the underlying pod's IP Address change.
				  logseq.order-list-type:: number
				- **Service Selector**: The Service uses a label selector to define which pods should be part of the Service. This allows the Service to automatically route traffic to new pods based on their labels.
				  logseq.order-list-type:: number
				- **Stable Endpoint**: The Service provides a stable DNS name and IP address that clients can use to access the pods, even if individual pods die and new ones are created with different IPs.
				  logseq.order-list-type:: number
				- **Load Balancing**: Services automatically load balance traffic across the healthy pods that match the service's selector.
				  logseq.order-list-type:: number
			- Types of Services:
			  logseq.order-list-type:: number
				- **ClusterIP** (default): Exposes the service on a cluster-internal IP. This is used when you want the service to be accessible only within the cluster.
				  logseq.order-list-type:: number
				- **NodePort**: Exposes the service on a static port on each node's IP. This allows external access to the service via `<NodeIP>:<NodePort>`.
				  logseq.order-list-type:: number
				- **LoadBalancer**: Provisions an external load balancer that routes external traffic to the service.
				  logseq.order-list-type:: number
				- **ExternalName**: Maps the service to an external DNS name.
				  logseq.order-list-type:: number
- [[Docker vs Kubernetes]]
- [[Kubernetes vs Docker swarm]]