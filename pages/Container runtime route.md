- ![The differences between Docker, containerd, CRI-O and runc - Tutorial Works](https://www.tutorialworks.com/assets/images/container-ecosystem-docker.drawio.png)
- # Docker
  
  Docker is a comprehensive containerization platform that includes some API:
	- Docker Engine: The core runtime and containerization engine
	- Docker CLI: Command-line interface for interacting with Docker
	- Docker Hub: Image repository and distribution service
	- Docker Swarm: Container orchestration tool
- # Dockerd
  
  Dockerd refers specifically to the Docker daemon, which is the background service that manages containers [2](https://stackoverflow.com/questions/46649592/dockerd-vs-docker-containerd-vs-docker-runc-vs-docker-containerd-ctr-vs-docker-c). It handles tasks like:
	- Creating, starting, stopping, and deleting containers
	- Managing container networks
	- Handling volume mounting
	- Performing image management
- # Docker-containerd
  
  Docker-containerd is a container runtime that was developed by Docker and is now maintained by the Cloud Native Computing Foundation (CNCF) [3](https://blog.purestorage.com/purely-educational/containerd-vs-docker-whats-the-difference/)[5](https://medium.com/@argferreira1/docker-vs-containerd-unraveling-the-differences-and-analyzing-performance-9cdd369ead17). It focuses on:
	- Low-level container lifecycle management
	- Image management
	- Storage layer integration
	- Network attachment