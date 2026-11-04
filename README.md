# ME Analysis 1 — Exam 2 Interactive Step-by-Step Tutor

An interactive, self-contained tutoring web application for **Mechanical Engineering Analysis 1 (Exam 2)** covering **120 guided ODE and Laplace Transform problems** (**20 questions per topic across all 6 exam topics**).

## ✨ Key Features

- **3-Stage Interactive Tutoring Flow**:
  1. **Step 1 — Method Identification**: Diagnose the correct solution technique via multiple-choice with targeted feedback explaining *why* a method works (and why common exam traps fail).
  2. **Step 2 — Governing Equations & Method Recipe**: Unlocks the exact formula sheet equations, integrating factor / Wronskian / Laplace identities, and step-by-step recipe for the chosen method.
  3. **Step 3 — Solve Yourself & Progressive Checkpoints**: Check your final answer with a two-attempt system. On a first miss, intermediate setup and integral checkpoints unlock automatically so you can compare your work before your second attempt.
- **120 Guided Problems (20 Questions per Topic)**:
  1. **Topic 1 — Separable & Linear First-Order ODEs** (20 Qs: 4 Assignment 3 + 16 Practice Bank)
  2. **Topic 2 — Bernoulli & Substitution First-Order ODEs** (20 Qs: 4 Assignment 3 + 16 Practice Bank)
  3. **Topic 3 — Higher-Order Homogeneous, Reduction of Order & Cauchy-Euler** (20 Qs: 5 Assignment 3 + 15 Practice Bank)
  4. **Topic 4 — Undetermined Coefficients & Variation of Parameters** (20 Qs: 5 Assignment 4 + 15 Practice Bank)
  5. **Topic 5 — Direct & Inverse Laplace Transforms** (20 Qs: 4 Assignment 4 + 16 Practice Bank)
  6. **Topic 6 — Laplace IVPs & Mechanical Applications** (20 Qs: 4 Assignment 4 + 16 Practice Bank)
- **🎠 Mock Exam Carousel**:
  - Indefinite count-up stopwatch (pause/reset anytime), **Skip for Later**, and **Jump to Skipped** navigation.
  - Preset decks for a **Balanced 6-Question Mock Exam (1 per Topic)**, **20-Question Topic Mastery Decks (Topics 1–6)**, **Assignments 3 & 4 Only (26 Qs)**, or **All 120 Questions (Shuffled)**.
- **📘 Integrated Lecture & Outside Notes**:
  - **Professor's 21-Page Classroom Board Notes** (Unit 1 through Unit 8)
  - **Dennis G. Zill Textbook Reference Guide**
  - **Paul's Online Math Notes (Lamar DE)** Solved Examples & Practice Deck
  - Contextual slide-over reference drawer linked directly from every problem
- **📱 Tablet, Stylus & Mobile Ready**:
  - Built-in touch/stylus/mouse **Scratchpad** for working out integrals on iPad or tablet.
  - Local progress persistence in `localStorage` and Light/Dark mode support.

---

## 🚀 Deploying to Netlify via GitHub

This repository is pre-configured for zero-build static deployment on **Netlify**:

1. Push this repository (`AnalysisInMEexam2`) to GitHub:
   ```bash
   git add .
   git commit -m "Deploy ME Analysis 1 Exam 2 Interactive Tutor (120 problems)"
   git push -u origin main
   ```
2. Log in to [Netlify](https://app.netlify.com/) and click **Add new site → Import an existing project**.
3. Choose **GitHub** and select the **`Juan23DG/AnalysisInMEexam2`** repository.
4. Netlify will automatically detect [`netlify.toml`](./netlify.toml):
   - **Branch to deploy**: `main`
   - **Build command**: *(leave blank)*
   - **Publish directory**: `.`
5. Click **Deploy site** — your interactive tutor will be live immediately!
