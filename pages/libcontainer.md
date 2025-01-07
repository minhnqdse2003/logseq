- Docker. Inc, develop this tool in the scenarios of ((6755c288-36c4-4012-8032-63fd4d5a82ed)) and ((6755c2e5-cd60-401b-9aed-e57355458b24)) as a replace for LXC.  The goal of *libcontainer* was to be a platform-agnostic tool that provided Docker with access to fundamental container bulding-blocks that exist in the host kernel.
- libcontainer was an `internal library` created by Docker to handle the low-level operations necessary for container management, such as setup namespaces,cgroups and managing container processes. It was embedded within Docker's codebase and used to run container directly from Docker.
- Due to words `internal library`, Docker, Inc wanted to adhere to the **OCI specifications** for making it more modular, interoperal, and comliant with open standards.
- And now [[Runc]] come into place, it was born from `libcontainer` - It took the foundational code and refactored it to be a standalone, OCI compliant container runtime. It was designed to be simple, lightweight, and capable of being used by any container engine, not just Docker.