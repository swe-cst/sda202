# Architecture Pitch Activity

## Activity Instructions

> "You are now senior architects at a consulting firm. A client has walked in with a business problem. You have 25 minutes to design their system architecture. Your job is not to build it—your job is to make a recommendation they can trust.
>
> **Your deliverables:**
>
> 1. Choose ONE architecture style (Big Ball of Mud, Unitary, Client/Server)
> 2. Write THREE justification points based on the scenario constraints
> 3. Identify ONE major risk
> 4. Prepare a 90-second pitch to convince the CTO
>
> **Rules:**
>
> - No 'it depends'—make a decision
> - You must explain WHY, not just WHAT
> - Be ready to defend against peer critique

---

## Scenario Cards (14 Groups)

### **Group 1: Food Truck Ordering App**

**Context:** A single food truck owner wants customers to order via mobile app to reduce wait times. Peak load: 50 orders/hour. Owner manages orders via tablet. Budget: Nu. 500. Timeline: 2 weeks. Technical skill: Owner knows Excel.

**Constraints:**

- Single user (owner) on backend
- Customers need simple menu display
- No internet at some food truck locations
- Owner will manually confirm orders

---

### **Group 2: University Club Event Registration**

**Context:** A student club needs a website for their annual festival. Expected: 500 registrations over 2 weeks. Team: 3 computer science students working for free. Timeline: 3 weeks. Must handle ticket payments via reference number of online banking payment.

**Constraints:**

- Volunteers with limited time
- One-time event (won't be reused)
- Must look professional for sponsors
- Data privacy concerns (student emails)

---

### **Group 3: Personal Finance Tracker**

**Context:** A freelancer wants to track income and expenses across 3 freelance gigs. They are the only user. They know basic spreadsheet skills but want something automated. Timeline: "I want it by next week." Budget: Nu. 0.

**Constraints:**

- Single user
- Data sensitive (bank transactions)
- User is not technical
- May want to share reports with accountant later

---

### **Group 4: Local Library Digital Catalog**

**Context:** A small community library with 2,000 books wants to digitize their catalog. Staff: 2 librarians (non-technical). Budget: Nu. 200. Timeline: 1 month. Currently using index cards.

**Constraints:**

- Staff cannot maintain complex systems
- Only used during library hours
- Need to search by title, author, genre
- No plans to expand beyond this library

---

### **Group 5: Food Delivery Startup**

**Context:** A startup launching in one city. Expects 500 users in month 1, growing to 10,000 in year 1. Will have web and mobile apps. Team: 5 developers. Timeline: 4 months. Investors want to see scalability plan.

**Constraints:**

- Multiple client types (iOS, Android, Web)
- Real-time order tracking needed
- Payment processing required
- Competition means fast iteration is critical

---

### **Group 6: Telehealth Consultation Platform**

**Context:** A healthcare startup connecting patients with doctors via video. Must handle 200 concurrent video sessions. Must follow the regulations of the Ministry of Health. Team: 8 developers. Timeline: 9 months. Medical investors backing.

**Constraints:**

- Strict security requirements
- Video streaming infrastructure needed
- Patient records must be secure
- Doctors need reliable 99.9% uptime

---

### **Group 7: Construction Project Management Tool**

**Context:** A construction company wants to track 50 active job sites. Project managers need to update status, upload photos, assign workers. Team: 4 developers. Timeline: 6 months. Currently using WhatsApp and spreadsheets.

**Constraints:**

- Workers in field have limited connectivity
- Photos need to sync when connection returns
- Office managers need real-time dashboards
- System must work offline for field workers

---

### **Group 8: Local E-commerce Marketplace**

**Context:** A platform for local artisans to sell handmade goods. Launching with 50 sellers, expecting 500 sellers in year 1. Team: 6 developers. Timeline: 5 months. Must handle inventory, payments, shipping.

**Constraints:**

- Multi-tenant (each seller sees their own data)
- Payment splitting (platform takes commission)
- Search and discovery important
- Sellers are not technical

### **Group 9: National Census System**

**Context:** Government census for 50 million citizens. Conducted once every 5 years. Data accuracy is legally critical. Unlimited budget. Timeline: 4 years. Multiple government agencies will access results.

**Constraints:**

- Peak usage: 1 month of data collection
- Must be 99.99% accurate
- Multiple stakeholders with different data needs
- Security classified as critical infrastructure

---

### **Group 10: IoT Sensor Network for Agriculture**

**Context:** 10,000 sensors across farms monitoring soil moisture, temperature, and crop health. Sensors send data every 5 minutes. Farmers need alerts when conditions change. Team: 12 developers. Timeline: 18 months.

**Constraints:**

- Massive data ingestion (10k sensors × 288 readings/day)
- Sensors have intermittent connectivity
- Real-time alerts needed for frost/drought
- Data analysis for yield prediction

---

### **Group 11: Banking Transaction System**

**Context:** A digital bank processing 1 million transactions daily. Must maintain accurate balances with zero errors. Regulatory audits required. Team: 20 developers. Timeline: 2 years (replacing legacy system).

**Constraints:**

- Atomic transactions (cannot lose money)
- 99.999% uptime required
- Must pass security audits
- Integration with existing banking infrastructure

---

### **Group 12: Social Media Platform for Creators**

**Context:** A TikTok competitor targeting creators. Launching with 100,000 beta users. Expected to scale to 10 million in year 1. Team: 25 developers. Features: video uploads, comments, likes, follows, recommendations.

**Constraints:**

- Video storage and streaming at scale
- Recommendation algorithm needs constant iteration
- Viral spikes can be 1000x normal traffic
- Content moderation required

### **Group 13: Museum Interactive Guide**

**Context:** A museum wants a mobile app that uses Bluetooth beacons to detect visitor location and play audio guides. Museum has 20 rooms, 500 daily visitors. Team: 3 developers. Timeline: 2 months. Budget: Nu. 15,000.

**Constraints:**

- Indoor positioning without GPS
- Audio files stored locally on device
- App must work offline (poor museum cellular)
- Content will be updated quarterly

---

### **Group 14: Emergency Alert System**

**Context:** A city government needs a system to send emergency alerts (floods, fires, evacuations) to all residents. Must reach 500,000 people within 5 minutes of activation. Team: 5 developers. Timeline: 8 months. Critical infrastructure.

**Constraints:**

- Must work when cell networks are congested
- Multiple channels (SMS, app push, sirens)
- Authentication required for authorized senders
- System must never fail during actual emergency

---
