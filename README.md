# ASRO - Agentic Slurm Resource Optimizer

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://ctrl-gaurav.github.io/ASRO/)
[![License](https://img.shields.io/badge/license-Academic-blue)]()
[![Status](https://img.shields.io/badge/status-active-success)]()

> An intelligent AI system that automatically optimizes HPC cluster resources, reducing waste and manual intervention

## 🎯 The Problem

Large HPC clusters face critical resource management challenges:

- **GPU Underutilization**: Jobs request more resources than they use, leaving expensive hardware idle
- **Configuration Errors**: Incorrect GPU bindings cause jobs to fail or run inefficiently
- **Manual Overhead**: Administrators spend hours diagnosing issues and tuning parameters
- **Queue Congestion**: Resource waste leads to longer wait times for all users

These problems cost research facilities thousands of dollars daily and slow down scientific progress.

## 💡 Our Solution

ASRO is an intelligent multi-agent system that continuously monitors your HPC cluster, identifies inefficiencies, and safely applies optimizations with minimal human intervention. It combines real-time monitoring, AI-powered planning, and multi-stage safety mechanisms to keep your cluster running at peak efficiency.

**[View Live Documentation →](https://ctrl-gaurav.github.io/ASRO/)**

## ✨ Key Features

### 🤖 Intelligent Multi-Agent Architecture
Five specialized AI agents work collaboratively to optimize your cluster:
- **Monitor Agent** - Continuous resource tracking and anomaly detection
- **Profiler Agent** - Historical usage analysis and pattern recognition
- **Planner Agent** - AI-powered optimization recommendations
- **Executor Agent** - Safe action implementation with rollback
- **Audit Agent** - Complete transparency and approval workflows

### 🛡️ Safety-First Design
Multiple layers of protection ensure no disruption to running workloads:
- Simulation before execution
- Risk-based human approval gates
- Canary deployments for high-risk changes
- Automatic rollback on performance degradation
- Comprehensive audit trails

### 📊 Real-Time Insights
Web dashboard provides instant visibility into:
- Current cluster utilization and bottlenecks
- Pending optimization recommendations
- Historical performance trends
- Cost savings and efficiency gains

### 🔧 Enterprise-Grade Architecture
Built on proven technologies for production reliability:
- Kubernetes orchestration for scalability
- Kafka event streaming for durability
- gRPC with mTLS for secure communication
- PostgreSQL and Redis for data persistence

## 🏗️ System Design

ASRO implements a sophisticated multi-agent architecture with clear separation of concerns:

```
┌─────────────┐    ┌──────────────┐    ┌─────────────┐
│   Monitor   │───▶│   Profiler   │───▶│   Planner   │
│    Agent    │    │    Agent     │    │    Agent    │
└─────────────┘    └──────────────┘    └─────────────┘
       │                                       │
       │           ┌──────────────┐           │
       └──────────▶│    Kafka     │◀──────────┘
                   │   Backbone   │
                   └──────────────┘
                          │
                   ┌──────┴──────┐
                   │             │
            ┌──────▼─────┐ ┌────▼───────┐
            │  Executor  │ │   Audit    │
            │   Agent    │ │   Agent    │
            └────────────┘ └────────────┘
```

### 📐 Architecture Highlights

- **13 Design Components** - Modular architecture for maintainability
- **35 Requirements** - Comprehensive functional and non-functional specifications
- **10 Design Decisions** - Thoroughly justified architectural choices
- **100% Traceability** - Complete mapping from requirements to implementation

[Explore Full Architecture →](https://ctrl-gaurav.github.io/ASRO/architecture.html)

## 📚 Documentation

Our comprehensive design documentation covers every aspect of the system:

### 📋 [Requirements Specification](https://ctrl-gaurav.github.io/ASRO/requirements.html)
- 20 functional requirements covering monitoring, planning, execution, and communication
- 15 non-functional requirements for performance, security, and reliability
- Clear customer and user personas

### 🏛️ [System Architecture](https://ctrl-gaurav.github.io/ASRO/architecture.html)
- Interactive component diagrams
- Detailed agent descriptions
- Communication protocols and data flows
- Deployment architecture
- Technology stack

### 💭 [Design Rationale](https://ctrl-gaurav.github.io/ASRO/rationale.html)
- 10 key architectural decisions explained
- Alternatives considered and rejected
- Trade-off analysis
- Requirements-driven justifications

### 🔗 [Traceability Matrix](https://ctrl-gaurav.github.io/ASRO/traceability.html)
- Forward mapping: Requirements → Components
- Backward mapping: Components → Requirements
- Coverage validation
- Gap analysis

## 🎓 Academic Context

This project was developed as part of **CS 5744: Software Design and Quality** at Virginia Tech. It demonstrates advanced software design principles including:

- Multi-agent system architecture
- Event-driven communication patterns
- Safety-critical system design
- AI/LLM integration with safety constraints
- Requirements engineering and traceability
- Design rationale documentation

## 👥 Design Team

- **Gaurav Srivastava**
- **Aafiya Hussain**
- **Najibul Haque Sarker**
- **Zaber Ibn Abdul Hakim**
- **Ali Asgarov**

## 🚀 Project Motivation

This design emerged from real operational challenges we encountered:

> During job submission to Virginia Tech's ARC cluster, we received an alert about low GPU utilization. Investigation revealed our code was accessing the wrong GPU due to incorrect device mapping - a problem that required manual diagnosis and intervention. Similar resource allocation issues are common across HPC facilities worldwide.

ASRO addresses these challenges through intelligent automation while maintaining the safety guarantees required for production infrastructure.

## 🛠️ Technologies

- **Frontend**: HTML5, CSS3, JavaScript
- **Diagrams**: Mermaid.js for interactive visualizations
- **Deployment**: GitHub Pages
- **Design**: Multi-agent architecture, event-driven systems, microservices

## 📊 Key Metrics

- **35** total requirements (20 functional + 15 non-functional)
- **13** architectural components
- **10** design decisions with full justification
- **5** specialized AI agents
- **100%** requirements-to-components traceability
- **4** interactive system diagrams

## 🌐 Live Demo

**[Visit the complete design documentation →](https://ctrl-gaurav.github.io/ASRO/)**

The documentation website features:
- ✅ Professional, responsive design
- ✅ Interactive architecture diagrams
- ✅ Mobile-friendly interface
- ✅ Print-optimized layouts
- ✅ Fast navigation between sections

## 📄 License

This project is submitted as academic coursework for CS 5744: Software Design and Quality at Virginia Tech. All rights reserved by the design team.

---

<div align="center">

**CS 5744: Software Design and Quality** | **Fall 2025** | **Virginia Tech**

[Documentation](https://ctrl-gaurav.github.io/ASRO/) • [Requirements](https://ctrl-gaurav.github.io/ASRO/requirements.html) • [Architecture](https://ctrl-gaurav.github.io/ASRO/architecture.html) • [Rationale](https://ctrl-gaurav.github.io/ASRO/rationale.html)

</div>
