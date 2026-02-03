# CareerAtlas
*A Digital Twin–Driven Skill Alignment and Career Intelligence Platform*

> TL;DR — CareerAtlas quantifies how well university curricula align with real-world technology skill demand in Turkey using NLP, Machine Learning, Knowledge Graphs, Explainable AI, and Digital Twin modeling.
 
CareerAtlas

A Digital Twin–Driven Skill Alignment and Career Intelligence Platform

CareerAtlas is a data-driven career intelligence system designed to analyze the alignment between labor market skill demand and university curriculum supply in the Turkish technology ecosystem.
The project combines Natural Language Processing (NLP), Machine Learning, Knowledge Graphs, Explainable AI (XAI), and Digital Twin modeling to support curriculum analysis, skill gap detection, and personalized career guidance.

This repository contains the research-grade implementation of the system described in the academic study:

“Analysis of Skill Alignment Between the Turkish Technology Sector and University Curricula Through a Digital Twin Approach: An Explainable AI and Agent-Based Career Recommendation Model”

🎯 Project Objectives

Quantitatively measure skill mismatches between industry demand and academic curricula

Model labor market and education systems as interacting digital twins

Provide explainable, data-driven career and learning pathway recommendations

Support policy-making, curriculum design, and student career planning with interpretable metrics

🧠 Core Contributions

This project goes beyond a classical job recommender system by introducing:

Education–Labor Market Alignment Index

Heterogeneous Knowledge Graph (Role–Skill–Course–University)

Skill Gap Metrics (Demand vs. Supply)

Digital Twin–based “What-if” Curriculum Simulations

Explainable AI–assisted Career Recommendations

🏗️ System Architecture

The system follows a multi-layer analytical pipeline:

1️⃣ Data Acquisition

~5,300 Turkish technology job postings (multi-source)

Course descriptions from 30 universities / 209 core engineering courses

Optional CV/PDF inputs for micro-level analysis

2️⃣ Text Processing & Normalization

Turkish NLP preprocessing

Domain-specific normalization
(k8s → kubernetes, sklearn → scikit-learn, power bi → powerbi, etc.)

Unified technical skill vocabulary

3️⃣ Skill Extraction (Hybrid Approach)

Dictionary-based matching

NER-assisted skill detection

Binary and weighted skill representations

4️⃣ Role Classification

TF-IDF + skill vectors

Supervised models (LogReg, XGBoost)

Roles such as:

Data Scientist

Data Engineer

Software Engineer

DevOps / MLOps

Best performance:
Hybrid (Text + Skill) XGBoost

~90% Accuracy / F1-score

5️⃣ Skill Gap Analysis

For each skill i:

𝐺
𝑖
=
𝐷
𝑖
−
𝑆
𝑖
G
i
	​

=D
i
	​

−S
i
	​


Where:

𝐷
𝑖
D
i
	​

: Industry demand (job postings)

𝑆
𝑖
S
i
	​

: Academic supply (curricula)

This enables quantitative identification of underrepresented skills.

🕸️ Knowledge Graph Modeling

A heterogeneous knowledge graph is constructed with four node types:

Role

Skill

Course

University

Edges represent:

Role → Skill (demand intensity)

Course → Skill (coverage level)

University → Course (structural mapping)

This structure enables:

Traceable skill gaps

Curriculum-level diagnostics

Explainable recommendations

🔍 Explainable AI (XAI)

To avoid black-box decision-making:

LIME is used to explain role predictions

Users can see:

Why a role was suggested

Which skills influenced the decision

Missing vs. matched competencies

This is critical for:

Educational decision support

Ethical AI deployment

User trust and transparency

🧪 Digital Twin & Scenario Simulation

The education system and labor market are modeled as asymmetric digital twins:

Labor Market → fast-evolving demand system

Universities → slow-changing supply system

Using this framework, the system supports:

Curriculum change simulations

“What-if” analyses

Quantitative evaluation of curriculum updates

📈 Results show that targeted course updates can improve alignment scores by 8–14% per role.

🌐 Prototype & Deployment

A web-based prototype (Streamlit) demonstrates:

CV → role & skill inference

Skill gap visualization

Personalized learning recommendations

The UI is intentionally treated as a demonstration layer, not the core contribution.
The primary value lies in the analytical pipeline and models.

🛠️ Technologies Used

Python

NLP (TF-IDF, NER)

Machine Learning (Scikit-learn, XGBoost)

Knowledge Graphs

Explainable AI (LIME)

Agent-based & Digital Twin modeling

Streamlit (prototype layer)

📊 Key Findings

Only 7 of the top 20 industry-demanded skills are consistently covered in curricula

Major gaps identified in:

Cloud Computing

DevOps

Data Engineering

BI & Visualization Tools

Curriculum changes can be quantitatively optimized before implementation

🔮 Future Work

Graph Neural Networks (GNNs) for skill propagation

Cross-disciplinary curriculum expansion

National-scale education–labor alignment platform

Policy-level decision dashboards
