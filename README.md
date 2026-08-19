# Hi, I'm Marwan Youssef 👋

### Systems & Distributed Systems Engineer · Security Researcher

I build **high-performance systems across the entire computing stack** — from CPU pipelines, memory management, and kernel runtimes to distributed systems, financial infrastructure, and offensive security.

My work sits at the intersection of:

**Low-Level Systems · Distributed Systems · Security · Performance Engineering**

---

## ⚙️ What I Build

* **Systems & Kernel Engineering** — CPU pipeline simulation, VMM/MMU address translation, page tables, ELF loaders, relocations, memory-safety primitives, asynchronous runtimes, eBPF/XDP.
* **Distributed Systems** — event-driven architectures, Kafka-based pipelines, Saga & Outbox patterns, geo-sharding, distributed caching, consistency, and fault isolation.
* **Financial Infrastructure** — double-entry ledgers, transactional guarantees, concurrency control, idempotency, and double-spend prevention.
* **Offensive Security** — web/API exploitation, business-logic vulnerabilities, ROP/JOP analysis, CFI, stack protection, W⊕X enforcement, and hardened microservices.
* **Performance Engineering** — cache hierarchy modeling, pipeline hazards, forwarding, CPI analysis, benchmarking, and low-level optimization.

---

## 🛠️ Core Engineering Stack

### Languages

`C` · `C++20` · `Rust` · `Go` · `x86-64 Assembly` · `C#` · `TypeScript` · `SQL` · `Bash`

### Systems

`Linux` · `Kernel Internals` · `VMM/MMU` · `PML4` · `Paging` · `ELF` · `eBPF` · `XDP` · `Thread Pools` · `Memory Management`

### Distributed Systems

`Apache Kafka` · `Redis` · `Redis Streams` · `PostgreSQL` · `CockroachDB` · `gRPC` · `Docker`

### Security

`Burp Suite` · `Metasploit` · `PortSwigger` · `ROP/JOP` · `CFI` · `Stack Canaries` · `W⊕X` · `API Security`

### Engineering & Tooling

`Git` · `Linux` · `CMake` · `Make` · `XeLaTeX` · `Benchmarking` · `System Tracing`

---

# 🚀 Featured Research & Engineering Projects

## 1. Mini Systems Stack — Threat Shield

**Research-grade systems stack combining CPU pipeline simulation, MMU/VMM components, kernel-runtime primitives, and hardware-aware security mechanisms.**

### 🔬 Architecture

Threat Shield integrates security checks across the system lifecycle:

`Fetch → Decode → Execute → Memory → Retire`

and extends protection into:

`Virtual Address → Page Table Walk → Physical Memory`

### 🛡️ Security Mechanisms

* Runtime **W⊕X memory enforcement**
* Per-process dynamic stack canaries
* Strict memory bounds checking
* Lightweight CFI return-address validation
* ROP/JOP detection mechanisms
* Page-table and address-translation validation
* Thread isolation through bounded asynchronous workers

### 📊 Benchmark Results

| Metric                      |      Result |
| --------------------------- | ----------: |
| Baseline CPI                |      `1.23` |
| Protected CPI               |      `1.28` |
| CPI Overhead                |   **4.06%** |
| Synthetic Exploit Detection |    **100%** |
| False Positive Rate         |    **0.8%** |
| Stress Checks               | **500,000** |

The objective is not simply to detect attacks, but to explore **how security mechanisms can be integrated into the execution pipeline and memory-management layer while keeping performance overhead measurable and controlled.**

📄 **Research:** `docs/reports/security_architecture.pdf`

💻 **Repository:** `Marwan6112/mini-systems-stack`

---

# 2. AetherPay — Distributed Financial Infrastructure

A distributed financial backend designed around **correctness, concurrency, and event-driven architecture**.

### 💰 Ledger Engine

Implemented a double-entry accounting system in Go with:

* Transactional consistency
* PostgreSQL row-level locking
* `SELECT ... FOR UPDATE`
* Concurrency-safe balance updates
* Double-spend prevention
* Idempotent transaction processing

### 🔄 Distributed Consistency

Implemented an **Outbox Pattern** to maintain atomic consistency between:

`PostgreSQL State → Outbox → Kafka → Consumers`

This prevents the classic failure mode where a database transaction succeeds but the corresponding event is never published.

### Architecture

```text
                ┌──────────────┐
                │   API Layer  │
                └──────┬───────┘
                       │
                ┌──────▼───────┐
                │ Ledger Core  │
                │     Go       │
                └──────┬───────┘
                       │
             ┌─────────▼─────────┐
             │    PostgreSQL     │
             │  ACID + Locking   │
             └─────────┬─────────┘
                       │
                  ┌────▼────┐
                  │ Outbox  │
                  └────┬────┘
                       │
                  ┌────▼────┐
                  │  Kafka  │
                  └─────────┘
```

---

# 3. Zenith — Real-Time Spatial Infrastructure

A low-latency spatial service for real-time logistics and driver assignment.

### Core Technologies

`Go` · `Redis Streams` · `H3 Indexing` · `gRPC`

### Engineering Focus

* Real-time driver state
* Spatial indexing
* Low-latency location queries
* Event-driven assignment
* Redis Streams based communication
* Geo-sharding strategies
* Horizontal scalability

---

# 🛡️ Security Research

I approach security from both sides:

**Understanding how systems break → engineering systems that are harder to break.**

### Offensive Security

* **180+ PortSwigger Web Security Labs**
* Business logic vulnerabilities
* Authentication & authorization flaws
* API security
* Race conditions
* SSRF
* Request smuggling
* Web cache attacks
* Exploit development fundamentals
* Linux/system-level security

### Defensive Systems Security

* Control-Flow Integrity
* Dynamic stack canaries
* W⊕X memory policies
* ROP/JOP mitigation
* Memory bounds enforcement
* Hardened microservices
* Runtime isolation

---

# 📈 Engineering Philosophy

I care about the layer **underneath the abstraction**.

Instead of only asking:

> *"How do I use this system?"*

I try to understand:

> *"What is the machine actually doing?"*

That means tracing abstractions down through:

```text
Distributed Service
       ↓
   RPC / Network
       ↓
     Kernel
       ↓
 Virtual Memory
       ↓
     CPU
       ↓
 Cache Hierarchy
       ↓
   Instructions
       ↓
    Hardware
```

The goal is to become capable of **designing, debugging, securing, and optimizing systems across these boundaries**.

---

# 📚 Research & Technical Writing

I document engineering work using research-oriented workflows, including:

* USENIX-style technical papers
* IEEE-style documentation
* XeLaTeX automation
* Reproducible benchmarks
* Terminal-based architecture demonstrations
* Performance measurements
* Experimental security analysis

📄 **Security Architecture Research:**
`docs/reports/security_architecture.pdf`

---

# 🧠 Current Focus

```text
Systems Programming
        +
Distributed Systems
        +
Computer Architecture
        +
Security Engineering
        +
Performance Optimization
        ↓
High-Performance Secure Infrastructure
```

Currently going deeper into:

* CPU microarchitecture
* Operating-system internals
* Virtual memory & MMU design
* Distributed consistency
* Fault-tolerant architectures
* Kernel security
* eBPF/XDP
* High-performance networking
* Advanced exploit mitigation

---

# 🤝 Let's Connect

I'm interested in:

**Systems Engineering · Distributed Systems · Kernel Security · Computer Architecture · Performance Engineering · Security Research**

If you're working on difficult problems at the systems layer, I'd love to talk.

📫 **LinkedIn:** Marwan Youssef
💻 **GitHub:** [Marwan6112](https://github.com/Marwan6112)

---

> **Build below the abstraction.
> Measure everything.
> Break the system before someone else does.**
