<h1 align="center">Tunahan Ali Öztürk</h1>

<p align="center"><b>Senior .NET Backend Developer</b><br>
Distributed systems · Multi-tenant SaaS · Event-driven architecture · Applied AI (RAG, MCP)</p>

<p align="center">
  <a href="https://linkedin.com/in/tunahan-ali-ozturk"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://www.nuget.org/profiles/Moongazing"><img src="https://img.shields.io/badge/NuGet-Moongazing-004880?style=flat-square&logo=nuget&logoColor=white" alt="NuGet"></a>
  <a href="mailto:tunahan.ali.ozturk@outlook.com"><img src="https://img.shields.io/badge/Email-333333?style=flat-square&logo=maildotru&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/NuGet%20downloads-360K%2B-004880?style=flat-square" alt="360K+ NuGet downloads">
</p>

---

I build backends that are still easy to change six months later: clean boundaries, observability from day one, and fast releases that don't break production. I've spent 8+ years on .NET across SaaS, fintech, retail and e-learning. Today I design multi-tenant platforms on Azure and build AI features with Azure OpenAI, RAG and MCP.

- **Day job:** architecture of multi-tenant license and subscription platforms on the Microsoft Partner Center APIs
- **Open source:** Orion, 25+ standalone .NET libraries, 100+ NuGet packages, 360,000+ downloads
- **Lately:** retrieval pipelines, LLM gateways and MCP servers that give models real tools

## Orion: focused .NET libraries for distributed systems

Small, single-purpose, production-shaped building blocks. One rule from day one: **the cores never depend on each other**, so you take one and the rest stay out of your project.

| Library | What it does | Downloads |
| --- | --- | --- |
| [OrionGuard](https://github.com/tunahanaliozturk/OrionGuard) | Guard clause and validation ecosystem: security guards, source generator, 22 integration packages | ![](https://img.shields.io/nuget/dt/OrionGuard?style=flat-square&label=) |
| [OrionLock](https://github.com/tunahanaliozturk/OrionLock) | Distributed locking with lease auto-renewal (Redis, PostgreSQL, SQL Server, EF Core) | ![](https://img.shields.io/nuget/dt/OrionLock?style=flat-square&label=) |
| [OrionAudit](https://github.com/tunahanaliozturk/OrionAudit) | EF Core audit trail: JSON Patch diffs, multi-tenant, time-travel reconstruction | ![](https://img.shields.io/nuget/dt/OrionAudit?style=flat-square&label=) |
| [OrionPatch](https://github.com/tunahanaliozturk/OrionPatch) · [OrionInbox](https://github.com/tunahanaliozturk/OrionInbox) | Transactional outbox and inbox: at-least-once out, exactly-once effects in | ![](https://img.shields.io/nuget/dt/OrionPatch?style=flat-square&label=) |
| [OrionVault](https://github.com/tunahanaliozturk/OrionVault) | Column-level AES-256-GCM encryption at rest for EF Core, with key rotation | ![](https://img.shields.io/nuget/dt/OrionVault?style=flat-square&label=) |
| [OrionKey](https://github.com/tunahanaliozturk/OrionKey) | Source-generated strongly typed IDs, Native AOT clean | ![](https://img.shields.io/nuget/dt/OrionKey?style=flat-square&label=) |
| [OrionSaga](https://github.com/tunahanaliozturk/OrionSaga) | In-process saga orchestration with automatic compensation | ![](https://img.shields.io/nuget/dt/OrionSaga?style=flat-square&label=) |
| [OrionBeacon](https://github.com/tunahanaliozturk/OrionBeacon) | Leader election with renewable leases and fencing tokens | ![](https://img.shields.io/nuget/dt/OrionBeacon?style=flat-square&label=) |
| [OrionOnce](https://github.com/tunahanaliozturk/OrionOnce) | HTTP idempotency middleware for ASP.NET Core | ![](https://img.shields.io/nuget/dt/OrionOnce?style=flat-square&label=) |
| [OrionRelay](https://github.com/tunahanaliozturk/OrionRelay) | Outbound webhook delivery: HMAC signing, backoff with jitter | ![](https://img.shields.io/nuget/dt/OrionRelay?style=flat-square&label=) |

<details>
<summary><b>More from the family</b></summary>
<br>

| Area | Libraries |
| --- | --- |
| Security | [OrionGrant](https://github.com/tunahanaliozturk/OrionGrant) permissions and policies · [OrionLedger](https://github.com/tunahanaliozturk/OrionLedger) API key lifecycle · [OrionShade](https://github.com/tunahanaliozturk/OrionShade) secret and PII redaction |
| APIs and streaming | [OrionStream](https://github.com/tunahanaliozturk/OrionStream) Server-Sent Events · [OrionEnvelope](https://github.com/tunahanaliozturk/OrionEnvelope) RFC 9457 response contract · [OrionPage](https://github.com/tunahanaliozturk/OrionPage) keyset pagination |
| Resilience | [OrionResilience](https://github.com/tunahanaliozturk/OrionResilience) retry and timeout · [OrionRate](https://github.com/tunahanaliozturk/OrionRate) rate limiting · [OrionCache](https://github.com/tunahanaliozturk/OrionCache) stampede-free cache-aside |
| Foundations | [OrionResult](https://github.com/tunahanaliozturk/OrionResult) Result and Option · [OrionClock](https://github.com/tunahanaliozturk/OrionClock) testable time · [OrionLens](https://github.com/tunahanaliozturk/OrionLens) correlation context · [OrionFlag](https://github.com/tunahanaliozturk/OrionFlag) feature flags · [OrionHealth](https://github.com/tunahanaliozturk/OrionHealth) liveness and readiness · [Orion.Abstractions](https://github.com/tunahanaliozturk/Orion.Abstractions) |

**[OrionShowcase](https://github.com/tunahanaliozturk/OrionShowcase)** wires the core libraries into a production-shaped banking sample (Clean Architecture, EF Core, MediatR, OpenTelemetry). One `docker compose up` brings up the API, Postgres, Seq and Jaeger.

</details>

## Distributed systems, proven under failure

Each of these ships with the failure it was built to survive, reproduced on purpose.

| Project | Description |
| --- | --- |
| [matchbook](https://github.com/tunahanaliozturk/matchbook) | Purchase-to-pay ERP as five .NET 10 microservices, reconciled across five databases after chaos (MassTransit, RabbitMQ, Keycloak, YARP) |
| [order-saga-system](https://github.com/tunahanaliozturk/order-saga-system) | One order flow, two saga strategies: orchestration vs choreography, with outbox and idempotency |
| [hookrelay](https://github.com/tunahanaliozturk/hookrelay) | Signed, ordered, replayable webhook delivery, proven against a receiver that fails 30% of requests |
| [walrus](https://github.com/tunahanaliozturk/walrus) | Postgres logical replication CDC into ordered, idempotent sinks, proven under source failover |
| [tallyhouse](https://github.com/tunahanaliozturk/tallyhouse) | Kafka-buffered analytics ingest with exactly-once counting and sub-second funnels on ClickHouse |
| [keyward](https://github.com/tunahanaliozturk/keyward) | OpenID Connect provider that revokes the whole token family on refresh-token replay |
| [grantpath](https://github.com/tunahanaliozturk/grantpath) | Relationship-based authorization with decisions you can still explain weeks later |
| [microquote](https://github.com/tunahanaliozturk/microquote) | Sub-millisecond, zero-allocation pricing API, benchmarked against the plain MVC version |

## AI and developer tooling

| Project | Description |
| --- | --- |
| [partner-center-mcp](https://github.com/tunahanaliozturk/partner-center-mcp) | MCP server: knowledge and codegen assistant for the Microsoft Partner Center REST API |
| [tollgate](https://github.com/tunahanaliozturk/tollgate) | LLM gateway: holds provider keys, caps team spend, fails over without double billing |
| [Vectra](https://github.com/tunahanaliozturk/Vectra) | Semantic and hybrid search on .NET 10, PostgreSQL and pgvector |
| [graphrag-hotpotqa](https://github.com/tunahanaliozturk/graphrag-hotpotqa) | LLM-built knowledge graph with Leiden communities and local/global GraphRAG search |
| [secure-dotnet-skills](https://github.com/tunahanaliozturk/secure-dotnet-skills) | Aegis: agent skills for secure, production-grade .NET on Azure |
| [atelier](https://github.com/tunahanaliozturk/atelier) | Agent-orchestration plugin for Claude Code: plan review, approval gating, task routing |

## Applications

| Project | Description |
| --- | --- |
| [Lendora](https://github.com/tunahanaliozturk/Lendora) | Fintech lending backend (.NET 10, PostgreSQL, Redis) covering the full loan lifecycle |
| [Veil](https://github.com/tunahanaliozturk/Veil) | Sensitive data masking and PII-safe logging for .NET |
| [KeyVaultSync](https://github.com/tunahanaliozturk/KeyVaultSync) | CLI that syncs appsettings.json into Azure Key Vault |

## Tech

| | |
| --- | --- |
| **Languages** | C# · TypeScript · Python · Go |
| **Backend** | .NET 10 · ASP.NET Core · EF Core · gRPC · REST · GraphQL |
| **Architecture** | DDD · CQRS · Clean and Vertical Slice · event-driven · sagas · outbox/inbox |
| **Data** | PostgreSQL · SQL Server · Redis · MongoDB · Elasticsearch · ClickHouse |
| **Messaging** | Kafka · RabbitMQ · Azure Service Bus · MassTransit · SignalR |
| **Cloud** | Azure (AKS, Functions, Service Bus, Key Vault, OpenAI) · AWS (Lambda, ECS, RDS) |
| **DevOps and observability** | Docker · Kubernetes · Helm · GitHub Actions · OpenTelemetry · Prometheus · Grafana · Serilog · Polly |

## GitHub

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=tunahanaliozturk&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&theme=graywhite" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs?username=tunahanaliozturk&layout=compact&hide_border=true&langs_count=8&theme=graywhite" alt="Top languages" />
</p>
<p align="center">
  <img height="165" src="https://github-readme-streak-stats.herokuapp.com/?user=tunahanaliozturk&hide_border=true&theme=graywhite" alt="Streak" />
</p>

<p align="center"><sub><a href="https://github.com/tunahanaliozturk?tab=repositories">All repositories</a> · <a href="https://www.nuget.org/profiles/Moongazing">All NuGet packages</a></sub></p>
