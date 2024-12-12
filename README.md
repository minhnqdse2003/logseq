# Programming and System Administration Notes

This repository houses my notes on programming (TypeScript, Java) and system administration (Docker, Kubernetes).

## Table of Contents

**I. Programming - TypeScript** <br> _(Focus: Modern JavaScript development)_

* **TypeScript Basics** <br> _(Foundation of TypeScript)_
    * **tsconfig.json:** Compiler configuration.  Specifies compiler options like target JavaScript version, module system, strictness, and output directories.  Crucial for controlling the build process. <br> _(Example: `compilerOptions`, `include`, `exclude`)
    * **Types:** Defining data structures and ensuring type safety. <br> _(Building blocks of TypeScript)_
        * **Primitive Types:** Basic data types like `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `void`, `any`, `unknown`, and `never`. <br> _(Simple values)_
        * **Non-Primitive Types:** Complex data types including `arrays`, `objects`, `tuples`, `enums`, and more.  Allows for creating custom types and structures. <br> _(Structures and custom types)_
        * **Type Assertions:**  Explicitly setting a type when TypeScript's inference isn't sufficient or desired.  Uses `as` or angle brackets (`<>`). <br> _(Overriding type inference)_
    * **Interfaces:** Defining the structure of objects and classes.  Acts as a contract for objects to adhere to, ensuring consistent shapes.  <br> _(Contracts for objects)_
* **Advanced TypeScript** <br> _(Deeper dive into TypeScript features)_
    * **Type Inference:** TypeScript automatically determines the type of a variable based on its initial value or usage.  Reduces the need for explicit type annotations.  <br> _(Less verbose code)_
    * **Type Compatibility:**  Rules that govern how TypeScript checks if two types are compatible.  Uses structural typing (comparing the shape of types) rather than nominal typing. <br> _(Working with different types)_
    * **Combining Types:** Creating more complex types from simpler ones. <br> _(Advanced type manipulation)_
        * **Type Unions:**  Allows a variable to hold values of different types, separated by a vertical bar (`|`).  <br> _(Flexibility with types)_
        * **Type Intersections:**  Combines multiple types into one, merging their properties.  Uses the ampersand symbol (`&`). <br> _(Combining type features)_
        * **Type Aliases:**  Creating a new name for an existing type.  Useful for readability and code organization. Uses the `type` keyword. <br> _(Code readability and organization)_
        * **`keyof` Operator:** Extracts the keys of an object type as a union of string literals.  Useful for dynamically accessing object properties based on their keys.  <br> _(Dynamically working with keys)_
    * **Type Guards/Narrowing:**  Techniques to refine the type of a variable within a specific scope, often using conditional logic. Improves type safety by eliminating type uncertainties. <br> _(Improving type safety)_
        * **`instanceof` Operator:**  Checks if an object is an instance of a particular class.  Narrows the type to the class if the check passes. <br> _(Class-based type checking)_
        * **`typeof` Operator:** Checks the type of a variable at runtime. Useful for narrowing down types based on their primitive type (e.g., 'string', 'number', 'boolean'). <br> _(Basic type checking)_
        * **Equality:** Narrowing types based on equality comparisons (e.g., `===`, `!==`).  TypeScript infers more specific types based on the values compared. <br> _(Conditional type refinement)_
        * **Truthiness:**  Narrowing types based on truthy or falsy values in conditional statements.  If a variable is checked in a condition, TypeScript can infer that it's not null or undefined within that block. <br> _(Conditional logic and types)_
        * **Type Predicates:** Functions that return a boolean and assert a specific type for a variable.  Used to create custom type guards for more complex scenarios.  <br> _(Specialized type checking)_
    * **Typing Functions:**  Defining the types of function parameters and return values.  Helps enforce correct function usage and improves code maintainability. <br> _(Enforcing correct function usage)_
        * **Typing Functions:**  Assigning type annotations to function parameters and the return type.  <br> _(Input and output types)_
        * **Function Overloading:** Defining multiple function signatures with different parameter types. TypeScript determines the correct overload based on the arguments passed during the function call. <br> _(Flexibility with different parameters)_
    * **Classes:**  Object-oriented programming constructs that allow for creating reusable blueprints for objects.  <br> _(Structuring code with classes)_
        * **Constructor Parameters:** Using constructor parameters to initialize class properties.  Can use access modifiers (public, private, protected) directly in the constructor parameters to define properties and their visibility.  <br> _(Initializing class instances)_
        * **Access Modifiers:** Keywords (`public`, `private`, `protected`) that control the accessibility of class members (properties and methods).  Encapsulation. <br> _(Encapsulation)_
        * **Abstract Classes:** Classes that cannot be instantiated directly. Serve as base classes for other classes to inherit from, defining common behavior. <br> _(Defining common behavior)_
        * **Inheritance vs. Polymorphism:**  Inheritance enables code reuse by creating subclasses that inherit properties and methods from a parent class. Polymorphism allows objects of different classes to be treated as objects of a common type, enabling flexible and dynamic behavior. <br> _(OOP principles)_
        * **Method Overriding:**  A subclass can provide a specific implementation for a method that is already defined in its parent class.  Modifies the inherited behavior. <br> _(Customization in subclasses)_
        * **Constructor Overloading:**  Defining multiple constructors for a class, each with a different set of parameters.  Allows for flexible initialization of objects. <br> _(Flexible initialization)_
    * **Generics:**  Writing reusable code components that can work with different types without knowing those types at compile time. <br> _(Type parameters)_

**II. Programming - Java** <br> _(Focus: Core Java concepts)_

* **Java Core Concepts** <br> _(Fundamentals of Java)_
    * **Data Structures:** Ways of organizing data in memory to access and manipulate it efficiently. <br> _(Efficient data manipulation)_
        * **Linear Data Structures:** Data elements arranged sequentially, where each element is directly connected to the next and previous element (except the first and last). Examples: arrays, linked lists, stacks, queues. <br> _(Ordered data)_
        * **Non-Linear Data Structures:** Data elements are not arranged sequentially.  Relationships can exist between elements that are not adjacent. Examples: trees, graphs, hash tables. <br> _(Unordered or interconnected data)_
    * **OOP Concepts** <br> _(Object-oriented principles in Java)_
        * **Objects and Classes:** Objects are instances of classes.  Classes are blueprints that define the state (fields/variables) and behavior (methods) of objects. <br> _(Core OOP concepts)_
        * **Inheritance:**  A mechanism that allows a class (subclass/derived class) to inherit properties and methods from another class (superclass/base class). Promotes code reuse and establishes an "is-a" relationship.  Uses the `extends` keyword. <br> _(Extending classes)_
        * **Method Overloading:** Defining multiple methods within the same class with the same name, but different parameter lists (number, type, or order of parameters). The compiler determines which method to call based on the arguments passed. <br> _(Polymorphism with parameters)_
        * **Method Overriding:** A subclass providing a specific implementation for a method that is already provided by its parent class. The method in the subclass must have the same signature (name, return type, and parameters) as the method in the parent class. Uses the `@Override` annotation (recommended). <br> _(Polymorphism with inheritance)_


**III. System Administration - Docker** <br> _(Focus: Containerization)_

* **Docker Fundamentals** <br> _(Core concepts and usage of Docker)_
    * **Container Concepts:** Understanding what containers are, their benefits (portability, isolation, consistency), and how they differ from virtual machines.  <br> _(High-level understanding)_
    * **Container Techniques:** Basic Docker commands and workflows, including building images (`docker build`), running containers (`docker run`), managing images (`docker images`, `docker pull`, `docker push`), and inspecting containers (`docker ps`, `docker inspect`).  <br> _(Practical usage)_
    * **Containers vs. Images:**  Distinguishing between Docker images (read-only templates) and containers (running instances of images). <br> _(Build-time vs. runtime)_
    * **Container Port vs. Host Port:** How port mapping works between the container and the host machine, including the `-p` flag and port publishing. <br> _(Network connectivity)_
    * **Docker CLI:** Commonly used Docker commands for managing images, containers, networks, and volumes. <br> _(Command-line interface)_
    * **Debugging Containers:** Techniques for troubleshooting container issues, such as using `docker logs`, `docker exec`, and debugging tools. <br> _(Troubleshooting)_
    * **Docker vs. Virtual Machines:**  Key differences between Docker containers and virtual machines in terms of architecture, resource usage, and performance. <br> _(Comparison and advantages)_
    * **Docker vs. Kubernetes:**  A high-level comparison of Docker (containerization platform) and Kubernetes (container orchestration platform).  Understanding when each technology is appropriate. <br> _(Different levels of management)_
* **Advanced Docker** <br> _(Deeper understanding of Docker components and architecture)_
    * **Low-Level Docker Concepts:** <br> _(Underlying mechanisms)_
        * **OCI (Open Container Initiative):** Standards for container formats and runtimes, ensuring interoperability between different containerization technologies. <br> _(Standardization)_
        * **Namespaces:** Linux kernel feature that provides isolation for containers (PID, network, IPC, mount, UTS, user).  <br> _(Isolation)_
        * **Runc:**  The low-level container runtime that creates and runs containers based on the OCI specifications.  <br> _(Container execution)_
        * **libcontainer:** Docker's initial container runtime library, which evolved into `runc`. <br> _(Historical context)_
        * **OCI Bundle:**  A standardized directory structure containing the configuration and root filesystem for a container. <br> _(Container packaging)_
        * **OCI Layer:** Refers to the level of abstraction where `containerd` and other high-level runtimes interact with low-level runtimes like `runc`.  <br> _(Abstraction layer)_
    * **Docker Daemon (Engine):** The background service (`dockerd`) that manages containers, images, networks, and volumes. <br> _(Core Docker service)_
        * **Why Daemonless is Required:**  Explanation of daemonless container technologies (like `containerd` and Podman) and their benefits. <br> _(Architectural considerations)_
        * **Container Runtime Route:** The flow of execution from the Docker CLI to the container runtime, including the role of `containerd` and `runc`. <br> _(Execution flow)_
    * **Images:** Read-only templates for creating containers.  <br> _(Building blocks for containers)_
        * **The Basics:** Understanding image layers, Dockerfiles, and image repositories. <br> _(Image fundamentals)_
        * **The Deep Dive:** Multi-stage builds, image optimization, and advanced Dockerfile instructions.  <br> _(Optimizing images)_
    * **Container:**  A running instance of a Docker image. <br> _(Runtime unit)_
    * **Development Process:**  Using Docker for development workflows, including building, testing, and deploying applications. <br> _(Development lifecycle)_
    * **Sample Docker Configurations:**  Example `docker-compose.yml` files and Dockerfiles for various applications and services. <br> _(Practical examples)_
    * **Docker Best Practices:**  Recommendations for building efficient and secure Docker images and managing containers effectively.  <br> _(Optimization and security)_
    * **Docker Swarm:**  Docker's native container orchestration tool for creating and managing clusters of Docker nodes. <br> _(Clustering and orchestration)_
        * **Docker Swarm Is All About Two Things:** Core features and purposes of Docker Swarm (cluster management and microservice orchestration). <br> _(High-level overview)_
        * **Docker Swarm: The Deep Dive:** Advanced Swarm concepts, including swarm mode, manager high availability, routing mesh, ingress networks, and service management. <br> _(Detailed understanding)_
            * **Building a Secure Swarm Cluster:**  Setting up and securing a Docker Swarm cluster, including network configurations and security best practices. <br> _(Security and configuration)_
                * **Swarm Primer:** Fundamental concepts of Swarm nodes, managers, workers, and the `etcd` database.  <br> _(Swarm components)_
                * **Step-by-step:** Guide to creating and joining nodes to a Swarm cluster, managing tokens, and using swarm init. <br> _(Setting up a cluster)_
            * **Swarm Services:** Deploying and managing applications as services in a Swarm cluster. <br> _(Application deployment)_
                * **Rolling Updates:**  Updating services with zero downtime, including scaling, update parallelism, and update delays. <br> _(Deployment strategies)_
                    * **Scaling Services:**  Changing the number of replicas of a service to handle varying loads. <br> _(Dynamic scaling)_
                * **Routing Mesh and Ingress Network:** Internal routing within the Swarm and managing external access to services. <br> _(Network traffic management)_
        * **The Commands:** Essential Docker Swarm CLI commands for managing the swarm, nodes, and services. <br> _(Command reference)_
            * **Docker Swarm Commands Cheat Sheet:**  A quick reference for common Swarm commands. <br> _(Command summary)_
        * **Scenario of Replicas and Node:**  Illustrative example to understand the relationship between replicas, nodes, and high availability. <br> _(Conceptual understanding)_
        * **Consensus Algorithms:**  Understanding how Swarm achieves consensus and elects a leader, including the Raft consensus algorithm.  Covers terms, features, and the election process.  <br> _(Distributed consensus)_
            * **Split-Brain (Network Partitions):**  Handling network partitions and avoiding split-brain scenarios. <br> _(Fault tolerance)_


**IV. System Administration - Kubernetes** <br> _(Focus: Container orchestration)_

* **Kubernetes Basics** <br> _(Introduction to Kubernetes)_
    * **What is Kubernetes?:**  Definition, purpose, and key features of Kubernetes as a container orchestration platform.  <br> _(High-level overview)_
    * **Kubernetes Architecture:**  Components of a Kubernetes cluster (master node, worker nodes, kubelet, API server, etcd).  <br> _(Cluster components)_
    * **Kubernetes Concepts:**  Understanding Pods, Deployments, Services, and other core Kubernetes objects. <br> _(Core objects)_
    * **Docker vs. Kubernetes:**  Clarifying the relationship and differences between Docker and Kubernetes. <br> _(Comparison and integration)_
    * **Kubernetes vs. Docker Swarm:**  Comparing Kubernetes and Docker Swarm as container orchestration tools. <br> _(Choosing the right tool)_


This enhanced outline provides more detail and context for each topic, making it easier to understand the overall structure and find specific information.  Remember to populate the sections with your detailed notes.  This structured outline will help keep your notes organized and make them a valuable resource for learning and reference.
