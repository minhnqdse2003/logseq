- **Basic Concepts and Setup**
- [[RDBMS Fundamentals]]
  collapsed:: true
	- Object Model: data types, columns, rows, tables, schemas, databases, queries
	- Relational Model: domains, attributes, tuples, relations, constraints, NULL
	- High-Level Concepts: ACID, MVCC, transactions, write-ahead log, query processing
- **PostgreSQL Installation and Setup**
  collapsed:: true
	- Package Managers (APT, YUM, etc.)
	- Docker
	- Service Management (systemd, pg_ctl)
	- Connecting with psql
- **SQL Basics**
  collapsed:: true
	- Data Types
	- DML: querying, modifying, filtering, joining
	- Advanced DML: transactions, CTE, subqueries, lateral joins, grouping, set operations
	- DDL: managing tables and schemas
	- Data Import/Export with COPY
	  
	  **Configuration and Security**
- **PostgreSQL Configuration**
  collapsed:: true
	- postgresql.conf overview
	- Resource Usage
	- Write-Ahead Log
	- Checkpoints and Background Writer
	- Cost-Based Vacuum and Auto-Vacuum
	- Replication
	- Query Planner
	- Reporting, Logging, and Statistics
	- Extensions
- **PostgreSQL Security**
  collapsed:: true
	- Authentication Models, Roles, pg_hba.conf, SSL Settings
	- Object Privileges (grant/revoke, default privileges)
	- Advanced Security: row-level security, SELinux
	  
	  **Database Administration Skills**
- **Infrastructure DBA Skills**
  collapsed:: true
	- Replication (streaming, logical)
	- Backup/Recovery Tools
	- Upgrading Procedures
	- Connection Pooling
	- Infrastructure Monitoring
	- High Availability and Cluster Management
- **Automation**
  collapsed:: true
	- Shell Scripting (Bash, Python, Perl)
	- Configuration Management (Ansible, Salt, Chef, Puppet)
- **Application DBA Skills**
  collapsed:: true
	- Migrations
	- Data Import/Export, Bulk Loading, Processing
	- Queues (practical patterns)
	- Skytools PGQ
	- Data Partitioning and Sharding
	- Database Normalization
	  
	  **Advanced Topics**
- **PostgreSQL Internals**
  collapsed:: true
	- Processes and Memory Architecture
	- Vacuum Processing
	- Buffer Management
	- Lock Management
- **Fine-Grained Tuning**
  collapsed:: true
	- Per-User, Per-Database Settings
	- Storage Parameters
	- Workload-Dependent Tuning (OLTP, OLAP, HTAP)
- **Advanced SQL**
  collapsed:: true
	- PL/pgSQL, Procedures, Functions, Triggers
- **Troubleshooting**
  collapsed:: true
	- Operating System Tools
	- PostgreSQL System Views
	- Query Analysis (EXPLAIN)
	- Log Analysis
	- External Tracing/Profiling Tools
- **SQL Optimization**
  collapsed:: true
	- Indexes and Use Cases
	- SQL Query Patterns and Anti-Patterns
	- SQL Schema Design Patterns and Anti-Patterns
	  
	  **Architectural Knowledge**
- **PostgreSQL Forks and Extensions**
  collapsed:: true
	- Greenplum, TimescaleDB, Citus, PostgreSQL-XL
- **RDBMS in General**
  collapsed:: true
	- Benefits and Limitations
	- Comparisons with Other RDBMS and NoSQL Databases
	  
	  **Community Involvement**
- **PostgreSQL Hacking**
  collapsed:: true
	- Mailing Lists
	- Patch Review
	- Patch Writing
	- Commitfests