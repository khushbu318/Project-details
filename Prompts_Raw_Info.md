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
**Role / Timeframe:** ...
**One-line summary:** ...

## Problem / Why it existed
(what business/user problem this solved)

## My Role & Ownership
(what specifically I did vs. team)

## Architecture / How it worked
(flow of the system, step by step)

## Tech Stack
(with a short "why this tool" note per major piece)

## Key Technical Decisions
(tricky choices, trade-offs made)

## Challenges & How I Solved Them
## Impact / Results
(metrics if any, qualitative outcomes)

## Interview Talking Points
(the 2-3 things I'd highlight if asked about this in an interview)

## Open Questions / Gaps
(anything I couldn't recall — flagged, not faked)
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
