# cv-optimizer-portfolio
**Code Repository:** [CV Optimizer GitHub](https://github.com/Carina6ST/cv-optimizer)  
**Jira Board:** [COW Project Board](https://cristinaaateaca.atlassian.net/jira/software/projects/COW/boards/67?atlOrigin=eyJpIjoiMmQwM2U0NDJkZjAzNDU1Yzk0NDIzOWMxYjAxZTg5MzYiLCJwIjoiaiJ9)  
# Digital Portofolio 
This repository contains the development work for CV Optimizer. The goal of the system is to help job seekers tailor their CVs to specific job descriptions by parsing uploaded documents, extracting keywords, and scoring coverage.

The repo is structured into frontend (React + Tailwind) and backend (Flask, Python) components, with supporting NLP libraries (spaCy, NLTK) for text analysis. Artefacts such as the use case diagram, Gantt chart are included in this portfolio, alongside links to the Jira board and final project reflection.
Project Development — CV Optimizer
1) Scope & Goals

The project delivers a vertical prototype aimed at helping job seekers improve their CVs against specific job descriptions. In its current slice, the system allows users to upload a CV (PDF/DOCX), paste a job description, run basic keyword extraction and coverage scoring, and then view suggestions for improvement.

This directly aligns with the objectives and six-week Agile plan set out in Task 1, though in practice the build compressed into a shorter delivery window.

Acceptance criteria (achieved where marked “done”):

✅ Upload and parse CV (PDF/DOCX) → extracted text shown in UI.

✅ JD input captured on UI and sent to backend.

✅ /api/parse-cv returns extracted text; /api/score returns JSON payload with score, matched keywords, and missing keywords.

✅ Results page highlights coverage and suggestions.

⚠ Basic auth stub wired in (Firebase config only) but payments remain unimplemented.

✅ Verified local run instructions and dev deploy preview.

These items form the working MVP for Task 2.

2) Team Roles & Contributions

Carina - Project Lead & Tester: project planning, QA, documentation.

Cristina - Backend Developer: Flask/FastAPI endpoints.

Atanaska - Frontend Developer: React + Tailwind interface.

This structure mirrors the repository organisation, with /backend and /frontend directories and a README tracking features and run steps.

3) Architecture (Thin Slice)

Frontend (React + Vite, Tailwind CSS)

Pages: Home (CV upload + JD input), Results (coverage + suggestions), Auth stub.

State managed for CV text, JD text, and backend response payloads.

Backend (Python Flask API)

POST /api/parse-cv: accepts file upload, extracts text with pdfplumber and python-docx.

POST /api/score: accepts {cvText, jdText}, tokenises with spaCy/NLTK, calculates coverage %, and suggests missing terms.

Data Flow:
CV file → /api/parse-cv → CV text → /api/score (with JD text) → coverage metrics → frontend highlights.

This reflects the current repo “API (current)” and the declared tech stack.

4) Use Case Diagram

Actors: Job Seeker, Admin (optional).
Use cases: Upload CV, Paste JD, Analyse Keywords, View Score & Suggestions, Download Report (MVP), Sign-up/Login (stub), Subscribe Premium (placeholder).

Diagram image placeholder <img width="1600" height="960" alt="Use_case_diagram" src="https://github.com/user-attachments/assets/44b940f4-8bbe-4c55-b7f9-b980d7665a50" />


5) Project Plan — Planned vs Actual

The initial plan was a six-week Agile sprint framework (28 Jul → 20 Sep 2025). The figure below shows the original timeline alongside actual progress from the GitHub repo.

Gantt chart image <img width="1920" height="960" alt="Gantt_chart" src="https://github.com/user-attachments/assets/766c51dd-2540-427e-be33-33695336f5bb" />


Planned (blue):

Week 1: Repo config, Firebase setup, prerequisites.

Week 2: CV upload & parsing.

Week 3: Flask REST API.

Week 4: React + Tailwind integration.

Week 5: NLP + Stripe integration.

Week 6: Usability tests, benchmark vs Jobscan, deployment.

Actual (red marker):

24 Sep 2025: Repo import with backend + frontend committed, README updated, sample CVs added.

Deviation: Usability testing and Stripe integration were not completed.

6) Technology Stack Implemented

Frontend: React.js + Tailwind CSS

Backend: Flask (Python) REST API

Parsing: pdfplumber (PDF), python-docx (Word)

NLP: spaCy, NLTK

Auth/Database: Firebase (login stub)

Payments (planned): Stripe (not completed)

Deployment & Version Control: Render/Vercel, GitHub

This balance of modern frontend tooling and Python’s NLP ecosystem met the module requirements while remaining feasible in the timeframe.

7) Evidence of Work Done

Repo setup with backend + frontend scaffolding and a structured README.

Backend API stubs (/api/parse-cv, /api/score) created; parsing libraries installed.

Frontend pages set up (upload, JD input, results view).

Early NLP keyword extraction attempted.

Stripe integration and usability tests not completed.

Screenshots from the repo and Jira board provide supporting evidence.

8) Reflection on Project Lead Role

In my role as Project Lead I was responsible for:

Designing the six-week Agile plan and mapping tasks across the team.

Ensuring repo structure and documentation were clear.

Coordinating backend and frontend work through Jira and team check-ins.

Re-prioritising when deadlines tightened, focusing on parsing and scoring features as core deliverables.

Although usability testing was not achieved, I recognise this gap and would enforce smaller pilot testing earlier in future projects to reduce risk. This experience highlights leadership, adaptability, and reflective practice in line with the course outcomes.
