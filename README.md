## Hi there

CS and Software Engineering student seeking Software Engineering internships.

I build distributed backend systems, cloud-native infrastructure, and full-stack applications. My recent work focuses on systems that handle concurrent load at scale — with benchmarks to back it up.

---

### Projects

**[ai-inference-gateway](https://github.com/powoftech/ai-inference-gateway)** — Multi-tenant API gateway for GenAI workloads, written in Go. Translates HTTP/2 SSE to gRPC streams, enforces per-tenant token quotas via a two-tier state model (in-memory `sync.Map` + async Redis), and routes traffic with a custom EWMA load balancer. Deployed and load-tested on AWS EKS:
- ~181μs gateway processing overhead (requirement: <5ms)
- 13.5% P95 latency reduction and 60% lower median TTFT vs. round-robin under degraded backend conditions
- Shed 132K+ excess requests at 1,500 concurrent users without impacting active streams

**[task-engine](https://github.com/powoftech/task-engine)** — Distributed task execution engine using polyglot microservices: Java/Spring Boot for the API gateway, Go for the worker node. Uses the Transactional Outbox pattern (Debezium CDC → RabbitMQ) to guarantee at-least-once delivery without distributed transactions. Traced end-to-end with OpenTelemetry + Jaeger. Load-tested with k6: P95 = 5.44ms at 1,000 concurrent VUs, 100% success rate across ~10,500 checks.

**[connector-nextjs](https://github.com/powoftech/connector-nextjs)** — Full-stack social platform built with Next.js, Prisma, and Docker.

**[starless](https://github.com/powoftech/starless)** — TypeScript CLI tool to bulk-unstar GitHub repositories. Supports concurrent requests, configurable rate limiting, and dry-run mode.

---

### Stack

Go · TypeScript · Java · Python · Dart  
Next.js · React · Spring Boot · FastAPI · Flutter · Tauri  
PostgreSQL · Redis · RabbitMQ  
Docker · Kubernetes · Terraform · AWS  
OpenTelemetry · Jaeger · Prometheus · k6
