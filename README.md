# Programming and System Administration Notes

This repository contains my notes on various programming concepts, focusing on TypeScript and Java, as well as system administration topics with an emphasis on Docker and Kubernetes.

## Table of Contents

**I. Programming - TypeScript**

- **TypeScript Basics**
  - tsconfig.json
  - Types
    - Primitive Types
    - Non-Primitive Types
    - Type Assertions
  - Interfaces
- **Advanced TypeScript**
  - Type Inference
  - Type Compatibility
  - Combining Types
    - Type Unions
    - Type Intersections
    - Type Aliases
    - keyof Operator
  - Type Guards/Narrowing
    - instanceof operator
    - typeof Operator
    - Equality
    - Truthiness
    - Type Predicates
  - Typing Functions
    - Typing Functions
    - Function Overloading
  - Classes
    - Constructor Params
    - Access Modifiers
    - Abstract Classes
    - Inheritance vs Polymorphism
    - Method and Overriding
    - Constructor Overloading
  - Generics

**II. Programming - Java**

- **Java Core Concepts**
  - Data Structures
    - Linear data structure & Non-linear data structure
  - OOP Concepts
    - Object and Class
    - Inheritance
    - Method Overloading
    - Method Overriding

**III. System Administration - Docker**

- **Docker Fundamentals**
  - Container Concept
  - Container technique
  - Containers vs. Images
  - CONTAINER port vs HOST port
  - Docker CLI
  - Debugging Containers
  - Docker vs. Virtual Machines
  - Docker vs. Kubernetes
- **Advanced Docker**
  - Low-Level Docker Concepts
    - OCI (Open Container Initiative)
    - Namespaces
    - Runc
    - libcontainer
    - OCI Bundle
    - OCI layer
  - Docker Daemon (Engine)
    - Why Daemonless is Required
    - Container Runtime Route
  - Images
    - The basic
    - The deep dive
  - Container
  - Development process
  - Sample Docker Configurations
    - postgres - pgadmin4
    - Vite - ReactTs
  - Docker Best Practices
  - Docker Swarm
    - Docker swarm is all about two things
    - Docker Swarm the deep dive
      - Build a secure swarm cluster
        - Swarm primer
        - Step-by-step
      - Swarm services
        - Rolling updates
          - Scaling service
        - Routing Mesh and Ingress Network
    - The commands
      - Docker Swarm Commands Cheat Sheet
    - Scenario of replicas and node
    - Consensus Algorithms
      - Problem
      - Effective Consensus Algorithms
      - Features of Consensus Algorithms
      - Terms
      - How raft consensus perform
        - Prerequisite
        - Log Replication
        - Edge case
          - Split-Brain (Network partitions)
- **Kubernetes Basics**
  - What is Kubernetes?
  - Kubernetes Architecture
  - Kubernetes Concepts
  - Docker vs. Kubernetes
  - Kubernetes vs. Docker Swarm
