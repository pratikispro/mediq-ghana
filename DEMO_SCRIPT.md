# MedIQ — 5 Minute Demo Script

## Opening (30 seconds)
"By 2030, the world will face a shortage of 10 million healthcare workers. 
But the real problem isn't shortage — it's coordination. 
Skilled doctors exist. Hospitals exist. But nobody knows where care is truly missing.
We built MedIQ to solve that."

## Show the Data Problem (30 seconds)
- Open Databricks catalog
- Show the raw Ghana dataset: 995 facilities, messy free-form text
- Point out the procedure/equipment columns: mostly empty or unstructured
- "This is the data the Virtue Foundation has. It's real. It's messy. And right now, nobody can reason over it."

## Show the IDP Agent (60 seconds)
- Open Notebook 02_IDP_Agent
- Show the system prompt and Pydantic schema
- Run a single facility through the agent live
- Show extracted procedures, equipment, capabilities
- "In seconds, our agent extracted structured medical facts from unstructured text — 
  and did this for all 995 facilities."

## Show the Gap Analysis (60 seconds)
- Open Notebook 03_Gap_Analyzer
- Show the desert score output
- "758 out of 1,067 facilities — 71% — are medical deserts."
- Show the anomaly detection output
- "Saint John of God Hospital claims ICU care — but has no equipment listed. 
  Our agent flagged this automatically."

## Show the Map (45 seconds)
- Open Notebook 05_Map_Visualization
- Show the interactive dark map with red/orange/green dots
- Zoom into Western Region — all red
- "Every red dot is a community without adequate healthcare. 
  This map didn't exist before today."

## Show the Chat Interface (45 seconds)
- Open Notebook 04_Chat_Interface
- Type: "Where should we deploy an emergency surgery team?"
- Show the agent's response with specific facility names and regions
- "Any NGO planner — no technical skills needed — can now get actionable 
  intelligence in plain English."

## Show Citations (30 seconds)
- Open Notebook 06_Citations
- Show a citation report with reasoning steps
- "Every fact is traceable. Every decision is auditable. 
  This is AI that NGOs can trust."

## Closing (30 seconds)
"MedIQ processed 995 real Ghana facilities, identified 758 medical deserts,
flagged 169 anomalies, and built a planning tool any NGO can use — 
all on Databricks, all with no external API keys.

The Virtue Foundation ships their agent June 7th. 
MedIQ is ready to be that agent."
