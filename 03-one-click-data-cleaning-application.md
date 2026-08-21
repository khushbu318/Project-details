# One-Click Data Cleaning Application

**Company:** Capgemini  
**Role:** Associate (Python Developer)  
**Timeframe:** 2022–2023 (internal hackathon; exact date not remembered)  
**Team Size:** 5  
**My Position in Team:** Team Lead / Technical Integration Lead

**One-line Summary:** Built a Streamlit-based interactive data cleaning and EDA prototype that accepted CSV/XLSX files, profiled datasets, provided common cleaning and date/time operations through a UI, and exported the cleaned data as CSV.

---

## 1. Problem / Why It Existed

### Business Problem

The project was created for an internal **Data Engineering hackathon**. The goal was to make basic exploratory data analysis (EDA) and common data-cleaning activities more interactive and accessible through a single application.

Instead of requiring users to write or run separate Python code for every operation, the team created a UI where a user could upload a dataset, inspect its characteristics, perform selected cleaning operations, and download the resulting cleaned data.

### Technical Problem

The application aimed to simplify common data-preparation tasks such as:

- Inspecting dataset structure and quality.
- Identifying missing values.
- Understanding column data types and basic statistics.
- Performing common null-value operations.
- Renaming columns.
- Creating useful date/time-derived columns.
- Exporting the resulting cleaned dataset.

### Who Used It

The application was a **hackathon prototype** for demonstration and evaluation. It was not deployed as a production internal tool.

### Why This Solution Was Needed

I chose Streamlit for the UI because I had recently learned it while working on the Bench Employee Ranking Dashboard. The hackathon provided an opportunity to apply and learn the technology further while building an interactive Python-based data-engineering solution.

---

## 2. My Role & Ownership

### What I Personally Built

I personally implemented:

- CSV and XLSX file upload/reading.
- Loading uploaded files into pandas DataFrames.
- Initial data preview.
- EDA/data profiling.
- Sidebar displaying dataset information.
- Most of the Streamlit UI/layout.
- Final cleaned-data display/export.
- CSV download.
- Integration of the different team members' functionality.
- Finding suitable Kaggle test data.
- Manual application testing.

My EDA/profile functionality included:

- Number of rows.
- Number of columns.
- Column names.
- Data types.
- Missing/null values per column.
- Unique/distinct values.
- Minimum and maximum values.
- Standard deviation.
- Mean, median, and mode where applicable.
- Duplicate information, including a remembered check/count when duplicates exceeded 10.
- Preview of the data.

### What I Contributed To

As team lead, I:

- Divided the application into feature areas/tabs.
- Assigned functionality to the other four team members.
- Explained the overall project idea and application structure.
- Reviewed teammates' code before integration.
- Integrated their implementations into the main Streamlit application.
- Helped a teammate implement the date/time functionality.
- Organized the presentation/PPT work among the team.
- Acted as the team's lead representative during the second-round interview, after the team mutually decided that I would take the lead role.

### What Other Team Members Owned

Team members primarily owned:

- Missing-value cleaning functionality.
- Column-renaming functionality.
- Date/time and derived-column functionality.

I assisted with the date/time functionality and integrated the team's implementations.

---

## 3. System / Product Overview

### What the System Does

The One-Click Data Cleaning Application was a Streamlit application for interactive data inspection and common cleaning operations.

The user could:

1. Upload a CSV or XLSX file.
2. Analyze and preview the dataset.
3. View dataset information from the sidebar.
4. Work with missing values.
5. Rename columns.
6. Create new columns from date/time data.
7. Review the final cleaned dataset.
8. Export the cleaned dataset as CSV.

### End-to-End Flow

**Upload → Analyze → Profile/EDA → Clean → Transform → Review Final Data → Export CSV**

The working dataset was maintained as a pandas DataFrame and persisted between tabs using Streamlit session state.

---

## 4. Architecture / How It Worked

### High-Level Architecture

The application had a simple Python-based architecture:

- **UI:** Streamlit
- **Data processing:** Python and pandas
- **Application state:** Streamlit session state
- **Input:** CSV and XLSX files
- **Output:** Cleaned CSV file
- **Execution:** Local machine

The project was a hackathon prototype and was not deployed to a production server.

### Step-by-Step Flow

1. The user uploaded a CSV or XLSX file through the Streamlit upload widget.
2. The application used pandas to read the file.
3. The uploaded data was loaded into a pandas DataFrame.
4. The application displayed an initial preview.
5. The DataFrame was stored in Streamlit session state.
6. The sidebar displayed information about the dataset.
7. Individual tabs provided separate cleaning/transformation functionality.
8. Cleaning operations modified the DataFrame.
9. The modified DataFrame remained available across tabs through session state.
10. The final tab displayed information about the cleaned dataset.
11. The final DataFrame was exported as CSV and made available for download.

### Component Responsibilities

**File Upload / Ingestion**
- Accepted CSV and `.xlsx` files.
- Used pandas `read_csv()` and `read_excel()` to read uploaded files.
- Loaded the result into a DataFrame.
- Displayed a preview.

**EDA / Profiling**
- Displayed basic structural and statistical information.
- Provided dataset information in the sidebar.

**Missing Value Handling**
- Showed null counts by column.
- Allowed users to choose how to handle missing values.

**Column Renaming**
- Allowed one or multiple columns to be renamed.
- Checked that a new name would not create a duplicate column name.

**Date/Time Transformation**
- Allowed users to select an existing date/time column and create a new column based on a selected transformation.
- Remembered transformations included date, time, day, weekday, month, year, hour, minute, and converting a column to datetime.

**Export**
- Displayed the final cleaned dataset.
- Exported the DataFrame as CSV.

---

## 5. Tech Stack

| Technology | Where It Was Used | Why It Was Used |
|---|---|---|
| Python | Application/backend logic | Main programming language for data processing |
| Streamlit | User interface | Build an interactive Python-based UI quickly |
| Pandas | Data ingestion, EDA, cleaning and transformation | DataFrame-based data manipulation |
| CSV | Input/output format | Common tabular data format |
| XLSX | Input format | Support for Excel datasets |
| GitHub | Source-code sharing | Share and collaborate on the hackathon code |
| Kaggle datasets | Test data | Obtain sample datasets for testing |

---

## 6. Implementation Details

### Backend

The backend logic was implemented in Python.

Pandas DataFrames were the primary data structure. Uploaded CSV and XLSX files were read into DataFrames, and the DataFrame was maintained in Streamlit session state so different tabs could operate on the same dataset.

Cleaning operations modified the existing DataFrame.

### Frontend

The UI was implemented primarily by me using Streamlit.

The application used a feature-oriented tab structure. The main workflow was approximately:

- Upload / Analyze
- Missing-value replacement
- Rename columns
- Create new columns / date-time operations
- Final cleaned data / export

Dataset information was displayed in the sidebar so users could continue seeing it while working in other tabs.

### AI / ML

No AI or machine-learning component was used.

This was a **Data Engineering/data-processing hackathon project** focused on interactive EDA and data cleaning.

### Database / Storage

No database or external persistent storage was used.

The working dataset was held as a pandas DataFrame in Streamlit session state during application use.

### APIs / Integrations

No external APIs or enterprise data integrations were implemented.

The application accepted files uploaded through the Streamlit interface.

### Infrastructure / Deployment

The application ran locally on the team's machine/environment.

It was not deployed to Streamlit Cloud, a company server, or another production environment.

The hackathon submission consisted of the project code repository and presentation/PPT.

---

## 7. Key Technical Decisions

### Decision 1
**What:** Use Streamlit for the user interface.

**Why:** I had recently worked with Streamlit while building the Bench Employee Ranking Dashboard. Streamlit was also a new Python library for me, so the hackathon provided an opportunity to learn it further while building an interactive application.

**Alternative:** A different web UI/framework could have been used.

**Trade-off:** Streamlit allowed rapid development in Python, but the resulting application was primarily suited to a prototype-style workflow rather than a production enterprise application.

### Decision 2
**What:** Use pandas DataFrames as the central data representation.

**Why:** The application was focused on tabular data analysis and cleaning, and pandas provided the required DataFrame operations.

**Alternative:** Another data-processing framework could have been used.

**Trade-off:** Pandas made the prototype straightforward to build, while larger datasets exposed performance limitations during testing.

### Decision 3
**What:** Keep the working DataFrame in Streamlit session state.

**Why:** Different tabs needed to operate on the same progressively modified dataset.

**Alternative:** Reload or reconstruct the dataset between operations.

**Trade-off:** Session state made the multi-tab workflow straightforward, but it kept the working dataset within the application session rather than providing persistent storage.

---

## 8. Challenges & How I Solved Them

### Challenge 1
**Problem:** The application needed multiple cleaning features while allowing users to work with the same dataset.

**Root Cause:** Each feature was represented separately in the UI, but all operations needed to affect the same underlying data.

**Solution:** The team used a pandas DataFrame stored in Streamlit session state. I integrated the individual feature implementations so that they worked together on the shared DataFrame.

**Result:** Users could move through the feature tabs while retaining changes made to the dataset.

### Challenge 2
**Problem:** The application became noticeably slower with a large dataset.

**Root Cause:** The prototype was tested with a Kaggle stock-price CSV containing more than 100,000 rows.

**Solution:** No formal performance optimization was implemented during the hackathon. The large dataset was primarily used to test the application's ability to handle a relatively high row count.

**Result:** The application successfully loaded the dataset, but I observed approximately **20–30 seconds of response time for some button clicks or data changes**.

This was an observed prototype limitation, not a formal performance benchmark.

### Challenge 3
**Problem:** The hackathon judges pointed out that enterprise data is often obtained from data lakes or data warehouses rather than CSV/Excel files.

**Root Cause:** The prototype was designed around file-based input.

**Solution:** During the Round 2 discussion, I acknowledged the limitation and was asked to think about how the application could work with data from enterprise data sources.

**Result:** The feedback identified a clear direction for making the concept more relevant to enterprise data-engineering environments.

---

## 9. Testing / Validation

Testing was primarily manual.

### Test Data

The team used dummy data obtained from Kaggle. One important test used a **stock-price CSV containing more than 100,000 rows**.

### Testing Performed

- Uploaded and read CSV data.
- Tested the application with a large dataset.
- Manually interacted with the Streamlit UI.
- Checked the application's ability to process and display the data.
- Used the application during development to verify the overall workflow.

### Testing Limitations

I do not remember performing:

- Formal automated tests.
- A systematic comparison against expected output.
- A formal performance benchmark.
- Comprehensive testing of every cleaning feature against the 100K+ dataset.

---

## 10. Production / Deployment

This project remained a **hackathon prototype**.

- It ran locally.
- It was not deployed to a company server.
- It was not deployed to Streamlit Cloud.
- It was not converted into a production internal tool.
- The project code was shared through GitHub.
- The hackathon submission included the code repository and PPT.

---

## 11. Impact / Results

### Technical Impact

The project demonstrated that common EDA and data-cleaning operations could be combined into a single interactive Python/Streamlit workflow.

It also gave me practical experience with:

- Streamlit application development.
- Pandas-based data processing.
- Session-state management.
- Integrating multiple contributors' Python code.
- Building a data-processing UI.
- Working with larger tabular datasets.

### Business Impact

The project was a hackathon prototype rather than a production system, so there are no verified production adoption or business-impact metrics.

The project was **selected for the second round** of the hackathon process.

### Metrics

Known/verified figures:

- **Team:** 5 members.
- **Test dataset:** 100K+ rows.
- **Observed response time:** approximately 20–30 seconds for some button clicks/data changes on the large test dataset.
- **Hackathon result:** Selected for Round 2.

No other business metrics are currently verified.

---

## 12. Resume / Portfolio Summary

### Short Summary

Led a 5-member internal hackathon team to build a Streamlit-based one-click data cleaning prototype using Python and pandas. Personally developed the file-ingestion, EDA/profile, Streamlit UI, session-state integration, and CSV export functionality, while integrating teammates' cleaning and transformation modules.

### Resume-Oriented Bullets

- Led a 5-member team in building a **Streamlit-based interactive data cleaning and EDA application** for an internal Data Engineering hackathon.
- Developed CSV/XLSX ingestion, pandas-based data profiling, Streamlit UI, session-state data flow, and cleaned-CSV export functionality.
- Integrated teammate-built modules for missing-value handling, column renaming, and date/time transformations into a unified application.
- Tested the prototype with a **100K+ row Kaggle stock-price dataset**, identifying approximately 20–30 second response times for some interactions.
- Advanced the project to the **Round 2 evaluation**, where enterprise data-source considerations such as data lakes and warehouses were discussed.

---

## 13. Interview Talking Points

### 1. Why did you choose Streamlit?

I had recently worked with Streamlit on the Bench Employee Ranking Dashboard. I wanted to use that knowledge to build an interactive data-cleaning application and also learn the framework further.

### 2. What was your personal contribution?

I was the technical team lead. I personally built the file-upload/reading functionality, EDA and profiling, sidebar information, most of the Streamlit UI, final CSV export, and integration of the team's modules. Other members owned specific cleaning features.

### 3. How did data move through the application?

The uploaded CSV/XLSX file was read into a pandas DataFrame. The DataFrame was stored in Streamlit session state and accessed by the different feature tabs. Cleaning operations modified the DataFrame, and the final DataFrame was exported as CSV.

### 4. Why did you use session state?

The different tabs needed to operate on the same progressively modified DataFrame. Streamlit session state provided a way to preserve that working DataFrame as the user moved through the application.

### 5. What happened when you tested large data?

We tested with a Kaggle stock-price CSV containing more than 100,000 rows. It successfully processed the dataset, but some interactions took approximately 20–30 seconds. We did not perform formal performance optimization during the hackathon.

### 6. Was this a production application?

No. It was an internal hackathon prototype. It ran locally and was submitted through the project repository and presentation.

### 7. What feedback did you receive?

The application and idea were considered good, but a director-level interviewer pointed out that enterprise data is often sourced from data lakes or warehouses rather than CSV/Excel files. The discussion therefore highlighted how the solution could be adapted to enterprise data sources.

### 8. How did you lead the team?

I divided the application into feature areas, assigned each area to a team member, explained the overall application idea and structure, reviewed their code, and integrated the separate implementations into the final Streamlit application. I also organized the presentation and acted as the team's lead representative during the second-round discussion.

### 9. Did you deploy the application?

No. It was a hackathon prototype that ran locally. We submitted the code repository and PPT rather than deploying it as a production application.

### 10. What was your role versus your teammates' roles?

I owned the main UI, file ingestion, EDA/profile functionality, export, and integration. Teammates primarily implemented missing-value handling, column renaming, and date/time functionality. I assisted with the date/time functionality.

---

## 14. Likely Interview Questions

### Q1. Why did you choose Streamlit instead of another framework?
**Answer:** I had recently worked with Streamlit on the Bench Employee Ranking Dashboard, so I already had some familiarity with it. For the hackathon, it allowed us to quickly expose Python-based data-processing functionality through an interactive UI while also helping me learn the framework further.

### Q2. How did you maintain the DataFrame between tabs?
**Answer:** We used Streamlit session state. The uploaded file was converted into a pandas DataFrame and stored in session state. The different tabs accessed and modified that same DataFrame.

### Q3. What did your EDA module provide?
**Answer:** It provided row and column counts, column names, data types, null counts, unique values, min/max, standard deviation, and mean/median/mode where applicable. It also displayed a preview of the data.

### Q4. What cleaning operations did the application support?
**Answer:** It supported null handling through dropping or replacement with mean, median, mode, or a custom value. It also supported column renaming and creating new columns from date/time fields.

### Q5. How did you handle categorical columns?
**Answer:** We did not blindly apply numeric statistics to categorical columns. The application provided information such as unique values to help determine an appropriate treatment.

### Q6. What was the biggest technical limitation?
**Answer:** Performance with larger datasets was one limitation. With a 100K+ row Kaggle stock-price CSV, I observed approximately 20–30 seconds for some button clicks or data changes. The prototype also accepted file-based input rather than connecting directly to enterprise data sources.

### Q7. How would you improve the application if you continued it?
**Answer:** Based on the hackathon feedback, I would first look at integrating enterprise data sources such as data lakes or warehouses rather than relying only on uploaded CSV/Excel files. I would also investigate the causes of the observed large-dataset latency and add more systematic validation and testing.

### Q8. How did you lead the team?
**Answer:** I divided the application into feature areas, assigned each area to a team member, explained the overall application idea and structure, reviewed their code, and integrated the separate implementations into the final Streamlit application. I also organized the presentation and acted as the team's lead representative during the second-round discussion.

### Q9. Did you deploy the application?
**Answer:** No. It was a hackathon prototype that ran locally. We submitted the code repository and PPT rather than deploying it as a production application.

### Q10. What was your role versus your teammates' roles?
**Answer:** I owned the main UI, file ingestion, EDA/profile functionality, export, and integration. Teammates primarily implemented missing-value handling, column renaming, and date/time functionality. I assisted with the date/time functionality.

---

## 15. Open Questions / Gaps

- [ ] Exact hackathon date/month is not currently remembered.
- [ ] Exact project/repository name is not remembered.
- [ ] Exact Streamlit version is unknown.
- [ ] Exact pandas version is unknown.
- [ ] Exact repository/file structure is not remembered.
- [ ] Exact tab names are not remembered.
- [ ] Exact implementation of the duplicate-value threshold/check is not fully remembered.
- [ ] Exact validation behavior beyond duplicate column-name prevention and Streamlit warnings is unknown.
- [ ] Exact file-size limitation, if any, is unknown.
- [ ] Exact Kaggle dataset name is unknown; it is remembered as a stock-price CSV with 100K+ rows.
- [ ] Exact performance measurement methodology is unknown; 20–30 seconds is an observed approximate response time, not a formal benchmark.
- [ ] Automated testing was not performed/remembered.
- [ ] No formal output-validation methodology is remembered.
- [ ] No production deployment details exist because the application remained a hackathon prototype.
- [ ] The exact causal relationship between the hackathon and the later GenAI Developer role transition should not be overstated. What is remembered is that after the hackathon Round 2, a manager interviewed me for Python and I subsequently joined a team working on a RAG-based chatbot/SAP data migration context.

---

## 16. Personal Learning / Takeaways

- Learned how to turn Python/pandas data-processing functionality into an interactive Streamlit application.
- Learned how Streamlit session state can maintain a working dataset across different UI sections.
- Gained experience integrating code developed by multiple team members.
- Learned the importance of dividing a larger application into independently developed feature areas.
- Gained experience leading a small technical team during a hackathon.
- Learned that a prototype designed around local file uploads may not directly match enterprise data-engineering environments.
- The Round 2 feedback helped me recognize the importance of considering **data lakes and data warehouses** when designing enterprise-oriented data applications.
- Learned from the large-dataset test that functionality that works on smaller datasets can experience significant response-time issues as data volume increases.
- The project strengthened my Python application-development experience and preceded my transition into work involving GenAI/RAG systems.
