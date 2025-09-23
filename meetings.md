### Week of Sept 23, 2025 – Meeting Notes

1) **What was planned (MS Project)**
- Build a simple **Work Breakdown Structure (WBS)** for the PEMS dataset work:
  Setup & Onboarding → Data Extraction → Data Cleaning/Normalization → EDA → Vector DB (demo) → Documentation.
- Assign placeholder durations (1 day per task) and show a **Gantt chart** to communicate sequencing and dependencies.

2) **What I learned (clarification)**
- **MS Project is for planning, not data cleaning.** It makes timelines/dependencies but cannot clean rows/columns.
- I will use **MS Project (or a free alternative)** for the plan only, and **Python/Excel** for actual cleaning/analysis.

3) **What I did this week (results)**
- Identified columns for analysis:
  - Location: `Fwy`, `District`, `County`, `City`
  - Geometry: `CA PM`, `Abs PM`, `Length`
  - Attributes: `Lanes`, `HOV`, `Type`, `Sensor Type`
- Wrote a **cleaning plan** (to implement in Python/Excel):
  - Normalize column names/types (`Length`, `CA PM`, `Abs PM` → numeric; `Lanes` → integer).
  - Standardize categories (e.g., `HOV` → {Yes, No, Unknown}).
  - Create `SegmentID = Fwy + '_' + round(Abs PM, 3)`.
  - Handle missing values (keep `City` as “Unknown”; decide rule for missing `Length`).
- Defined initial **EDA**:
  - Histogram of `Length`, bar chart of `Lanes`.
  - HOV coverage by district/county.
  - Counts by `District`/`County` and missing-data hotspots.
  - Basic anomalies: `Length <= 0`, `Lanes <= 0`, duplicate `SegmentID`.

4) **Roadblocks**
- Could not use MS Project locally (software access), so no native .MPP/Gantt yet.
- Workaround: document WBS/timeline in Markdown/Excel in GitHub; use ProjectLibre/GanttProject if a Gantt is required.

5) **Agenda for next week**
- Implement `/src/clean/clean_pems.py` → output `/data/processed/pems_clean.csv`.
- Create `/notebooks/01_eda.ipynb`:
  - Histogram of `Length`
  - Bar chart of `Lanes`
  - HOV coverage table by district
- Draft `/docs/data_dictionary.md` and `/docs/eda_report.md`.

6) **Repo updates**
- Added this status to `meetings.md`.
- Planning docs will live under `/docs/` so progress is visible even without MS Project.

**Note:** MS Project won’t clean data. I’ll keep planning artifacts in GitHub and proceed with Python/Excel for the data work; will switch to a free PM tool if a Gantt visualization is requested.
