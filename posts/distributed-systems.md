---
title: Notes on Distributed Systems
date: 2026-03-25
tags: [Systems, Architecture, Engineering]
---

After a decade of building distributed systems, here are the lessons that were the most expensive to learn.

## The Eight Fallacies (Revisited)

Peter Deutsch's fallacies are older than most engineers writing microservices today, yet they remain painfully relevant:

1. The network is **not** reliable
2. Latency is **not** zero
3. Bandwidth is **not** infinite
4. The network is **not** secure
5. Topology **does** change
6. There is **not** one administrator
7. Transport cost is **not** zero
8. The network is **not** homogeneous

> "A distributed system is one in which the failure of a computer you didn't even know existed can render your own computer unusable." — Leslie Lamport

## CAP Theorem in Practice

The CAP theorem is often misunderstood. It's not about choosing two out of three — it's about understanding **what you sacrifice during a network partition**:

| Strategy | During Partition | Trade-off |
|----------|-----------------|-----------|
| CP | Reject writes | Users see errors |
| AP | Accept writes | Users see stale data |

Most real systems are **neither purely CP nor AP** — they make nuanced trade-offs per operation.

## Patterns That Save Lives

### Circuit Breaker

```python
class CircuitBreaker:
    def __init__(self, threshold=5, timeout=60):
        self.failures = 0
        self.threshold = threshold
        self.timeout = timeout
        self.state = "CLOSED"

    def call(self, func, *args):
        if self.state == "OPEN":
            if time_since_open() > self.timeout:
                self.state = "HALF_OPEN"
            else:
                raise CircuitOpenError()

        try:
            result = func(*args)
            self.on_success()
            return result
        except Exception as e:
            self.on_failure()
            raise e
```

### Idempotency Keys

Every mutating API call should be idempotent. Use a unique key per request:

```
POST /api/payments
Idempotency-Key: 550e8400-e29b-41d4-a716-446655440000
```

## The Golden Rule

**Design for failure.** Not because you're pessimistic — because you're realistic.

---

*The best distributed system is the one you didn't need to build.*
