Role: you are a resume writer and my Guide
Aim: You have to help me format my currect raw and not so self explaining projects on my protfolio and resuem to detailed implementation doc which will be only for me to understand and freshen up what i did using what tech stack and what was impacted
Instruction: 
1. you will first extract the main project info from my given info then create the table as company, project name, tech stack. After confirming the no of project and no of doc to create which will be detailed and md files
2. Before writing md file will finalize the md doc template
3. Then will select one project and you have to question me about it like interviewer so that i can think and get more info and if i say don't know or i am confused then will keep that part empty of that time but in doc will make sure to complete the project fully as the one.
4. Will do the step 3 for each project one by one
guadrails: 
1. Don't assume anything ask me question regarding it and then confirm as per my answer
2. 
---

AI Engineer | IKS Health | SEP 2025 – Present
Designed and developed scalable FastAPI-based REST APIs for authentication, RBAC, and secure healthcare workflows, enabling integration with internal services and external platforms.

Contributed to a HIPAA-compliant, containerized Agentic AI framework for automated prior authorization across multiple payer portals, integrating AI-driven workflows with enterprise applications.

Engineered event-driven pipelines using Google Pub/Sub for asynchronous batch patient processing, supporting scalable healthcare workflow automation.

Integrated Google Vertex AI (LLMs) by configuring GCP service account access and securely connecting the application to Vertex AI models for intelligent browser automation and workflow reasoning.

Implemented Human-in-the-Loop (HITL) and MFA (OTP) workflows using n8n, PostgreSQL, and Redis within a distributed multi-agent system to support reliable AI-driven automation.

Contributed to scalable multi-portal automation infrastructure with secure credential management, supporting enterprise healthcare workflows.

Analyst (AI/ML Developer) | Capgemini | 2024 – SEP 2025

Monitored and refined a time-series forecasting model using hana_ml through March 2025 to forecast electricity usage, supporting cost-saving decisions and CO₂ reduction through optimized resource planning.

Built an Agentic AI prototype to streamline SSP–Hub workflows for rare medication access, developing multi-agent systems using Semantic Kernel, React, and Flask to automate eligibility and financial-aid monitoring, with hands-on experience in Azure and GitHub Copilot.

Associate (Python Developer) | Capgemini | July 2022 – 2023
Built a machine learning model to predict patient no-shows, improving scheduling efficiency; developed Streamlit dashboards to rank bench employees, enhancing visibility and resource utilization.
Led a hackathon team to develop a one-click data-cleaning application, advanced to the second round, and subsequently transitioned into a GenAI Developer role on a project.
Developed hands-on RAG pipelines using vector databases and embedding workflows to support Generative AI automation and business insights.

Associate (Gen AI Developer) | Capgemini | 2023 – 2024
Forecasted hourly electricity usage using hana_ml, supporting cost-saving decisions and CO₂ reduction through optimized resource deployment across building locations.
Prototyped a Generative AI invoice processing system on AWS to process multilingual invoices and detect fraud; demonstrated the solution to clients to showcase automation and financial accuracy.
Built a RAG-based AI chatbot using document retrieval and vector search to assist SAP HANA developers with data migration; performed intensive prompt engineering over 3 months to improve response quality, relevance, and consistency, leading to successful internal adoption and client interest during beta testing.
Developed a natural language-to-SQL tool that automated query generation from metadata and visualized results using React and Google Charts, streamlining data analysis for non-technical users.

text from my portfolio
Healthcare Agentic AI Prior Authorization Framework
Contributed to a containerized multi-agent automation framework for healthcare prior authorization. Built FastAPI services, implemented event-driven pipelines using Google Pub/Sub, integrated Vertex AI (LLMs) for intelligent browser automation, and developed HITL & MFA workflows using n8n, PostgreSQL, and Redis.

FastAPIVertex AIGoogle Pub/SubPostgreSQLRedisn8nDockerLLMs

Natural Language to SQL Intelligence Tool

Developed a system that converts natural language queries into SQL statements and visualizes insights using React and Google Charts, enabling non-technical users to perform data analysis efficiently.

PythonSQLReact.jsGoogle ChartsLLM Integration

RAG-Based Enterprise Chatbot
Built a Retrieval-Augmented Generation (RAG) chatbot to assist developers with data migration and internal workflows, leveraging vector databases and LLM orchestration.
LangChainSemantic KernelFAISSReact.jsFlaskRAG

Gen AI Invoice Processing & Fraud Detection System
Prototyped a multilingual invoice automation system using LLM pipelines to extract structured data and detect anomalies, improving financial processing accuracy.
AWSLLMsRAGVector DatabasesPython

Patient No-Show Prediction Model
Built a machine learning model to predict patient no-shows, improving scheduling efficiency. Integrated insights into interactive dashboards for data-driven decision making.
PythonMachine LearningStreamlitData Analysis

-------------------------

# [Project Name]

**Company:** ...
**Role:** ...
**Timeframe:** ...
**Team Size:** ...
**My Position in Team:** ...

**One-line Summary:** ...

---

## 1. Problem / Why It Existed

### Business Problem
...

### Technical Problem
...

### Who Used It
...

### Why This Solution Was Needed
...

---

## 2. My Role & Ownership

### What I Personally Built
...

### What I Contributed To
...

### What Other Team Members Owned
...

---

## 3. System / Product Overview

### What the System Does
...

### End-to-End Flow
...

---

## 4. Architecture / How It Worked

### High-Level Architecture
...

### Step-by-Step Flow
1. ...
2. ...
3. ...

### Component Responsibilities
...

---

## 5. Tech Stack

| Technology | Where It Was Used | Why It Was Used |
|---|---|---|
| ... | ... | ... |

---

## 6. Implementation Details

### Backend
...

### Frontend
...

### AI / ML
...

### Database / Storage
...

### APIs / Integrations
...

### Infrastructure / Deployment
...

---

## 7. Key Technical Decisions

### Decision 1
**What:** ...
**Why:** ...
**Alternative:** ...
**Trade-off:** ...

---

## 8. Challenges & How I Solved Them

### Challenge 1
**Problem:** ...
**Root Cause:** ...
**Solution:** ...
**Result:** ...

---

## 9. Testing / Validation

...

---

## 10. Production / Deployment

...

---

## 11. Impact / Results

### Technical Impact
...

### Business Impact
...

### Metrics
...

---

## 12. Interview Talking Points

### 1. ...
### 2. ...
### 3. ...

---

## 13. Likely Interview Questions

### Q1. ...
**Answer:** ...

### Q2. ...
**Answer:** ...

---

## 14. Open Questions / Gaps

- [ ] ...
- [ ] ...

----------
Ready for #2 — One-Click Data Cleaning App (hackathon) whenever you want to start. Round 1 questions for that one:

What kind of "dirty" data was it built to clean, and what format was input/output (CSV, Excel, etc.)?
It was the streamlit app and as the team leader i decided the ui to be the streamlit and the backend the python code as i learned about the streamlit in the project of building the dashboard for the bench people 
the category choosen for the hackathon was the data engineering so i thought to create the interactive way to do the basic eda and data cleaning.
data input was (csv and excel file) [as a dummy data we have taken data from kaggle and testd the application fro the 1 lakh + rows csv file] and the output was the clean csv file and the cleaning can be done by the button and the ui itself

What was your specific contribution as team lead — did you code the cleaning logic yourself, the UI, or mainly coordinate?
the section was 4 as far as i remember the first tab where user can upload the  file and click on the analyze then on the sidebar user can see the the data info such as no of rows, columns, and datatype of the columns and missing or null values in that column and if the coulumn is int then its mean, median, mode too, then thre war tab to work with the null value wehre user can select coulumn and then select the option if user want to drop the null or impute with mean , median , or mode or any othere value, then the functionality to reaname the column if want from ui itself, then tab to work with the date and time column where user can crate new column if want like day, date, time or weekday on taht date i didn't remrmber more but what ever data cleaning I learned in that no show project i tried to implement that and as includeing me we were 5 member so i have given each one of them to work on the functionality of each tab or sidebar and i was stiching the code so taht it shourl work together
You mentioned it advanced to round 2 and led to a GenAI Developer role transition — was the judging criteria or feedback something you remember, and roughly how big was the team?
Our project got select for the round 2 and it was interview round where there was one directore level persone was questioning aobut it and i got feed back that the application and idea is good but we don't get data from csv or excel but we get it from data lake or warehouses so you can think how we can use that data otherwise good try and he asked that why you choose this tech stack and i remember i said becalue recently i worked on one project of it and this streamlit is new python library so becacaus of thsi project we got to learn it more. and then after a week or so i got a call from some manager and they have taked my interview for python language and added me to the team where they building the RAG based chatbot or the sap developers who worked in data migration

---------

| # | Company    | Project Name                                                    | Detailed MD | Known Tech Stack                                                                             |
| - | ---------- | --------------------------------------------------------------- | ----------- | -------------------------------------------------------------------------------------------- |
| 1 | Capgemini  | **Patient No-Show Prediction**                                  | ✅           | Python, Machine Learning                                                                     |
| 2 | Capgemini  | **Bench Employee Ranking Dashboard**                            | ✅           | Python, Streamlit, Data Analysis                                                             |
| 3 | Capgemini  | **One-Click Data Cleaning Application**                         | ✅           | TBD                                                                                          |
| 4 | Capgemini  | **Electricity Usage Forecasting**                               | ✅           | hana_ml, Time-Series Forecasting                                                             |
| 5 | Capgemini  | **GenAI Invoice Processing & Fraud Detection System**           | ✅           | AWS, LLMs, Python                                                                            |
| 6 | Capgemini  | **RAG-Based Enterprise Chatbot / SAP HANA Migration Assistant** | ✅           | RAG, Vector DB, FAISS, LangChain, Semantic Kernel, React, Flask                              |
| 7 | Capgemini  | **Natural Language-to-SQL Intelligence Tool**                   | ✅           | Python, SQL, LLM, React, Google Charts                                                       |
| 8 | Capgemini  | **SSP–Hub Rare Medication Access Agentic AI**                   | ❌           | Semantic Kernel, React, Flask, Azure                                                         |
| 9 | IKS Health | **Healthcare Agentic AI Prior Authorization Framework**         | ✅           | FastAPI, Vertex AI, Google Pub/Sub, PostgreSQL, Redis, n8n, Docker, LLMs, Browser Automation |

------- 

# Resume content
---

# Professional Summary

AI/ML Engineer with experience at Capgemini across machine learning, Generative AI, RAG, NLP, and data-driven automation. Built and contributed to projects spanning healthcare prediction, time-series forecasting, enterprise RAG, natural-language-to-SQL, and internal automation, using Python, Scikit-learn, Streamlit, LangChain, React, Flask, and SAP HANA ML. Experienced in taking AI/ML solutions from data preparation and experimentation through evaluation, prototyping, and business-oriented presentation.

At IKS Health, contributed to a containerized Agentic AI framework for healthcare prior-authorization automation, developing FastAPI services and integrating Google Vertex AI, Google Pub/Sub, PostgreSQL, Redis, n8n, Docker, and browser automation. Worked on event-driven healthcare workflows, Human-in-the-Loop and MFA/OTP automation, and secure integration of AI services to support scalable automation across payer portals.

# Projects

## 1. Patient No-Show Prediction

Built a machine learning classification solution to predict patient appointment no-shows using a Kaggle healthcare dataset as part of an internal ML learning initiative at Capgemini. Led a ~6-member team, coordinated model experimentation, and implemented data cleaning, exploratory data analysis, categorical encoding, and date-based feature engineering including appointment waiting time. Compared multiple classification approaches including tree-based and boosting models, with CatBoost selected based on comparative model performance, while consolidating the final Jupyter Notebook and presentation for the project mentor. **Tech:** Python, Pandas, NumPy, Scikit-learn, XGBoost, CatBoost, Matplotlib, Seaborn.

## 2. Bench Employee Ranking Dashboard

Developed an interactive Streamlit dashboard to analyze and rank bench employees, providing improved visibility into employee profiles and supporting more data-driven resource utilization decisions. Processed and analyzed employee-related data using Python and presented the resulting rankings through an interactive dashboard, transforming raw employee information into a more accessible view for internal decision-making. **Tech:** Python, Streamlit, Data Analysis.

## 3. One-Click Data Cleaning Application — Hackathon

Led a 5-member team during an internal Microsoft-organized hackathon to build a one-click data-cleaning application aimed at simplifying repetitive data preparation tasks. Contributed to the development of the solution while coordinating the team and integrating the team's work into a demonstrable prototype, which advanced to the second round of the hackathon and contributed to my transition toward a Generative AI development role. **Tech:** Python, Generative AI/AI tooling, Microsoft Semantic Kernel (where applicable to the prototype).

## 4. Electricity Usage Forecasting

Worked on a time-series forecasting solution to predict hourly electricity usage across building locations, using SAP HANA ML (`hana_ml`) to support more informed resource planning. Monitored and refined the forecasting model through March 2025, analyzing prediction behavior and model performance to support cost-conscious resource deployment and potential CO₂ reduction through optimized energy usage. **Tech:** Python, SAP HANA ML (`hana_ml`), Time-Series Forecasting, Machine Learning.

## 5. RAG-Based Enterprise Chatbot / SAP HANA Migration Assistant

Built a Retrieval-Augmented Generation (RAG) chatbot to assist SAP HANA developers with data migration and internal technical workflows by combining document retrieval, vector search, and LLM-based response generation. Developed and refined the retrieval and prompting workflow through intensive prompt engineering over approximately three months to improve response relevance, consistency, and usefulness, contributing to successful internal adoption and client interest during beta testing. **Tech:** Python, RAG, Vector Databases, FAISS, LangChain, Semantic Kernel, React.js, Flask, LLMs.

## 6. Natural Language-to-SQL Intelligence Tool

Developed a natural-language-to-SQL solution that enabled non-technical users to query data using plain-language questions instead of manually writing SQL. Implemented the workflow to interpret natural-language requests, generate SQL using metadata/context, execute the resulting queries, and visualize the returned data through an interactive React interface with Google Charts, streamlining data exploration and analysis. **Tech:** Python, SQL, LLM Integration, React.js, Google Charts.

## 7. Healthcare Agentic AI Prior Authorization Framework

Contributed to a containerized multi-agent healthcare automation framework designed to streamline prior-authorization workflows across payer portals. Developed FastAPI-based services, integrated Google Vertex AI for LLM-powered workflow reasoning and browser automation, and implemented event-driven processing with Google Pub/Sub; also contributed to Human-in-the-Loop and MFA/OTP workflows using n8n, PostgreSQL, and Redis to support reliable and scalable healthcare automation. **Tech:** Python, FastAPI, Google Vertex AI, LLMs, Google Pub/Sub, Playwright/Browser Automation, PostgreSQL, Redis, n8n, Docker, Kubernetes/GKE.
