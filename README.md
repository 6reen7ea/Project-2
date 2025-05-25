# Russian Tech Job-Market Exploration 

Analyzing 49 k+ job postings from the Russian hiring platform **HeadHunter** with PostgreSQL & Python.

---

## Table of Contents
1. [Project Goals](#project-goals)  
2. [Dataset](#dataset)  
3. [Analysis Pipeline](#analysis-pipeline)  
4. [Key Findings](#key-findings)  
5. [Repository Structure](#repository-structure)  
6. [Reproducing the Results](#reproducing-the-results)  
7. [Next Steps](#next-steps)  
8. [Author](#author)

---

## Project Goals  

> *“What does the Russian tech-hiring landscape actually look like, and how can a data scientist use SQL to uncover it?”*  

This project walks through the full analytics workflow:

* **Business questions**  
  * How many vacancies, employers and regions are represented?  
  * Which skills (Python, SQL, Postgres, etc.) appear most often in Data-Science roles?  
  * What salary levels are offered at different experience tiers?  
* **Technical objective** – demonstrate advanced SQL + pandas skills (queries, CTEs, window functions) and storytelling with data.

---

## Dataset  

| Source | Description | Rows |
|--------|-------------|------|
| `vacancies` | Raw postings pulled from HeadHunter API | 49 197 jobs :contentReference[oaicite:0]{index=0} |
| `employers` | Hiring companies | 23 501 employers :contentReference[oaicite:1]{index=1} |
| `areas`, `industries`, … | Supporting reference tables | — |

The course-provided PostgreSQL instance is hosted by SkillFactory.  
Credentials are **NOT** committed to the repo — set them with environment variables or your own `config.py`.

---

## Analysis Pipeline  

1. **SQL Exploration** – pure SQL in Jupyter:  
   * aggregate counts, salary statistics, skill frequencies  
   * join across areas & industries  
2. **pandas + psycopg2** – fetch query results into DataFrames for quick EDA and charting.  
3. **Visual Storytelling** (matplotlib / seaborn) – salary distributions, top-N skills, city rankings.  
4. **Interpretation** – business-oriented insights and actionable recommendations.

---

## Key Findings  

* **Market size** – ~50 k open roles from >23 k companies over the snapshot period.  
* **Skill demand** – Python & SQL dominate Data-Science listings; Postgres is the most named database engine.  
* **Experience & pay** – Senior DS roles (3-6 yrs) offer the highest median salary; entry-level roles cluster in Moscow & St-Petersburg.  
* **Breadth of skills** – On average, a DS vacancy lists ~5 distinct key skills, signalling broad expectations from employers.  

*(Full query outputs, tables and charts live inside the notebook.)*

---

## Repository Structure  

