# How docker engine work (High-level view)
	- Docker CLI send commands to Docker deamon (Dockerd) -> Docker daemon parses these commands and delegates lower-level container lifecycle task to containerd -> Containerd, in turn, uses runc to execute the container with proper isolation and configuration on the host OS.
	  logseq.order-list-type:: number
	- ![2024-12-08-002627_697x267_scrot.png](../assets/2024-12-08-002627_697x267_scrot_1733592395193_0.png)
	  logseq.order-list-type:: number
- # How docker engine work (Low-level view)
	-