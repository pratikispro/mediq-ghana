# 🏥 MedIQ: Bridging Medical Deserts in Ghana
### Databricks x Accenture Hackathon — Virtue Foundation Track

## 🎯 Project Overview

MedIQ is an AI-powered Intelligent Document Parsing (IDP) agent that analyzes healthcare facility data across Ghana to identify medical deserts, detect anomalous claims, and help NGO planners deploy resources where they're needed most.

Built on Databricks using real data from the Virtue Foundation, MedIQ processed **995 real Ghana healthcare facilities** and discovered that **71% are medical deserts** — severely under-resourced facilities that lack basic equipment, procedures, or capabilities.

---

## 🚀 What We Built

| Notebook | Description |
|---|---|
| `01_Data_Ingestion` | Loads and cleans the Virtue Foundation Ghana dataset |
| `02_IDP_Agent` | LLM-powered extraction of procedures, equipment & capabilities from free-form text |
| `03_Gap_Analyzer` | Detects medical deserts and anomalous facility claims |
| `04_Chat_Interface` | Natural language Q&A for NGO planners |
| `05_Map_Visualization` | Interactive map of medical deserts across Ghana |
| `06_Citations` | Row-level and step-level citations with MLFlow tracing |

---

## 📊 Key Findings

- **758 out of 1,067 facilities (71%)** are medical deserts
- **Western Region: 100%** of facilities are medical deserts
- **169 facilities** have anomalous or suspicious data including:
  - 80 facilities with zero medical data
  - 55 claiming surgery but no surgical theater
  - 46 claiming advanced care but no equipment
  - 5 claiming ICU but no ICU equipment
- **Saint John of God Hospital, Duayaw Nkwanta** — flagged on 3 anomalies

---

## 🏗️ Architecture

```
Ghana Facility Data (995 facilities)
        ↓
  Databricks Delta Tables
        ↓
  IDP Agent (Llama 3.3 70B via Databricks Serving)
        ↓
  Structured Extraction → Pydantic Schema Validation
        ↓
  Gap Analyzer → Medical Desert Scoring → Anomaly Detection
        ↓
  MLFlow Experiment Tracking + Row-Level Citations
        ↓
  Natural Language Chat Interface + Interactive Map
```

---

## 🛠️ Tech Stack

- **Platform**: Databricks Free Edition
- **LLM**: Meta Llama 3.3 70B Instruct (via Databricks Foundation Model APIs)
- **Experiment Tracking**: MLFlow
- **Storage**: Delta Lake
- **Visualization**: Folium + Leaflet.js
- **Data**: Virtue Foundation Ghana Dataset (v0.3)

---

## ▶️ How to Run

### Prerequisites
- Databricks account (Free Edition works)
- Ghana dataset uploaded to Databricks catalog

### Steps
1. Upload `Virtue_Foundation_Ghana_v0_3_-_Sheet1.csv` to Databricks
2. Import all notebooks into your Databricks workspace
3. Run notebooks in order: `01` → `02` → `03` → `04` → `05` → `06`
4. Each notebook builds on the previous Delta tables

### No API keys needed!
All LLM calls use Databricks' built-in Foundation Model APIs.

---

## 📈 Evaluation Criteria Coverage

| Criteria | Weight | What We Built |
|---|---|---|
| Technical Accuracy | 35% | IDP agent with Pydantic validation + anomaly detection |
| IDP Innovation | 30% | Multi-step LLM extraction with citations + MLFlow tracing |
| Social Impact | 25% | 758 medical deserts identified, regional breakdown, resource recommendations |
| User Experience | 10% | Natural language chat interface for non-technical NGO planners |

---

## 👥 Team
Built during the Databricks x Accenture Hackathon for the Virtue Foundation Track.

## 📄 License
MIT License
