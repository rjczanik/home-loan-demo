# home-loan-demo

This is a demo to show how a home loan system in the Netherlands would receive documents, evaluate the uploaded documents, and almost on the fly give you an indication on whether you can afford the house, and if the asking price is a reasonable buy.

## Overview

This project is a full-stack, Docker-based demo of a modern home loan system. It integrates a Databricks/Spark-based datalakehouse using Delta tables, Java 23 data ingestion pipelines, Python-based AI and risk models, and a React front-end.

### Architecture

- **Datalakehouse:**  
  Built on Databricks/Spark, using Delta tables for scalable, reliable storage and analytics.
- **Java 23 Data Pipelines:**  
  Microservices for ingesting and processing documents uploaded via the portal.
- **Python AI & Risk Models:**  
  (Planned) Analyze ingested data for affordability and risk assessment.
- **React Front-End:**  
  Allows users to create profiles, log in, and upload documents.
- **Docker Stack:**  
  All components are containerized for easy deployment and orchestration.

## Features (First Release)

- Document ingestion pipeline (Java 23) for uploaded documents
- Basic React front-end:
  - User registration and login
  - Document upload

## Getting Started

### Prerequisites

- Docker & Docker Compose
- Java 23
- Python 3.10+
- Node.js 18+

### Quick Start

1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-org/home-loan-demo.git
   cd home-loan-demo
   ```

2. **Start the stack:**
   ```sh
   docker compose up --build
   ```

3. **Access the application:**
   - Front-end: [http://localhost:3000](http://localhost:3000)
   - Databricks/Spark UI: [http://localhost:8080](http://localhost:8080) (if exposed)

4. **Development:**
   - Java pipeline: `cd ingestion-pipeline && ./gradlew bootRun`
   - Front-end: `cd frontend && npm install && npm start`
   - Python models: (future releases)

## Roadmap

- Integrate Python AI/risk models for real-time evaluation
- Expand front-end features (loan status, feedback, etc.)
- Add support for additional document types

## License

This project is released into the public domain under [The Unlicense](LICENSE).