# Plant GPT | Industrial AI Assistant for Field Engineers

Plant GPT is a specialized **Multimodal RAG (Retrieval-Augmented Generation)** system designed for predictive maintenance and real-time troubleshooting in high-stakes industrial environments. 

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

## System Workflow Visualization

```mermaid
flowchart TD
    subgraph "Predictive Analytics Layer"
        A[Live Sensor Streams] --> B[PCA Anomaly Detection]
        B --> C{Anomaly Detected?}
        C -->|Yes| D[Trigger RAG Agent]
    end

    subgraph "Knowledge Retrieval Layer"
        D --> E[Query Technical Manuals]
        D --> F[Fetch Live Sensor Context]
        D --> G[Analyze Maintenance Logs]
    end

    subgraph "Intelligent Synthesis Layer"
        E --> H[Multimodal LLM Processing]
        F --> H
        G --> H
        H --> I[Plain English Troubleshooting Steps]
        I --> J[Field Engineer Mobile/Tablet]
    end
```

---

## Visualization & Demo Insights

To demonstrate the system's effectiveness, the following visualizations are typically generated during the anomaly-to-resolution cycle:

### 1. PCA Anomaly Detection (Clustering & Reconstruction Error)
- **High-Dimensional Clustering:** Visualizes sensor data reduced to 2D/3D space. Normal operating states form dense, stable clusters, while anomalous drifts are identified as statistical outliers.
- **Isolation Forest Comparison:** While Isolation Forest was evaluated for its efficiency in high-dimensional outlier detection, **Principal Component Analysis (PCA)** was selected for production due to its superior reconstruction error sensitivity, providing a more reliable 15-20 minute lead time for industrial failures.
- **Reconstruction Error Trendline:** A time-series visualization tracking the variance from the learned baseline. A breach of the statistically defined "Upper Control Limit" (UCL) serves as the autonomous trigger for the RAG agent.

<p align="center">
  <img src="./assets/pca_clustering.png" width="80%" alt="PCA Clustering Visualization" />
</p>
<p align="center"><i>Figure 1: Multidimensional clustering showing normal operating baseline vs. anomalous drift.</i></p>

### 2. Multimodal Diagnostic Output
- **Sensor Trend Analysis:** High-resolution trendlines comparing real-time sensor data (e.g., vibration, thermal discharge) against predicted normal ranges.
- **Root Cause Synthesis:** The RAG system correlates the detected trendline breach with historical maintenance logs and technical schematics to provide a definitive diagnosis.

<p align="center">
  <img src="./assets/sensor_trendlines.png" width="80%" alt="Sensor Trendline Analysis" />
</p>
<p align="center"><i>Figure 2: Real-time sensor trendlines showing the 20-minute lead time provided by the PCA engine.</i></p>

---

## Business & Industrial Impact

- **90% Reduction in Search Time:** Engineers no longer need to manually navigate thousands of pages of technical documentation during an emergency.
- **Uptime Optimization:** Early warning allows for controlled shutdowns or rapid component replacement before catastrophic failure.
- **Knowledge Transfer:** Captures and digitizes institutional knowledge for future troubleshooting and training.

---

## Tech Stack (Conceptual)

- **AI/ML:** PCA (Scikit-Learn), LangChain (RAG Orchestration).
- **LLMs:** Llama 3 (Groq), GPT-4o-mini (Vision Integration).
- **Data:** DuckDB (Sensor Analytics), ChromaDB (Vector Search).
- **Parsing:** Layout-aware parsing of engineering PDFs and charts.

---

*This project represents professional work delivered for a previous organization, demonstrating expertise in combining Predictive Analytics with Generative AI for industrial reliability.*
