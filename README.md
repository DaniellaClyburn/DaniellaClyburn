Software Engineer, distributed ingestion and payments infrastructure
## @DaniellaClyburn
I build ingestion pipelines and payment APIs around durable queues, idempotent workers, and versioned schemas. I own failure modes across API boundaries, retries, cache invalidation, and operational recovery. I prefer boring implementations with explicit backpressure, bounded concurrency, and traces that survive worker restarts. I accept duplicated read models when they keep write paths predictable and migrations reversible.
### 🛠 Tech & Infrastructure
- **Core:** `TypeScript`, `Node.js`, `PostgreSQL`, `Redis`
- **Data:** `Kafka`, `Apache Avro`, `dbt`, `ClickHouse`
- **Infra:** `Docker`, `Terraform`, `GitHub Actions`
- **Tooling:** `ESLint`, `TypeScript`, `Vitest`
### ⚙️ Engineering Areas
- Durable event ingestion with schema contracts, backpressure, and replayable dead-letter queues
- Payment API boundaries with idempotency keys, state transitions, and outbox writes
- PostgreSQL schema migrations, indexing strategy, and read-model reconciliation
- Worker concurrency controls with traces, metrics, and bounded retry policies
### 🔭 Current Focus
- Moving payment webhooks into Kafka without losing at-least-once delivery guarantees
- Limiting PostgreSQL migration locks while replaying historical events into ClickHouse
- Replacing unbounded worker queues with per-tenant concurrency limits and dead-letter routing
- Adding trace propagation through RPCs, workers, and cache clients without adding latency
### 📌 Engineering Notes
- Idempotency keys belong at the service boundary, not only inside workers.
- Cache invalidation should be explicit enough to reproduce during incident review.
- Migrations stay reversible when new columns and read paths can deploy independently.
- Retry budgets need deadlines, circuit breakers, and dead-letter queues together.
### 🧭 How I Work
- Keep contracts narrow and make failure modes visible in logs and traces.
- Prefer small, reversible changes over large migrations or opaque abstraction layers.
daniellaclyburn7737@outlook.com

[Email](mailto:daniellaclyburn7737@outlook.com)