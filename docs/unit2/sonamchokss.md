# 2.5 Service-Based Architecture Style

**Contributed by:** Sonam Choki 

**Student ID:** 02240361 

**Date:** 11 May 2026  

**Course:** SDA202

--- 
### Defination
Service-based architecture is a hybrid of the microservices architecture style and is considered one of the most pragmatic architectural patterns. It is often chosen for its balance between the agility of microservices and the simplicity of monolithic applications.

---

## 2.5.1 Topology Variants
The topology of a service-based architecture typically consists of a **user interface**, **separately deployed services**, and a **monolithic or partitioned database**.

### Key Variants:
1.  **Shared Database Variant:**
    * Multiple services connect to a single, large database.
    * **Pros:** Simplifies data integrity and joins.
    * **Cons:** Creates a single point of failure and potential "bottleneck" at the database level.
2.  **Partitioned Database Variant:**
    * The database is split logically or physically based on service domains.
    * **Pros:** Reduces coupling and increases scalability.
3.  **API Gateway Variant:**
    * An API Gateway sits between the UI and the services to handle request routing, protocol translation, and security.

---

## 2.5.2 Service Design and Granularity
Granularity refers to the size and scope of the services within the architecture. Service-based architecture typically uses **domain-driven design** to find the "sweet spot" for service size.

### Characteristics:
* **Domain-Centric:** Services are usually grouped around a business domain (e.g., "Order Service", "Customer Service").
* **Coarse-Grained vs. Fine-Grained:**
    * Unlike microservices (which are fine-grained), service-based architecture services are **coarse-grained**. 
    * A single service might contain several related business functions to reduce the overhead of inter-service communication.
* **Maintainability:** By keeping services larger than microservices, developers avoid the "distributed monolith" pitfall where every change requires updating ten different services.

---

## 2.5.3 Database Partitioning
In service-based architecture, how you handle data is critical for performance and scalability.

### Strategies:
1.  **Logical Partitioning:**
    * Services share the same database instance but use different schemas or tables. 
    * This provides some isolation without the cost of managing multiple database servers.
2.  **Physical Partitioning (Database per Service):**
    * Each service has its own physical database instance.
    * **Benefits:** High fault tolerance and independent scaling.
    * **Challenges:** Difficult to perform cross-service reporting and maintain ACID transactions.
3.  **Data Synchronization:**
    * When databases are partitioned, data is often synchronized using asynchronous messaging or ETL (Extract, Transform, Load) processes for reporting purposes.

---

## References & Further Reading
- [GeeksforGeeks: Service Oriented Architecture (SOA)](https://www.geeksforgeeks.org/service-oriented-architecture/)
- [GeeksforGeeks: Monolithic vs. Service-Oriented vs. Microservice Architecture](https://www.geeksforgeeks.org/system-design/monolithic-vs-service-oriented-vs-microservice-architecture/)
- [GeeksforGeeks: Database Partitioning Strategy](https://www.geeksforgeeks.org/system-design/data-partitioning-techniques/)
