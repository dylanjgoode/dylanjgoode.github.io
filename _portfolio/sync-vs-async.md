---
title: "Sync vs Async Microservices"
excerpt: "A hands-on demonstration of Synchronous (HTTP) vs Asynchronous (Message Queues) communication patterns in microservices."
collection: portfolio
order: 7
---

**[Sync vs Async Microservices](https://github.com/dylanjgoode/sync-vs-async)**

"Why is my microservice architecture slower than my monolith?"
This project is a hands-on demonstration of the two most common communication patterns in microservices: Synchronous (HTTP) and Asynchronous (Message Queues).
It includes a Side-by-Side Visualization so you can feel the difference in latency and user experience.

![Sync vs Async](/images/syncvsasu.png) 

### What You Will Learn

- **Coupling**: Why Service A shouldn't crash just because Service B is down.
- **Latency**: How blocking calls stack up and kill performance.
- **Event-Driven Architecture**: How to use RabbitMQ to decouple services.
- **Developer Experience**: How to visualize these concepts for your team.

### The Architecture

#### 1. The "Sync" Trap (Blocking)
This is how most people start. Service A calls Service B directly.
- **The Problem**: If Payment takes 3 seconds, Checkout takes 3 seconds. The user waits.
- **The Risk**: If Payment is down, Checkout throws a 500 Error.

#### 2. The "Async" Solution (Non-Blocking)
This is how you scale. Service A sends a message and moves on.
- **The Benefit**: Checkout responds instantly. The user is happy.
- **The Resilience**: If Payment is down, the message waits in the Queue. Nothing is lost.
