# ⚡ Distributed Lovable — AI-Powered SaaS Application Builder

**Transform natural-language prompts into React applications with an AI-powered, cloud-native development platform.**

Distributed Lovable is an AI-powered SaaS platform designed to simplify application development through automated code generation, real-time AI streaming, persistent project storage, and Kubernetes-based application previews.

The platform combines AI integration with distributed backend services and event-driven communication to explore the architecture behind modern AI application builders.

---

## 🚀 Key Features

### 🤖 AI-Powered Code Generation
- Generate application code from natural-language instructions.
- Integrate Large Language Models (LLMs) through Spring AI.
- Stream generated responses to provide an interactive experience.
- Process structured AI output to support project and file generation workflows.

### ⚡ Real-Time AI Streaming
- Deliver incremental AI responses to the frontend.
- Use Server-Sent Events (SSE) for server-to-client streaming.
- Support interactive code-generation workflows without waiting for the entire response.

### 🏗️ Microservices Architecture
- Organize backend functionality into independent Spring Boot services.
- Use Spring Cloud components for service communication and routing.
- Separate responsibilities across account management, workspace operations, and AI intelligence.
- Improve modularity and maintainability through service boundaries.

### 📁 Distributed File Management
- Store generated project files in MinIO object storage.
- Maintain project and file metadata in PostgreSQL.
- Support file-tree retrieval and project file access.
- Use Kafka-based asynchronous processing for file persistence workflows.

### 📨 Event-Driven Communication
- Use Apache Kafka for asynchronous inter-service communication.
- Process file-storage requests through event consumers.
- Track file-processing outcomes and support reliable workflow coordination.

### ☸️ Kubernetes-Based Application Previews
- Deploy application workloads using Kubernetes.
- Use containerized runner environments for generated React applications.
- Coordinate deployment workflows through backend services.
- Explore scalable application preview infrastructure using Kubernetes and Redis-based routing.

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Languages | Java, JavaScript |
| Backend | Spring Boot, Spring Cloud, Spring AI |
| Frontend | React |
| AI Integration | LLMs, streaming responses, structured output processing |
| Databases | PostgreSQL, pgvector |
| Object Storage | MinIO |
| Messaging | Apache Kafka |
| Caching & Routing | Redis |
| Containers | Docker |
| Orchestration | Kubernetes |
| API Testing | Postman |
| Version Control | Git, GitHub |

---

## 🏛️ System Architecture

The platform follows a distributed microservices architecture in which each service handles a specific responsibility.

```text
                 ┌──────────────────────┐
                 │    React Frontend    │
                 └──────────┬───────────┘
                            │
                 ┌──────────▼───────────┐
                 │   API Gateway        │
                 └──────────┬───────────┘
                            │
            ┌───────────────┼────────────────┐
            │               │                │
   ┌────────▼──────┐ ┌──────▼───────┐ ┌──────▼────────┐
   │ Account       │ │ Workspace    │ │ Intelligence  │
   │ Service       │ │ Service      │ │ Service       │
   └───────────────┘ └──────┬───────┘ └──────┬────────┘
                            │                │
                            └───────┬────────┘
                                    │
                           ┌────────▼────────┐
                           │  Apache Kafka   │
                           └────────┬────────┘
                                    │
                       ┌────────────┴────────────┐
                       │                         │
              ┌────────▼────────┐       ┌────────▼────────┐
              │   PostgreSQL    │       │      MinIO      │
              │ Metadata & Data │       │   Project Files │
              └─────────────────┘       └─────────────────┘

                   Kubernetes Application Runners
```

*Conceptual overview; the exact service interactions depend on the implemented deployment configuration.*

---

## 🔄 How It Works

1. **User Input:** The user submits a natural-language prompt through the React interface.
2. **Request Routing:** The backend routes the request to the appropriate microservice.
3. **AI Processing:** The Intelligence Service invokes the configured LLM through Spring AI.
4. **Response Streaming:** Generated content is streamed to the frontend using Server-Sent Events.
5. **File Processing:** Generated file changes are processed through the application's file-management workflow.
6. **Persistent Storage:** Project files are stored in MinIO, while associated metadata is maintained in PostgreSQL.
7. **Asynchronous Processing:** Kafka facilitates communication between services for supported background workflows.
8. **Application Preview:** The workspace infrastructure coordinates application deployment and preview through Kubernetes-based runners.

---

## 🧠 Engineering Concepts

This project explores practical implementation of:

- Microservices architecture and service discovery.
- API gateway routing and distributed service communication.
- Server-Sent Events and asynchronous response streaming.
- LLM integration and structured response processing.
- Event-driven architecture using Apache Kafka.
- Object storage and metadata persistence.
- Containerization and Kubernetes workload orchestration.
- Distributed application preview and routing workflows.
- Separation of concerns across backend services.

---

## 📂 Repository Structure

The repository is organized around the frontend, backend microservices, and infrastructure configuration.

```text
distributed-lovable/
├── account-service/
├── workspace-service/
├── intelligence-service/
├── api-gateway/
├── config-server/
├── discovery-server/
├── lovable-frontend/
└── lovable-config-server/
```

*Directory names may vary according to the current repository structure.*

---

## 🎯 Project Goals

- Simplify application development through AI-assisted code generation.
- Explore the engineering challenges of streaming LLM responses.
- Build modular and maintainable distributed backend services.
- Implement persistent storage for generated application files.
- Explore cloud-native deployment and isolated application previews.

---

## 🔮 Future Improvements

- Improve LLM integration reliability and error handling.
- Strengthen automated testing across microservices.
- Improve application-preview startup time and resource management.
- Add robust observability, metrics, and distributed tracing.
- Improve deployment automation and production readiness.

---

## 👨‍💻 About the Project

Distributed Lovable combines AI-powered development workflows with backend engineering, distributed messaging, persistent storage, and cloud-native infrastructure.

**Focus areas:** AI Engineering · Backend Development · Distributed Systems · Microservices · Cloud-Native Applications

---

*Built with Java, Spring Boot, React, Spring AI, Kafka, PostgreSQL, MinIO, Docker, and Kubernetes.*
