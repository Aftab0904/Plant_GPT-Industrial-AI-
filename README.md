# Plant GPT | Industrial AI Assistant for Field Engineers

Plant GPT is a specialized **Multimodal RAG (Retrieval-Augmented Generation)** system designed for predictive maintenance and real-time troubleshooting in high-stakes industrial environments like Aluminium Bahrain (ALBA). 

The system acts as a technical intelligence bridge, triggered by an **Early Warning System (EWS)** that detects anomalies using **Principal Component Analysis (PCA)** 15–20 minutes before a potential failure occurs.

---

## Technical Architecture Overview

The platform integrates traditional machine learning with state-of-the-art Generative AI to provide field engineers with actionable insights from complex, multimodal data sources.

### 1. Early Warning & Triggering (PCA-based)
- **Anomaly Detection:** Continuously monitors real-time sensor streams (Temperature, Pressure, Vibration, Flow Rates).
- **PCA Model:** Uses Principal Component Analysis to identify multidimensional drifts from normal operating baselines.
- **Agent Trigger:** Once an anomaly is detected, the system triggers the RAG agent and provides the detected drift context as a "situational snapshot."

### 2. Multimodal RAG Engine
- **Technical Documentation:** High-precision retrieval from PDF manuals, maintenance logs, and safety protocols.
- **Sensor Data Integration:** Live numerical data from SCADA/IoT systems.
- **Visual Intelligence:** Processing of technical schematics, graph data, and real-time diagnostic charts.
- **Plain English Synthesis:** Translates complex multimodal inputs into simplified, conversational troubleshooting steps for field operations.

---

## Core Capabilities

- **Predictive Troubleshooting:** Provides the "What," "Where," and "Why" of an anomaly 20 minutes before it escalates.
- **Multimodal Context:** Simultaneously queries live sensor data and static technical documentation to verify mechanical issues.
- **Layout-Aware Extraction:** Advanced parsing of engineering schematics and hierarchical technical manuals.
- **Conversational Feedback:** Engineers can ask follow-up questions about specific components or safety risks during a live event.

---

## Business & Industrial Impact

- **90% Reduction in Search Time:** Engineers no longer need to manually navigate thousands of pages of technical documentation during an emergency.
- **Uptime Optimization:** Early warning allows for controlled shutdowns or rapid component replacement before catastrophic failure.
- **Knowledge Transfer:** Captures and digitizes institutional knowledge for future troubleshooting and training.

---

## Tech Stack (Conceptual)

- **AI/ML:** PCA (Scikit-Learn), LangChain (RAG Orchestration).
- **LLMs:** Llama 3 (Groq), GPT-4o-mini (Vision).
- **Data:** DuckDB (Sensor Data), ChromaDB (Vector Search).
- **Parsing:** Layout-aware parsing of engineering PDFs and charts.

---

*This project represents professional work delivered for a high-stakes industrial client (ALBA), demonstrating expertise in combining Predictive Analytics with Generative AI.*
