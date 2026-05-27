# Skill: Recreate Ahmed Melaih's Portfolio

## What this skill does

Guides Claude through faithfully rebuilding `ahmedmelaih.github.io` — a dark-themed, single-page portfolio for a Data Scientist / Senior System Analyst — using the design tokens and rationale in `DESIGN.md`.

## When to use

- Rebuilding `index.html` from scratch or migrating to a new stack (React, Next.js, Astro, etc.)
- Adding new sections while staying visually consistent
- Generating a component in isolation (a new project card, a new timeline entry)
- Reviewing a change for design fidelity

## Context files to read first

Always read these before generating any markup or styles:

| File | Purpose |
|------|---------|
| `DESIGN.md` | Design tokens (colors, typography, spacing, animation, components) + rationale |
| `index.html` | Complete reference implementation in vanilla HTML/CSS/JS |
| `assets/style.css` | Supplementary styles (if present) |

## Content inventory

The portfolio has six data objects. Use this as the source of truth when recreating sections.

### Person
```
Name:     Ahmed Melaih
Title:    Data Scientist & Senior System Analyst
Tagline:  Turning messy data into deployable models that forecast outcomes and drive decisions.
Email:    ahmedemlaih@gmail.com
GitHub:   https://github.com/AhmedMelaih
LinkedIn: https://linkedin.com/in/ahmedmelaih
Resume:   assets/Ahmed Melaih Data Scientist Resume FO.pdf
Avatar:   docs/assets/me_official.png
Location: Bahrain
```

### Navigation sections (in order)
```
#about, #skills, #projects, #experience, #education
```

### Skills
```
Machine Learning & AI:   XGBoost, Keras/TensorFlow, LSTM, Scikit-learn, NLP, SHAP, LLMs/RAG, GenAI
Languages & Data:        Python, SQL, JavaScript, Pandas, NumPy, Power BI, Tableau
Cloud & MLOps:           AWS, Azure, GCP, MLflow, Docker, Git/GitHub, Jupyter
Systems & Platforms:     Core Banking Systems, ERP, ServiceNow (ITSM), IBM GBM, FreeRTOS, ESP32
```

### Projects
```yaml
- title: Tweet Sentiment Classification (NLP)
  icon: fa-brain
  github: https://github.com/AhmedMelaih/NLP_Tweets_Sentiment_Classification
  description: >
    End-to-end NLP pipeline classifying tweet sentiment using a bidirectional LSTM
    trained on GloVe word embeddings. Applied text cleaning, class balancing, and SHAP
    token-level attribution to make predictions auditable, not just accurate.
  metrics:
    - label: F1
      value: "0.89 (val)"
    - label: Stack
      value: "Keras · LSTM · GloVe · SHAP"
  tags: [LSTM, Keras, GloVe, SHAP, NLP]

- title: Credit Card Fraud Detection
  icon: fa-shield-alt
  github: https://github.com/AhmedMelaih/XGBoost_Fraud_Detection
  description: >
    Tackled extreme class imbalance (fraud < 0.2%) using XGBoost with custom class
    weighting and PR-AUC optimization. SHAP analysis revealed the top three fraud
    signals: transaction amount, time delta, and merchant risk score.
  metrics:
    - label: PR-AUC
      value: "0.84"
    - label: Stack
      value: "XGBoost · SHAP · imbalanced-learn"
  tags: [XGBoost, SHAP, Imbalanced Learning, Stratified CV]

- title: Bank Stock Price Analysis
  icon: fa-chart-line
  github: https://github.com/AhmedMelaih/Bank_Stock_Price_Analysis_For_GitHub
  description: >
    Comparative performance and correlation analysis of major U.S. bank tickers via
    yfinance. Built rolling-mean smoothing, cumulative return curves, and a correlation
    heatmap to surface highly-correlated pairs for potential pairs-trading strategies.
  metrics:
    - label: Max correlation
      value: "|ρ| > 0.8"
    - label: Stack
      value: "yfinance · Pandas · Seaborn"
  tags: [Python, yfinance, Pandas, Seaborn, Finance]
```

### Experience (reverse-chronological)
```yaml
- date: Jul 2020 — Present
  role: Sr. System Analyst — Core Systems
  company: Ministry of Information (GBM–IBM) · Bahrain
  bullets:
    - Led API integration, upgrade, and maintenance of mission-critical broadcasting systems, maintaining 99.999% uptime.
    - Delivered integration of a digital archiving platform, cutting asset retrieval time by 40%.
    - Managed multi-vendor relationships and SLA compliance across enterprise infrastructure.
  tags: [IBM, API Integration, SLA Management]

- date: Jan 2025 — Aug 2025
  role: Data Scientist — Advanced Skills Programme
  company: SkillsUnion
  bullets:
    - Intensive training in advanced ML, deep learning, NLP, and GenAI pipelines.
    - Applied data strategy, governance frameworks, and compliance in regulated industries.
  tags: [ML, Deep Learning, GenAI, Data Governance]

- date: Jan 2020 — Jun 2020
  role: ERP System Analyst
  company: Almoayyed Computers · Bahrain
  bullets:
    - Analyzed ERP data flows and translated complex client requirements into integration specifications.
    - Optimized delivery processes, improving efficiency and customer satisfaction scores.
  tags: [ERP, Data Analysis, Process Optimization]

- date: Jan 2017 — Dec 2019
  role: IT Engineer
  company: GWC Ltd · Bahrain
  bullets:
    - Supported continuity of banking systems; delivered tier-2/3 support for enterprise clients in financial and logistics sectors.
    - Managed system upgrades, patch management, and IT operations automation.
  tags: [Banking Systems, Enterprise IT, Automation]

- date: Jan 2017 — Jun 2017
  role: IT Support — Dealing Room
  company: BNP Paribas MEA · Bahrain
  bullets:
    - Provided end-user and infrastructure support on the trading floor under high-pressure conditions.
    - Managed hardware inventory and incidents via ServiceNow under BNP's global ITSM governance.
  tags: [ServiceNow, Trading Floor, ITSM]
```

### Education
```yaml
- year: 2025
  degree: Data Science, Analytics & AI
  school: SkillsUnion

- year: 2016
  degree: B.Sc. Computer Science
  school: University of Bahrain
```

## Reconstruction rules

### Structure
1. Single HTML file (`index.html`) with inline `<style>` and inline `<script>` — no build step required.
2. Font Awesome 6.5 CDN for icons (`fa-*` classes). No other icon library.
3. Google Fonts for Inter and JetBrains Mono — preconnect headers required.
4. No JavaScript frameworks. Use vanilla JS with `IntersectionObserver` for scroll behavior.

### CSS architecture
- All tokens are CSS custom properties on `:root` (see `DESIGN.md → colors`, `typography`).
- Use `var(--token-name)` everywhere; never hardcode hex values in component rules.
- Mobile-first: base styles target mobile, `@media (min-width: 768px)` handles tablet/desktop, `@media (min-width: 1100px)` for wide desktop.
- The sidebar uses `transform: translateX(-100%)` on mobile and `position: sticky; height: 100vh` on desktop — these are mutually exclusive states driven by the media query.

### JavaScript behavior
Three behaviors only — do not add more without explicit request:
1. **Mobile menu**: hamburger toggles `.open` on `#sidebar` and `.show` on `#overlay`.
2. **Active nav**: `IntersectionObserver` with `rootMargin: '-25% 0px -65% 0px'` sets `.active` on the matching nav link.
3. **Reveal animation**: `IntersectionObserver` with `threshold: 0.07` adds `.in` to `.reveal` elements; unobserves after first trigger.

### Adding a new project card
Copy this template, fill the placeholders, and append inside `.proj-grid`:
```html
<div class="proj-card">
  <div class="proj-top">
    <div class="proj-icon"><i class="fas {ICON}"></i></div>
    <div class="proj-gh"><a href="{GITHUB_URL}" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a></div>
  </div>
  <p class="proj-title">{TITLE}</p>
  <p class="proj-desc">{DESCRIPTION}</p>
  <div class="proj-metrics">
    <span class="metric"><strong>{METRIC_LABEL}</strong> {METRIC_VALUE}</span>
  </div>
  <div class="proj-tags">
    <span class="tag">{TAG}</span>
  </div>
</div>
```

### Adding a new experience entry
Copy this template and append inside `.timeline`:
```html
<div class="t-item">
  <p class="t-date">{DATE_RANGE}</p>
  <p class="t-role">{ROLE_TITLE}</p>
  <p class="t-company">{COMPANY} · {LOCATION}</p>
  <ul>
    <li>{BULLET_1}</li>
    <li>{BULLET_2}</li>
  </ul>
  <div class="t-tags badges">
    <span class="badge">{TAG}</span>
  </div>
</div>
```

## Design fidelity checklist

Before marking any recreation complete, verify:

- [ ] CSS custom properties match `DESIGN.md` color tokens exactly
- [ ] Inter used for headings/body; JetBrains Mono for all labels/metadata
- [ ] Sidebar is `sticky` on desktop, drawer on mobile
- [ ] Nav bar animates from 28px → 48px on hover/active
- [ ] Teal used only as accent (text, borders, icons) — never as a large fill
- [ ] Card hover: `translateY(-4px)` + teal border + deep shadow
- [ ] Reveal animation fires once per section (IntersectionObserver unobserves after trigger)
- [ ] `scroll-margin-top: 72px` on sections (mobile), `100px` (desktop)
- [ ] Mobile header has `backdrop-filter: blur(10px)`
- [ ] All external links have `target="_blank" rel="noopener"`
- [ ] Resume PDF link points to `assets/Ahmed Melaih Data Scientist Resume FO.pdf`
