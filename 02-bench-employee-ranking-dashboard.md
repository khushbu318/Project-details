# Bench Employee Ranking Dashboard

**Company:** Capgemini  
**Role:** Associate (Python Developer)  
**Timeframe:** July 2022 – 2023  
**Team Size:** Not remembered  
**My Position in Team:** Python Developer — Dashboard/Application Development

**One-line Summary:** Developed a Streamlit-based internal dashboard that used employee Excel data to filter, score, and rank bench employees against project requirements, helping the Project Allocation Team identify suitable candidates for interview and potential billing-project allocation.

---

## 1. Problem / Why It Existed

### Business Problem

Capgemini had a pool of employees who were on the bench and had not yet been allocated to billing projects.

The Project Allocation Team needed an effective way to identify suitable employees for ongoing project requirements. The existing process depended heavily on manually maintained Excel files across different accounts.

Because there could be hundreds of employees in an account and multiple Excel files, the manual process made it difficult to consistently identify the best-fit candidates. Employees whose resumes or information happened to be readily available could receive opportunities before other potentially better-matched candidates.

The project was created to make the candidate identification process more systematic by filtering and ranking employees according to project requirements.

### Technical Problem

The employee information was maintained in Excel files and handled manually.

The application needed to:

- Load employee data from account-specific Excel files.
- Allow users to specify project requirements.
- Filter employees according to required technical skills.
- Apply an approximately 80% skill-match criterion, with the threshold configurable by the user.
- Consider certifications and bench duration in candidate scoring.
- Rank the matching candidates.
- Present the ranked candidates through an interactive dashboard.
- Allow candidates to be moved toward the interview process.
- Allow results to be exported as CSV.

### Who Used It

The primary users were the **Project Allocation Team**.

They could use the dashboard to enter project requirements, identify matching bench employees, review ranked candidates, and move selected candidates into the interview process.

### Why This Solution Was Needed

The existing manual process involved multiple Excel files and large amounts of employee information.

The dashboard provided a more structured way to search for candidates instead of relying on manually finding resumes or employee records.

---

## 2. My Role & Ownership

### What I Personally Built

I worked as a Python Developer on the dashboard/application development team.

My primary responsibilities included:

- Building the Streamlit UI from scratch.
- Reading Excel data using Python and Pandas.
- Implementing the candidate filtering logic.
- Implementing the filtering → scoring → ranking flow in Python.
- Implementing the frontend action for moving a candidate toward the interview process.
- Debugging and testing the dashboard.
- Building the application based on the business requirements defined by the team.

I learned parts of the Streamlit implementation independently using resources such as YouTube, Medium, and Stack Overflow.

### What I Contributed To

I contributed to the implementation of the internal candidate-ranking application, particularly the dashboard and application logic.

The application allowed users to:

1. Load an account-specific Excel file.
2. Select project requirements.
3. Filter candidates.
4. Score matching candidates.
5. Rank candidates.
6. Review candidate information.
7. Move selected candidates toward the interview process.
8. Export results as CSV.

### What Other Team Members Owned

The project was a team effort.

A team-lead-level colleague worked with me and helped confirm the UI and logic.

The **business scoring rules were decided by the team**, rather than being independently designed by me.

A director requested that I work on the project and helped guide the overall requirement/business direction.

The exact responsibilities of other team members around deployment and Excel preparation are not fully remembered.

---

## 3. System / Product Overview

### What the System Does

The Bench Employee Ranking Dashboard is an internal Streamlit application for identifying suitable bench employees for project requirements.

The application takes employee information from account-specific Excel files and allows the Project Allocation Team to specify the technical requirements of a project.

Candidates are first filtered based on the requirements. Matching candidates are then scored and ranked.

The ranking considers factors such as:

- Technical skill match.
- Certification status.
- Bench duration.
- Other team-defined criteria.

The ranked results can then be reviewed by the allocation team, and selected employees can be moved into the interview process.

### End-to-End Flow

```text
Account-specific Excel File
            ↓
     Load Employee Data
            ↓
    Project Requirements
    (Dropdowns / Checkboxes)
            ↓
       Skill Filtering
            ↓
   Approx. 80% Skill Match
     Configurable Threshold
            ↓
       Candidate Scoring
            ↓
        Candidate Ranking
            ↓
      Ranked Candidate List
            ↓
    Review Candidate Details
            ↓
      Select for Interview
            ↓
       Interview Process
            ↓
 Potential Project / Billing Allocation
```

---

## 4. Architecture / How It Worked

### High-Level Architecture

The application was primarily a Python-based Streamlit dashboard.

The basic architecture consisted of:

```text
Excel Files
    ↓
Pandas
    ↓
Python Processing / Filtering
    ↓
Scoring & Ranking Logic
    ↓
Streamlit UI
    ↓
Project Allocation Team
```

The application processed one account file at a time because different accounts maintained separate Excel files.

The files followed the same general format.

### Step-by-Step Flow

1. The user loaded an account-specific Excel file into the application.
2. The application read the employee records using Pandas.
3. The user selected project requirements through Streamlit controls such as dropdowns and checkboxes.
4. The application compared project requirements against employee skill information.
5. Candidates below the configured skill-match threshold were filtered out.
6. Matching candidates were scored using team-defined criteria.
7. Candidates were sorted according to their score.
8. The ranked candidates were displayed in the dashboard.
9. The user could review relevant candidate information.
10. The user could select a candidate and move the candidate toward the interview process.
11. Results could also be exported as CSV.

### Component Responsibilities

| Component | Responsibility |
|---|---|
| Excel files | Source of employee information |
| Pandas | Read employee Excel data into Python |
| Python filtering logic | Match employee information against project requirements |
| Python scoring logic | Calculate candidate scores after filtering |
| Ranking logic | Sort candidates based on score |
| Streamlit | Provide the interactive dashboard/UI |
| CSV export | Allow users to export results |
| Interview action | Provide a frontend action to move a selected candidate toward interview |

---

## 5. Tech Stack

| Technology | Where It Was Used | Why It Was Used |
|---|---|---|
| Python | Application logic | Main programming language used to build the dashboard logic |
| Streamlit | Frontend/UI | Used to build the interactive internal dashboard |
| Pandas | Data loading and processing | Used to read and work with Excel employee data |
| Excel | Input data source | Existing source of bench employee information |
| CSV | Result export | Used to export candidate results |

---

## 6. Implementation Details

### Backend

The application logic was written in Python.

Pandas was used to load employee information from Excel files.

The employee data generally had one row per employee.

Different accounts had separate Excel files, but the files followed the same general structure.

The data included information such as:

- Employee ID
- Employee name
- Gender
- Joining information
- Account
- Bench-related information
- Main technical skills
- Certification information
- Mandatory certification status
- Other employee information

The employee skill information was represented using separate columns for the main skills rather than one comma-separated skills field.

For example, the structure could contain separate fields representing skills such as Python, SQL, Java, etc.

The certification information was also represented using separate columns. Around four main certifications were checked, with information represented using values such as **Yes/No**.

The code used lowercase representations for matching to make the skill comparisons consistent.

### Frontend

The Streamlit UI was created from scratch.

The dashboard had several functional areas.

One area displayed candidate records, primarily using the employee ID rather than exposing all employee information in the initial table.

Another area contained controls for filtering candidates according to project requirements.

The controls included remembered examples such as:

- Technical skill filters.
- Certification-related options.
- Bench-duration-related filters.
- Dropdowns.
- Checkboxes.

The final results area displayed ranked candidates and provided an action that could be used to move a selected candidate toward the interview process.

Candidate information displayed in the ranked results included items such as:

- Employee ID
- Technical stack
- Certification score/status where available

### AI / ML

No AI/ML component is remembered for this project.

The application used rule-based filtering and scoring rather than a machine-learning model.

### Database / Storage

No database is remembered as part of the application.

The primary input source was account-specific Excel files.

### APIs / Integrations

No external API integration is remembered.

The application primarily operated on Excel data using Python/Pandas and presented the results through Streamlit.

### Infrastructure / Deployment

The exact deployment infrastructure is **not remembered**.

This should remain an Open Question rather than assuming a particular hosting platform or deployment architecture.

---

## 7. Key Technical Decisions

### Decision 1

**What:** Use Streamlit for the dashboard UI.

**Why:** The project required an internal interactive dashboard, and Streamlit allowed the Python development team to build the UI without requiring a separate frontend technology.

**Alternative:** A separate web frontend/backend architecture could have been used.

**Trade-off:** Streamlit simplified development for a Python-focused team, while providing less traditional frontend separation than a dedicated frontend framework.

---

### Decision 2

**What:** Use Pandas to process Excel employee data.

**Why:** The existing employee information was maintained in Excel, and Pandas provided a practical way to load and process tabular data in Python.

**Alternative:** Manual Excel processing or another spreadsheet-processing approach.

**Trade-off:** Pandas allowed the filtering and scoring logic to be handled programmatically rather than manually.

---

### Decision 3

**What:** Filter candidates before applying the ranking/scoring process.

**Why:** The application first needed to identify candidates who sufficiently matched the project requirements before ranking them.

**Alternative:** Score every employee in the account and rank everyone.

**Trade-off:** Filtering reduced the candidate pool before scoring and made the ranking more focused on candidates who met the project requirements.

---

### Decision 4

**What:** Make the skill-match threshold configurable.

**Why:** The initial matching approach used an approximately 80% skill-match threshold, but users needed the ability to adjust the threshold if the default level did not produce suitable matches.

**Alternative:** Use a fixed 80% threshold.

**Trade-off:** A configurable threshold gave the allocation team more flexibility when dealing with different project requirements and candidate availability.

---

## 8. Challenges & How I Solved Them

### Challenge 1

**Problem:** The existing employee-selection process relied heavily on multiple Excel files and manual candidate identification.

**Root Cause:** Large amounts of employee information were maintained separately across account files, making manual searching inefficient.

**Solution:** Built an interactive Streamlit dashboard that allowed the allocation team to load an account file, specify requirements, filter candidates, and rank the resulting candidates.

**Result:** The team had a more structured way to identify candidates rather than relying only on manually locating employee information.

---

### Challenge 2

**Problem:** Candidates needed to be matched against project-specific technical requirements.

**Root Cause:** Different projects could require different combinations of technical skills.

**Solution:** Implemented configurable filtering controls and Python-based matching logic.

The matching process used normalized lowercase values and compared employee skills against the selected requirements.

**Result:** Candidates could be filtered according to the selected project requirements.

---

### Challenge 3

**Problem:** Simply finding technically relevant employees was not enough; candidates also needed to be prioritized.

**Root Cause:** Multiple employees could satisfy the project requirements.

**Solution:** Implemented a scoring and ranking process after filtering.

The team-defined scoring considered factors such as technical skill matching, certification status, and bench duration.

**Result:** Matching candidates were ordered by score so the allocation team could focus on higher-ranked candidates first.

---

### Challenge 4

**Problem:** I needed to build the Streamlit application while working with a technology I was learning.

**Root Cause:** Streamlit was part of the implementation and I did not have extensive prior experience with it.

**Solution:** Learned the required implementation patterns independently using resources such as YouTube, Medium, and Stack Overflow, and applied that knowledge while building the dashboard.

**Result:** I was able to build the Streamlit dashboard from scratch and take responsibility for debugging and testing it.

---

## 9. Testing / Validation

I was responsible for debugging and testing the dashboard.

Validation focused on the behavior of the dashboard and its filtering/ranking workflow.

Important scenarios included:

- Loading account employee data.
- Selecting project requirements.
- Filtering candidates based on skills.
- Applying the skill-match threshold.
- Calculating candidate scores.
- Sorting candidates by score.
- Displaying ranked candidates.
- Selecting a candidate for the interview process.
- Exporting results as CSV.
- Changing requirements and running the ranking process again.

The exact formal testing framework or automated test suite is not remembered.

---

## 10. Production / Deployment

The project was an internal Capgemini application.

The exact production/deployment process, hosting environment, and deployment tooling are not remembered.

**Open Question:** The final hosting/deployment mechanism should be confirmed if remembered.

---

## 11. Impact / Results

### Technical Impact

The project converted a largely manual Excel-based candidate identification process into an interactive Python/Streamlit dashboard.

The application provided:

- Programmatic candidate filtering.
- Rule-based candidate scoring.
- Candidate ranking.
- Interactive project requirement selection.
- Candidate interview actions.
- CSV result export.

### Business Impact

The dashboard helped the Project Allocation Team identify suitable bench employees more systematically against project requirements.

It was intended to improve the utilization of bench employees and help suitable employees reach interviews and potential billing-project opportunities.

### Metrics

No verified quantitative metrics are currently remembered.

We should **not** claim specific improvements in allocation time, utilization percentage, number of employees allocated, or project revenue without confirmation.

---

## 12. Resume / Portfolio Summary

### Short Summary

Built an internal Streamlit dashboard at Capgemini to help the Project Allocation Team identify suitable bench employees for project opportunities. The application loaded account-specific Excel data using Pandas, filtered employees based on configurable skill requirements, calculated team-defined candidate scores using factors such as skill match, certifications, and bench duration, and ranked candidates for the interview process.

### Resume-Oriented Bullets

- Developed a **Python/Streamlit internal dashboard** to rank bench employees against project requirements and improve visibility for the Project Allocation Team.
- Built Excel-based data processing using **Pandas**, with configurable skill filtering and an approximately 80% skill-match threshold.
- Implemented **rule-based candidate scoring and ranking** using technical skill match, certification status, and bench-duration criteria defined by the team.
- Created the Streamlit UI from scratch, including filtering controls, ranked candidate views, interview-selection actions, and CSV export.
- Debugged and tested the dashboard and independently learned Streamlit implementation techniques using technical learning resources.

---

## 13. Interview Talking Points

### 1. The Business Problem

The project addressed a manual bench-employee allocation process where employee information was spread across Excel files and it was difficult to consistently identify the best candidate for a project.

### 2. My Role

I worked as a Python Developer on the dashboard team. My main ownership was the Streamlit application, Python filtering/ranking implementation, UI development, debugging, and testing.

### 3. Why Streamlit

Streamlit allowed us to create an interactive dashboard using Python without requiring a separate frontend stack.

### 4. How Candidate Matching Worked

The user selected project requirements through dropdowns/checkboxes. Employees that did not meet the required skill-match threshold were filtered out. Matching candidates were then scored and ranked.

### 5. The 80% Skill Match

The application used an approximately 80% skill-match threshold. For example, if five skills were required and an employee matched four, that represented an 80% match. The threshold could be adjusted by the user.

### 6. How Ranking Worked

After filtering, the Python code calculated a candidate score. The scoring rules were defined by the team and considered factors such as technical skills, certifications, and bench duration. Candidates were then sorted according to their scores.

### 7. My Technical Ownership vs. Business Logic

I implemented the application and ranking flow in Python, but the underlying business scoring criteria were decided by the team. This distinction is important when describing my contribution accurately.

### 8. Handling Multiple Accounts

Each account had its own Excel file. The files were processed one at a time, although they followed the same general structure.

### 9. What Happened After Ranking

The allocation team reviewed the ranked candidates and could move selected candidates toward the interview process. The interview outcome ultimately helped determine the final selection when candidates were otherwise similarly ranked.

### 10. What I Learned

The project gave me practical experience building an internal data-driven application with Python, Pandas, and Streamlit, including interactive filtering, rule-based scoring, ranking, debugging, and working from business requirements.

---

## 14. Likely Interview Questions

### Q1. What problem did the project solve?

**Answer:**  
It helped the Project Allocation Team identify suitable bench employees for project opportunities. Previously, employee information was maintained across multiple Excel files and handled manually, which made it difficult to consistently find the best-fit candidates.

### Q2. Why did you use Streamlit?

**Answer:**  
We needed an internal interactive dashboard, and Streamlit allowed us to build the UI directly in Python. It was a practical choice because the application logic was also being developed in Python.

### Q3. How did you load the employee data?

**Answer:**  
The application loaded account-specific Excel files, and I used Pandas to read the tabular employee information into Python.

### Q4. How did the skill matching work?

**Answer:**  
The user selected required skills through the dashboard. Employee skills were stored in separate columns, and I normalized the values to lowercase before matching. Candidates below the configured skill-match threshold were filtered out.

### Q5. What was the 80% rule?

**Answer:**  
The application generally used an approximately 80% skill-match threshold. For example, if five skills were required and an employee matched four, that employee had an 80% match. The threshold could be adjusted by the user when necessary.

### Q6. How was the final ranking calculated?

**Answer:**  
After filtering, my Python code calculated the candidate score and sorted the candidates by that score. The scoring criteria were defined by the team and included factors such as technical skill match, certifications, and bench duration. I implemented the application-side scoring and ranking flow, but I did not independently design the business weighting methodology.

### Q7. What data was available for each employee?

**Answer:**  
The Excel data contained employee information such as employee ID, name, gender, joining information, account, bench-related information, technical skills, and certification status. The main skills and certifications were represented in separate columns.

### Q8. How did certifications affect ranking?

**Answer:**  
Completed relevant certifications contributed positively to the candidate score. The team-defined scoring rules gave additional weight to candidates with the relevant certifications.

### Q9. How did bench duration affect ranking?

**Answer:**  
Bench duration was considered when prioritizing candidates. When multiple candidates matched the project requirements, employees who had been on the bench for a longer period received greater consideration.

### Q10. Did you build the UI yourself?

**Answer:**  
Yes. I built the Streamlit UI from scratch. I also implemented the filtering logic and the frontend action for moving a selected candidate toward the interview process.

### Q11. Did you design the scoring rules?

**Answer:**  
No. The business scoring criteria were decided by the team. My responsibility was to implement the application logic based on those requirements and integrate the scoring and ranking into the dashboard.

### Q12. Did you use machine learning?

**Answer:**  
No. This was a rule-based application rather than a machine-learning system. The candidate ranking was based on filtering and team-defined scoring rules.

### Q13. What was challenging for you personally?

**Answer:**  
One challenge was building the Streamlit application while learning the framework. I independently used resources such as YouTube, Medium, and Stack Overflow to understand the technology and then applied it while developing the dashboard.

### Q14. What happened when candidates had the same score?

**Answer:**  
The dashboard displayed the relevant candidate information, and the candidates could proceed to the interview process. The final decision was based on the interview performance rather than relying on an additional automated tie-breaking algorithm.

### Q15. What would you improve if you built it again?

**Answer:**  
A useful improvement would be to make the scoring methodology more configurable and transparent, so allocation users could understand why a candidate received a particular score. I would also consider stronger validation of the Excel input structure and more formal automated testing.

---

## 15. Open Questions / Gaps

- [ ] Exact project start/end dates within July 2022–2023.
- [ ] Exact team size.
- [ ] Exact deployment/hosting environment.
- [ ] Exact scoring formula and numerical weights.
- [ ] Exact formula used to calculate bench duration.
- [ ] Whether the bench-duration calculation used a specific bench-start date or another date field.
- [ ] Exact names of the four certifications.
- [ ] Exact list of technical-skill columns.
- [ ] Exact Streamlit controls/buttons used in the final UI.
- [ ] Exact mechanism used by the interview-selection action beyond the frontend behavior.
- [ ] Exact formal testing approach or automated test coverage.
- [ ] Whether there was a formal production release or primarily an internal application/prototype.
- [ ] Quantitative business impact, such as number of candidates processed, employees allocated, time saved, or utilization improvement.

---

## 16. Personal Learning / Takeaways

- Learned to build an interactive data application using **Python and Streamlit**.
- Gained practical experience using **Pandas with Excel-based business data**.
- Learned how to translate business requirements into filtering and ranking logic.
- Learned the importance of separating **business rules** from their technical implementation.
- Gained experience building a UI from scratch rather than only working on backend code.
- Improved debugging and testing skills through hands-on application development.
- Learned independently through technical resources such as YouTube, Medium, and Stack Overflow.
- Gained experience working with a team where business/scoring decisions were defined collaboratively while I owned a significant portion of the dashboard implementation.
- Learned that internal business applications often need to balance technical matching with practical human decision-making—the ranking helped prioritize candidates, while interviews remained important for the final decision.