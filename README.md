# VegaDB: A High-Performance Distributed Key-Value Store (Educational Project)

---

## Project Description

VegaDB is a distributed, in-memory key-value store designed for high throughput and low latency. This project is being developed from the ground up as a learning exercise to explore the concepts and challenges involved in building distributed systems. It is **not intended for production use**.

## Features (Planned)

* **In-Memory Storage:** Data is primarily stored in memory for fast access.
* **Custom TCP Protocol:** A custom TCP-based protocol for efficient communication between clients and servers.
* **Append-Only Log:** Persistence is achieved using an append-only log to ensure data durability.
* **Snapshotting:** Periodic snapshots of the in-memory data for faster recovery.
* **Hash-Based Sharding:** Data is distributed across multiple nodes using consistent hashing.
* **Client-Side Routing:** Clients are responsible for determining the correct node for each request.
* **Basic Replication:** (Planned) Data replication for fault tolerance.

---

## Goals

* **Learning:** The primary goal of this project is to learn about distributed systems, network programming, data persistence, and concurrency.
* **Understanding Trade-offs:** To gain a deeper understanding of the trade-offs involved in designing and implementing a distributed system (e.g., consistency vs. availability).
* **Practical Experience:** To get hands-on experience with Go for systems programming.

---

## Architecture (Simplified)

+----------+      +----------+      +----------+| Client 1 | ---> | Router   | ---> | Node 1   |+----------+      |          |      +----------+|          |+----------+      |          | ---> | Node 2   || Client 2 | ---> |          |      +----------++----------+      +----------+      +----------+
* **Client:** Sends requests (`GET`, `PUT`, `DELETE`) to a router.
* **Router:** (Currently, the client simulates routing) Determines the appropriate node based on the key and forwards the request.
* **Node:** Stores the data and handles the requests.

---

## Current Status

This project is currently in the early stages of development. The following components are being implemented:

* Basic single-node in-memory key-value store.
* Custom TCP protocol for client-server communication.
* Basic TCP client and server.

---

## Planned Implementation Steps

1.  Define the TCP Protocol
2.  Implement the In-Memory Store
3.  Implement the TCP Server
4.  Implement a Basic TCP Client
5.  Choose a Persistence Strategy and Format
6.  Implement Persistence Logic
7.  Sharding Strategy (Basic)
8.  Basic Request Routing (Client-Side)
9.  Simulating Multiple Nodes

---

## Dependencies

* Go (version 1.24 or later)

## Installation

```bash
git clone https://github.com/prakashpandey/vegadb.git
cd VegaDB
go build -o vega-server ./cmd/server/main.go
go build -o vega-client ./cmd/client/main.go
UsageStart the server:./vega-server
```

---
