**Contributed by:** Namgay Lhamo  
**Student ID:** 02240350  
**Date:** 06 May 2026  
**Course:** SDA202

---

## 2.2 Monolithic Versus Distributed Architectures

### What is Monolithic Architecture?

A monolithic architecture is a software design where all components (presentation, business logic, data access) are built, deployed, and scaled as a single unified unit.

**Characteristics:**
- Single deployment unit (one JAR/WAR file)
- All components run together
- Shared database
- Local method calls between components

**When to Use Monolithic:**
- Small, simple applications
- Starting point for new projects
- Tight budget and time constraints
- Team is unsure about requirements
- Familiar to most developers

**Advantages:**
- Simple to develop initially
- Easy to test end-to-end
- Low cost
- No network latency
- Straightforward deployment

**Disadvantages:**
- Hard to scale individual parts
- Affects maintainability as app grows
- Slower development over time
- Architecture sinkhole anti-pattern (requests pass through layers with no processing)

### What is Distributed Architecture?

A distributed architecture has multiple independent deployment units that communicate through remote access protocols (REST API, messaging, etc.).

**Characteristics:**
- Multiple deployment units
- Independent services
- Network communication
- Decentralized data

**Advantages:**
- Better performance
- Scalability
- Deployability
- High availability

**Disadvantages:**
- Complex to build
- Significant trade-offs
- More expensive
- Multiple administrators needed

### Architecture Types Comparison

| Aspect | Monolithic | Distributed |
|--------|------------|-------------|
| Deployment | Single unit | Multiple units |
| Communication | Local method calls | Network calls (REST, messaging) |
| Data | Single database | Multiple databases |
| Cost | Low | High |
| Complexity | Simple at start | Complex from beginning |
| Scalability | Scale everything | Scale individual services |
| Team Structure | One team | Multiple teams |

---

## 2.2.1 Common Fallacies in Distributed Computing

### Introduction

The **Fallacies of Distributed Computing** are common mistakes people make when dealing with distributed systems. These misconceptions can cause big issues. Understanding them helps build stronger systems.

### Fallacy 1: The Network is Reliable

**The Mistake:** Believing the network will always work without problems.

**Reality:** Networks are vulnerable to:
- Packet drops
- Delays
- Connection loss
- Hardware breakdowns
- Software issues
- Physical disruptions

**How to Fix:**
- Build flexible, reliable mechanisms
- Implement proper retry logic
- Add redundancy features

---

### Fallacy 2: Latency is Zero

**The Mistake:** Assuming data transfers instantly across networks.

**Reality:** Multiple causes of latency:
- Distance between destinations
- Network congestion
- Processing delays

**Compare:**
- Monolithic: Local calls in nanoseconds
- Distributed: Remote calls in milliseconds

**How to Fix:**
- Use caching
- Implement asynchronous communication
- Consider latency in design

---

### Fallacy 3: Bandwidth is Infinite

**The Mistake:** Thinking the network can handle unlimited data.

**Reality:** Bandwidth is the amount of data that can be transferred over time. It can be a rate-limiting factor for high-tempo applications.

**Example:**
- 1000 concurrent requests can eat up bandwidth
- Slows down the network
- Increases latency between calls

**How to Fix:**
- Use compression
- Implement data encoding
- Prioritize critical data
- Manage bandwidth usage

---

### Fallacy 4: The Network is Secure

**The Mistake:** Believing the network is inherently safe.

**Reality:** Networks can be:
- Tapped (eavesdropped)
- Breached
- Attacked by unfriendly actors
- At higher risk in distributed systems (more surface area)

**How to Fix:**
- Use encryption
- Implement authentication
- Add authorization
- Regular security audits
- Keep security patches updated

---

### Fallacy 5: Topology Doesn't Change

**The Mistake:** Assuming network topology is fixed.

**Reality:** Topology changes all the time:
- New nodes added
- Existing nodes fail
- Configurations altered
- Routers, hubs, switches, firewalls change

**How to Fix:**
- Use dynamic routing techniques
- Implement load balancing
- Add self-healing capabilities
- Never assume fixed topology

---

### Fallacy 6: There is One Administrator

**The Mistake:** Thinking one person controls everything.

**Reality:** Distributed systems operate across multiple administrative territories. There is never a single administrator.

**Who is involved:**
- Network team
- Security team
- Database team
- Cloud team
- Application team

**How to Fix:**
- Clear communication channels
- Uniform protocols
- Shared leadership structures
- Collaborate with multiple admins

---

### Fallacy 7: Transport Cost is Zero

**The Mistake:** Believing network communication has no cost.

**Reality:** Transport cost includes:
- Network bandwidth usage
- Power consumption
- Additional hardware costs
- Servers, gateways, firewalls
- New subnets, proxies

**Monolithic vs Distributed:**
- Monolithic: Local method calls (no transport cost)
- Distributed: REST calls (significant cost)

**How to Fix:**
- Streamline data traffic
- Cut unnecessary costs
- Use resource-friendly infrastructure

---

### Fallacy 8: The Network is Homogeneous

**The Mistake:** Assuming all network parts are the same.

**Reality:** Networks have diverse elements:
- Different hardware vendors
- Different configurations
- Different operating parameters
- Not all vendors work well together

**How to Fix:**
- Design for diversity
- Build flexible systems
- Create adaptable properties
- Test with heterogeneous setups

---

### Fallacy 9: The System is Monolithic

**The Mistake:** Thinking the system is one single entity.

**Reality:** Distributed systems consist of multiple interacting components. They are separate and complex systems.

**How to Fix:**
- Manage component interactions carefully
- Track dependencies
- Monitor integration points
- Maintain system uniformity

---

### Fallacy 10: The System is Fully Observable

**The Mistake:** Believing you can see everything happening.

**Reality:** Achieving perfect listening to all components is very difficult due to:
- Inherent complexity
- System size
- Low transparency for monitoring

**How to Fix:**
- Implement proper logging
- Add monitoring tools
- Use distributed tracing
- Build robust observability

---

### Fallacy 11: The System is Always On

**The Mistake:** Assuming no downtime ever.

**Reality:** Downtime happens from:
- Scheduled maintenance
- System failures
- Network problems

**How to Fix:**
- Build redundancy
- Implement failover
- Create disaster recovery plans
- Design for interruptions

---

### Fallacy 12: There is One Root Cause

**The Mistake:** Trying to find one single cause for failures.

**Reality:** Distributed systems have multiple, associated causes of failure. Systems are highly interactive.

**How to Fix:**
- Use variety of analytic tools
- Identify multiple contributing factors
- Complete failure investigation
- Consider all possibilities

---

### Fallacy 13: Failures are Rare

**The Mistake:** Underestimating how often failures happen.

**Reality:** Critical failures happen frequently in distributed systems due to:
- Node dispersal
- Hardware inventory
- Software issues
- Network problems

**How to Fix:**
- Build survivable systems
- Add duplicate capacity
- Implement failover
- Create robust error correction
- Design for recurring failures

---

### Summary Table of Fallacies

| # | Fallacy | Reality | Key Solution |
|---|---------|---------|---------------|
| 1 | Network is reliable | Networks fail constantly | Retry, redundancy |
| 2 | Latency is zero | Network calls take time | Caching, async |
| 3 | Bandwidth is infinite | Bandwidth is limited | Compression, prioritization |
| 4 | Network is secure | Networks are vulnerable | Encryption, auth |
| 5 | Topology doesn't change | Topology changes often | Dynamic routing |
| 6 | One administrator | Multiple teams involved | Clear communication |
| 7 | Transport cost is zero | Network calls cost money | Streamline data |
| 8 | Network is homogeneous | Different vendors, configs | Design for diversity |
| 9 | System is monolithic | Multiple components | Manage interactions |
| 10 | System is fully observable | Hard to see everything | Logging, tracing |
| 11 | System is always on | Downtime happens | Redundancy, failover |
| 12 | One root cause | Multiple causes | Complete investigation |
| 13 | Failures are rare | Failures happen often | Design for failure |

---

### Key Takeaways

1. **Don't assume the network is reliable** - always plan for failures
2. **Latency matters** - what works locally may not work remotely
3. **Bandwidth is limited** - manage data transfer wisely
4. **Security is your responsibility** - never trust the network
5. **Topology changes** - build dynamic systems
6. **Multiple administrators exist** - communicate across teams
7. **Transport costs real money** - consider the budget
8. **Networks are diverse** - test with different hardware
9. **Systems are not monolithic** - manage component interactions
10. **Observability is hard** - invest in monitoring tools
11. **Downtime will happen** - plan for it
12. **Failures have multiple causes** - investigate thoroughly
13. **Failures are common** - build resilient systems

---

### References

- Deutsch, P. (1994). "The Eight Fallacies of Distributed Computing"
- GeeksforGeeks. (2025). "Fallacies of Distributed Systems"
- Panchal, S. (2022). "Monolithic V/s Distributed Architectures"
- Ford, N., Richards, M., Sadalage, P., & Dehghani, Z. (2021). "Software Architecture: The Hard Parts"

