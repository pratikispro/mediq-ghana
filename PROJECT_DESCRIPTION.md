# MedIQ — Project Description

## What We Built

MedIQ is an agentic AI system that transforms unstructured healthcare facility data into actionable intelligence for NGO planners. Built for the Virtue Foundation, it analyzes real Ghana healthcare data to identify where care is missing and where data is suspicious.

## The Problem

The Virtue Foundation has data on hundreds of Ghana healthcare facilities — but most of it is messy, incomplete, or unverified free-form text. Without an intelligent system to parse and reason over this data, critical decisions about where to deploy doctors and resources are made blindly.

## Our Solution

We built a 6-notebook pipeline on Databricks:

**1. Intelligent Document Parsing (IDP) Agent**
Uses Meta Llama 3.3 70B to extract structured medical facts (procedures, equipment, capabilities) from free-form text fields. Every extracted fact is validated against the Virtue Foundation's Pydantic schema.

**2. Medical Desert Detection**
Our gap analyzer scores every facility on a 0-100 desert scale based on missing procedures, equipment, and capabilities. We identified 758 out of 1,067 facilities (71%) as medical deserts — including entire regions like Western Ghana where 100% of facilities are severely under-resourced.

**3. Anomaly Detection**
We flagged 169 facilities with suspicious or contradictory claims — hospitals claiming ICU care with no equipment, facilities claiming surgery with no theater. These are prioritized for field verification.

**4. Natural Language Planning Interface**
NGO planners can ask questions in plain English: "Which regions need the most urgent help?" or "Where should we deploy an emergency surgery team?" The agent responds with specific facility names, regions, and concrete action recommendations.

**5. Interactive Map**
A visual map of Ghana showing medical deserts (red), suspicious facilities (orange), and adequate facilities (green) — making the crisis immediately visible to decision makers.

**6. Row-Level Citations with MLFlow Tracing**
Every extracted fact includes a citation pointing to the exact source field. Every reasoning step is logged in MLFlow, providing full transparency into how the agent reached its conclusions.

## Impact

- 758 medical deserts identified across Ghana
- 169 anomalous facilities flagged for investigation  
- Real-time Q&A for NGO resource planning
- Full audit trail via MLFlow experiment tracking
- Directly addresses the Virtue Foundation's June 7th deployment goal

## Why It Matters

Every data point we extracted represents a patient who could receive care sooner. By automating understanding from medical notes, MedIQ creates the intelligence layer that transforms scarcity into coordinated action.
