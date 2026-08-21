# Patient No-Show Prediction Model

**Company:** Capgemini (Associate — Python Developer)
**Role / Timeframe:** Jul 2022 – 2023
**One-line summary:** Internal learning project predicting whether a patient will miss a medical appointment, built end-to-end on a public Kaggle dataset to practice classification modeling and model comparison.

## Problem / Why It Existed
No-shows waste scheduling slots and hurt both clinic efficiency and patient health outcomes. This was a self-driven/internal upskilling exercise (not a client engagement) to practice building a full classification pipeline — from raw data to a tuned, compared model — using a real-world-style healthcare dataset.

## My Role & Ownership
Solo project. Owned the entire pipeline: data cleaning, feature engineering, EDA, model building, evaluation, and hyperparameter tuning.

## Architecture / How It Worked
1. **Data source:** Kaggle "Medical Appointment No Shows" dataset — ~110,000 appointment records from Brazil, Nov 2015–Jun 2016.
2. **Cleaning & feature engineering:**
   - Converted `ScheduledDay` / `AppointmentDay` to datetime; extracted day, month, year, and day-of-week for each.
   - Engineered a `DaysBetween` column (appointment date − scheduled date) and dropped ~5 rows with negative values (data errors).
   - Encoded categorical fields: `Gender` (M/F → 1/0), `No-show` (Yes/No → 1/0), `Neighbourhood` (label encoding).
   - Handled `Age` outliers using IQR bounds (e.g., corrected a −1 value to 1); confirmed `Age == 0` records were infants by checking they had no hypertension/diabetes/alcoholism flags.
   - Dropped `A_year` (constant, zero variance) and the raw `ScheduledDay`/`AppointmentDay` columns after correlation analysis showed them ~0.8 correlated with derived fields.
   - Dropped `PatientId` and `AppointmentID` as non-predictive identifiers.
3. **EDA:** Visualized show/no-show splits (~80% show / ~20% no-show) across gender, age groups, neighbourhood, scholarship status, hypertension, diabetes, alcoholism, handicap, and SMS-received, using count plots, box plots, and correlation heatmaps.
4. **Modeling:** Split data 80/20 train/test. Trained and evaluated four classifiers:
   - Decision Tree
   - Random Forest
   - XGBoost
   - CatBoost
   Each evaluated on accuracy, precision, recall, F1-score, and confusion matrix.
5. **Model selection & tuning:** CatBoost had the best accuracy of the four. Ran `GridSearchCV` (8-fold CV) over CatBoost hyperparameters (`iterations`, `learning_rate`, `depth`, `l2_leaf_reg`) to find the best configuration.

## Tech Stack
- **Python** — core language
- **Pandas / NumPy** — data loading, cleaning, feature engineering
- **Matplotlib / Seaborn** — EDA visualizations (count plots, box plots, correlation heatmaps)
- **Scikit-learn** — `LabelEncoder`, `train_test_split`, evaluation metrics, `GridSearchCV`, `DecisionTreeClassifier`, `RandomForestClassifier`
- **XGBoost** — gradient boosting classifier
- **CatBoost** — gradient boosting classifier with native categorical handling; best-performing model

## Key Technical Decisions
- Chose to compare four different model families (tree-based: Decision Tree, Random Forest, XGBoost, CatBoost) rather than committing to one upfront, to see which handled the mixed categorical/numerical healthcare data best.
- Dropped raw date columns in favor of derived features (day/month/weekday, days-between) once correlation analysis showed the raw dates were redundant — kept the model input cleaner and reduced multicollinearity.
- Used IQR-based bounds rather than removing age outliers outright, correcting invalid values instead of discarding rows, to preserve dataset size.
- Selected CatBoost as the final model based on accuracy comparison, then tuned it further with grid search rather than tuning all four models (time/effort trade-off).

## Challenges & How I Solved Them
- **Data inconsistencies:** Found ~5 rows where the scheduled date was after the appointment date (logically invalid) — resolved by filtering them out.
- **Ambiguous zero-age records:** Investigated whether `Age == 0` was bad data or represented infants, by cross-checking against health condition flags, before deciding to keep them as legitimate infant records.
- **Multicollinearity:** Correlation heatmap revealed the raw date columns were highly correlated with engineered features; resolved by dropping the raw columns post-feature-extraction.

## Impact / Results
- CatBoost emerged as the best-performing model among the four evaluated. After tuning via `GridSearchCV` (8-fold CV), best accuracy: **79.88%** with parameters `depth=10, iterations=90, l2_leaf_reg=3, learning_rate=0.2`.
- Stayed as a prototype/analysis — not deployed into a live scheduling system.
- Served as a hands-on upskilling project in classification modeling and model comparison methodology.

## Learnings
- Practical experience running a full classification pipeline end-to-end: cleaning → feature engineering → EDA → multi-model comparison → hyperparameter tuning.
- Reinforced why correlation analysis matters before model training — redundant/highly-correlated features can be quietly dropped without losing information.
- Learned to sanity-check "suspicious" data (like Age == 0) against other fields before deciding to clean vs. keep it, rather than assuming it's an error.
- Hands-on comparison of tree-based ensemble methods (Random Forest, XGBoost, CatBoost) and how their default performance differs on the same dataset.
- Identified follow-up areas for a more production-ready version: handling class imbalance explicitly, SHAP-based interpretability, and periodic retraining.

## Interview Talking Points
- Walk through the full pipeline end-to-end as a demonstration of classification workflow competency, from raw CSV to tuned model.
- Explain the model comparison methodology (why test 4 models, how CatBoost was selected) — shows structured decision-making, not just picking one algorithm by default.
- Mention the data-quality checks (invalid date ordering, age-zero infant validation) as an example of not blindly trusting raw data.

## Open Questions / Gaps
- Precision/recall/F1 breakdowns per class weren't captured in this summary (only overall tuned accuracy) — pull from the notebook if needed for deeper interview detail.
- No production deployment context, since this stayed a prototype.
