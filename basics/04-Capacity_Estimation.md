# Capacity Estimation

## Definition
Capacity Estimation is the process of calculating how much traffic, storage, bandwidth, memory, and servers a system needs to handle expected load efficiently.

---

# Why It Is Important
- Helps design scalable systems
- Prevents server crashes
- Avoids over-spending on infrastructure
- Identifies bottlenecks early

---

# Main Things Estimated

## 1. Traffic Estimation
Number of users or requests coming to the system.

### Formula
RPS = Total Requests / Seconds in a Day

### Example
- 10M requests/day

RPS = 10,000,000 / 86400 ≈ 115 RPS

---

## 2. Peak Traffic
Traffic is not constant throughout the day.

### Common Assumption
Peak Load = Average Load × 5

### Example
115 × 5 = 575 RPS

---

## 3. Storage Estimation
Calculating total data stored.

### Formula
Storage = Number of Files × File Size

### Example
- 1M images/day
- Each image = 2 MB

Storage/day = 2 TB

---

## 4. Bandwidth Estimation
Amount of data transferred per second.

### Formula
Bandwidth = Response Size × Requests/sec

---

## 5. Server Estimation
Calculating number of servers needed

### Formula
Servers Needed = Peak RPS / Capacity of One Server

---

# Common Interview Assumptions

| Metric | Value |
|---|---|
| 1 Day | 86400 sec |
| Peak Traffic | 5x average |
| Read:Write Ratio | 80:20 |
| 1 GB | 1024 MB |

---

# Real-Life Example
## YouTube
Estimate:
- video uploads/sec
- video views/sec
- storage growth
- CDN bandwidth
- database load

---

# Interview Flow
1. Clarify requirements
2. Estimate users and traffic
3. Estimate storage
4. Estimate bandwidth
5. Design architecture

---

# Common Mistakes
- Ignoring peak traffic
- Ignoring future growth
- Calculating only total users
- Ignoring read/write ratio

---

# Interview Answer
Capacity Estimation is the process of calculating the infrastructure requirements of a system such as traffic, storage, bandwidth, and servers based on expected load to build scalable and reliable systems.
