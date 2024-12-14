# Programming and System Administration Notes

This repository houses my notes on programming (TypeScript, Java) and system administration (Docker, Kubernetes, Postgres).

## Table of Contents

**I. Programming - TypeScript**

*   **TypeScript Basics**
    *   `tsconfig.json`
    *   Types
        *   Primitive Types
            *   `boolean`
            *   `number`
            *   `string`
            *   `void`
            *  `undefined`
            *   `null`
        *   Non-Primitive Types
            *   `interface`
            *   `class`
            *   `enum`
            *   `Array`
            *   `Tuple`
            *   `Object`
            *   `unknown`
            *   `any`
            *  `never`
        *   Type Assertions
            *   `as [type]`
            *   `as const`
            *   `as any`
            *   Non-null `!`
    *   Interfaces: Types vs. Interfaces
*   **Advanced TypeScript**
    *   Type Inference
    *   Type Compatibility
    *   Combining Types
        *   Type Unions
        *   Type Intersections
        *   Type Aliases
        *   `keyof` Operator
    *   Type Guards/Narrowing
        *   `instanceof` operator
        *   `typeof` Operator
        *   Equality checks (`===`, `!==`, `==`, `!=`)
        *   Truthiness
        *   Type Predicates
    *   Typing Functions
        *   Typing Function Declarations
        *   Arrow Function with Types
        *   Function Type Expressions
        *   Function Overloading
    *   Classes
        *   Constructor Parameters
        *   Access Modifiers (`private`, `protected`, `public`)
        *   Abstract Classes
        *   Inheritance vs. Polymorphism
        *   Method Overriding
        *   Constructor Overloading
    *   Generics
        *   Generic Constraints

**II. Programming - Java**

*   **Java Core Concepts**
    *   Data Structures
        *   Linear data structures
        *   Non-linear data structures
    *   OOP Concept
        *   Object and Class
            *   Fields
            *   Methods
            *   Constructor
            *  Instance Blocks
            * Static Blocks
        *   Inheritance
        *   Method Overloading
        *   Method Overriding

**III. System Administration - Docker**

*   **Docker Fundamentals**
    *   Container Concept
    *   Container Techniques
    *   Container vs. Image
    *   CONTAINER port vs. HOST port
    *   CLI
    *   Debug
    *   Docker vs. Virtual Machine
    *   Docker vs Kubernetes
*   **Advanced Docker**
    *   Low-Level Docker Concepts
        *   OCI (Open Container Initiative)
        *   `Namespace`
        *   `Runc`
        *   `libcontainer`
        *   OCI Bundle
        *  OCI layer
        *   The daemon (a.k.a engine)
            *   Why Daemonless is Required
            *   Container Runtime Route
    *   Images
        *   The Basics
        *   The Deep Dive
    *   Container
    *   Development Process with Docker
    *   Sample Docker Configurations (using docker-compose)
        *   postgres - pgadmin4
        *    Vite - ReactTs
    *   Docker Best Practices
    *   Docker Swarm
        *   Docker Swarm Is All About Two Things
            *   An Docker enterprise-grade secure cluster of Docker hosts
            *   An engine for orchestrating microservice apps
        *   Docker Swarm the deep dive
            *   Building a Secure Swarm Cluster
                *   Swarm Primer
                *   Step-by-step guide for creating a Swarm cluster
            *   Swarm Services
                *   Rolling Updates
                    *   Scaling Services
                *    Routing Mesh and Ingress Network
        *   Docker Swarm Commands Cheat Sheet
        *    Scenario of replicas and node
        *   Consensus Algorithms
            *   Split-Brain (Network Partitions)

**IV. System Administration - Kubernetes**

*   **Kubernetes Basics**
    *   What is Kubernetes?
    *   Kubernetes Architecture
    *   Kubernetes Concepts
         *  Pod/Container
    *   Docker vs. Kubernetes
    *   Kubernetes vs Docker swarm

**V. Database Administration - Postgres**

*   RDBMS Fundamentals
*   PostgreSQL Installation and Setup
*   SQL Basics
*   PostgreSQL Configuration
*   PostgreSQL Security
*   Infrastructure DBA Skills
*   Automation
*   Application DBA Skills
*   PostgreSQL Internals
*   Fine-Grained Tuning
*   Advanced SQL
*   Troubleshooting
*   SQL Optimization
*   PostgreSQL Forks and Extensions
*   RDBMS in General
*   PostgreSQL Hacking

**.NET**

*   .NET Overview
*   Building Block .NET Platform
    *   CLR or CoreCLR
    *   CTS (Common type system)
    *   CLS (Common Language Specification)
        *   Different between CTS & CLS
    *   BCL

**VI. Code Quality Setup**

*   Husky
*   Lint-staged
*   Prettier
*   Storybook
