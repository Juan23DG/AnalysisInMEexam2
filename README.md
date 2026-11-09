# ME Analysis 1 — Exam 2 Interactive Step-by-Step Tutor

An interactive, self-contained tutoring web application for **Mechanical Engineering Analysis 1 (Exam 2)** covering **140 guided ODE and Laplace Transform problems across 7 Topics (20 Questions per Topic)**, including a dedicated **Unit 7: Heaviside & Dirac Delta Forcing (20 Questions)** and **34 total Heaviside $u(t-c)$ & Dirac delta $\delta(t-c)$ problems** across the question bank.

## ✨ Key Features

- **3-Stage Interactive Tutoring Flow**:
  1. **Step 1 — Method Identification**: Diagnose the correct solution technique via multiple-choice with targeted feedback explaining *why* a method works (and why common exam traps fail).
  2. **Step 2 — Governing Equations & Method Recipe**: Unlocks the exact formula sheet equations, integrating factor / Wronskian / Laplace identities, and a plain-English step-by-step recipe for the chosen method.
  3. **Step 3 — Solve Yourself & Plain-English Hints**: Check your final answer with a two-attempt system. Every question includes plain-English hints explaining **how to set up the forcing function equation** and **how to apply the Laplace transform**.
- **140 Guided Problems Across 7 Topics (20 Questions Each)**:
  1. **Topic 1 — Separable & Linear First-Order ODEs** (20 Qs: 4 Assignment 3 + 16 Practice Bank)
  2. **Topic 2 — Bernoulli & Substitution First-Order ODEs** (20 Qs: 4 Assignment 3 + 16 Practice Bank)
  3. **Topic 3 — Higher-Order Homogeneous, Reduction of Order & Cauchy-Euler** (20 Qs: 5 Assignment 3 + 15 Practice Bank)
  4. **Topic 4 — Undetermined Coefficients & Variation of Parameters** (20 Qs: 5 Assignment 4 + 15 Practice Bank)
  5. **Topic 5 — Direct & Inverse Laplace Transforms** (20 Qs: 4 Assignment 4 + 16 Practice Bank)
  6. **Topic 6 — Laplace IVPs & Mechanical Applications** (20 Qs: 4 Assignment 4 + 16 Practice Bank)
  7. **Topic 7 — Heaviside & Dirac Delta Forcing** (20 Qs: Dedicated unit covering piecewise step $u(t-c)$ setup, 2nd Shifting Theorem $e^{-cs}F(s)$, and Dirac delta $\delta(t-c)$ impulse IVPs & mechanics)
- **⚡ "New Content Added!" Announcement Banner**:
  - Returning and new students see a dismissible announcement banner highlighting **Unit 7: Heaviside & Dirac Delta Forcing (20 Qs)** and the **1-Page Printable Formula Sheet**, with a 1-click button to jump straight into Unit 7.
- **📐 1-Page Printable Quick Method-Picker Guide & Formula Sheet**:
  - Scannable `"If You See..." → "Formula" → "Short Steps"` guide formatted to print cleanly on **one single 8.5" × 11" page**, plus a downloadable [`ODE_Solving_Processes_Formula_Sheet.md`](./ODE_Solving_Processes_Formula_Sheet.md).
- **🎠 Mock Exam Carousel**:
  - Indefinite count-up stopwatch (pause/reset anytime), **Skip for Later**, and **Jump to Skipped** navigation.
  - Preset decks for a **Balanced 7-Question Mock Exam (1 per Topic)**, **Topic Mastery Decks (Topics 1–7, 20 Qs each)**, **⚡ All Heaviside & Dirac Delta Questions Across Bank (34 Qs)**, **Assignments 3 & 4 Only (26 Qs)**, or **All 140 Questions (Shuffled)**.
- **📘 Integrated Lecture & Outside Notes**:
  - **Professor's 21-Page Classroom Board Notes** (Unit 1 through Unit 8)
  - **Dennis G. Zill Textbook Reference Guide**
  - **Paul's Online Math Notes (Lamar DE)** Solved Examples & Practice Deck
  - Contextual slide-over reference drawer linked directly from every problem
- **📱 Tablet, Stylus & Mobile Ready**:
  - Collapsible left sidebar, collapsible question bank pill drawer, and side-by-side **Split Problem View** so the ODE problem statement stays visible while solving Step 3.
  - Built-in touch/stylus/mouse **Scratchpad** for working out integrals on iPad or tablet.
  - Local progress persistence in `localStorage` and Light/Dark mode support.

---

## 🚀 Deploying to Netlify via GitHub

This repository is pre-configured for zero-build static deployment on **Netlify**:

1. Push this repository (`AnalysisInMEexam2`) to GitHub:
   ```bash
   git add .
   git commit -m "Deploy ME Analysis 1 Exam 2 Interactive Tutor (140 problems across 7 units)"
   git push -u origin main
   ```
2. Log in to [Netlify](https://app.netlify.com/) and click **Add new site → Import an existing project**.
3. Choose **GitHub** and select the **`Juan23DG/AnalysisInMEexam2`** repository.
4. Netlify will automatically detect [`netlify.toml`](./netlify.toml):
   - **Branch to deploy**: `main`
   - **Build command**: *(leave blank)*
   - **Publish directory**: `.`
5. Click **Deploy site** — your interactive tutor will be live immediately!
