# 🛠️ Technology Stack Guide

Recommended technologies for AI-age system architectures.

---

## Core Infrastructure

| Layer | Recommended | Alternatives |
|-------|-------------|--------------|
| **Cloud** | AWS, GCP, Azure | Cloudflare, Vercel |
| **Kubernetes** | EKS, GKE, AKS | k3s, Rancher |
| **Service Mesh** | Istio, Linkerd | Consul Connect |
| **API Gateway** | Kong, AWS API Gateway | Traefik, Envoy |

---

## Data Layer

### Operational Databases
| Type | Primary | Alternatives |
|------|---------|--------------|
| **Relational** | PostgreSQL | CockroachDB, TiDB |
| **Document** | MongoDB | Couchbase |
| **Key-Value** | Redis | DragonflyDB, Valkey |
| **Time-Series** | TimescaleDB | InfluxDB, QuestDB |

### Analytical Databases
| Type | Primary | Alternatives |
|------|---------|--------------|
| **OLAP** | Snowflake, Databricks | ClickHouse, DuckDB |
| **Data Lake** | Delta Lake | Apache Iceberg, Hudi |
| **Real-time** | Apache Kafka + Flink | Redpanda, RisingWave |

### Vector Databases (AI-Native)
| Purpose | Primary | Alternatives |
|---------|---------|--------------|
| **Embeddings** | Pinecone | Weaviate, Qdrant |
| **Hybrid Search** | Elasticsearch | Meilisearch |
| **Graph + Vector** | Neo4j | TigerGraph |

---

## AI/ML Infrastructure

### Foundation Models
```mermaid
graph LR
    subgraph Cloud["Cloud APIs"]
        C[Claude 3.5]
        G[GPT-4o/o1]
        M[Gemini Ultra]
    end
    
    subgraph Self["Self-Hosted"]
        L[Llama 3.3]
        Q[Qwen 2.5]
        D[DeepSeek]
    end
    
    subgraph Serving["Inference"]
        V[vLLM]
        T[TensorRT-LLM]
        O[Ollama]
    end
```

### Agent Frameworks
| Framework | Best For |
|-----------|----------|
| **LangChain** | RAG, chains, general AI apps |
| **LlamaIndex** | Data indexing, retrieval |
| **CrewAI** | Multi-agent collaboration |
| **AutoGen** | Conversational agents |
| **Semantic Kernel** | Enterprise .NET/Python |

### MLOps
| Stage | Tools |
|-------|-------|
| **Experiment** | MLflow, Weights & Biases |
| **Training** | Ray, PyTorch Lightning |
| **Serving** | Triton, BentoML, KServe |
| **Monitoring** | Arize, Whylabs, Evidently |

---

## Observability

```mermaid
graph TB
    subgraph Collect["Collection"]
        M[Metrics - Prometheus]
        L[Logs - Loki/ELK]
        T[Traces - Jaeger/Tempo]
        P[Profiles - Pyroscope]
    end
    
    subgraph Analyze["Analysis"]
        G[Grafana]
        D[Datadog]
        N[New Relic]
    end
    
    subgraph AI["AI-Powered"]
        A[Anomaly Detection]
        R[Root Cause Analysis]
        F[Forecasting]
    end
    
    Collect --> Analyze --> AI
```

---

## Security

| Layer | Tools |
|-------|-------|
| **Identity** | Okta, Auth0, Keycloak |
| **Secrets** | Vault, AWS Secrets Manager |
| **SAST/DAST** | Snyk, Semgrep, Checkmarx |
| **Runtime** | Falco, Sysdig |
| **AI Security** | Prompt injection detection, guardrails |

---

## Event-Driven Architecture

```mermaid
graph LR
    P[Producers] --> K[Kafka/Redpanda]
    K --> C[Consumers]
    K --> F[Flink/Spark]
    F --> S[Storage]
    F --> A[AI Processing]
```

| Component | Options |
|-----------|---------|
| **Message Broker** | Kafka, Redpanda, Pulsar |
| **Stream Processing** | Flink, Spark Streaming, Kafka Streams |
| **Event Store** | EventStoreDB, Kafka + Compact Topics |

---

## Edge & CDN

| Use Case | Options |
|----------|---------|
| **CDN** | Cloudflare, Fastly, AWS CloudFront |
| **Edge Compute** | Cloudflare Workers, Lambda@Edge |
| **Edge AI** | NVIDIA Jetson, AWS Panorama |
