---
layout: default
title: Ahmed Melaih — Data Scientist & Senior System Analyst
description: "Data Scientist and Senior System Analyst with 7+ years of experience in financial services, enterprise platforms, and mission-critical systems in Bahrain."
---

<!-- ── About ── -->
<section id="about" class="section reveal">
  <h2 class="section-heading">About</h2>
  <p>I'm a <strong>Data Scientist and Senior System Analyst</strong> with <strong>7+ years of experience</strong> across financial services, enterprise platforms, and mission-critical systems in Bahrain and the wider MENA region.</p>
  <p>My work sits at the intersection of <strong>machine learning, NLP, and GenAI</strong> — I don't just build models in notebooks, I take them into production. I've delivered fraud detection pipelines, customer segmentation engines, time-series forecasting systems, and LLM-powered support applications that real teams depend on.</p>
  <p>What sets me apart is the combination: deep technical expertise in <strong>Python, XGBoost, Keras, and cloud platforms</strong> layered on top of hands-on experience with core banking infrastructure, government broadcasting systems, and ERP platforms. I understand both the data and the systems it flows through.</p>
  <p>Currently completing an advanced programme in <strong>Data Science, Analytics & AI</strong> at SkillsUnion, focused on data strategy, governance, and cutting-edge ML methods.</p>
</section>

<!-- ── Skills ── -->
<section id="skills" class="section reveal">
  <h2 class="section-heading">Skills</h2>

  <div class="skill-group">
    <h3>Machine Learning &amp; AI</h3>
    <div class="skill-badges">
      <span class="badge">XGBoost</span>
      <span class="badge">Keras / TensorFlow</span>
      <span class="badge">LSTM</span>
      <span class="badge">Scikit-learn</span>
      <span class="badge">NLP</span>
      <span class="badge">SHAP</span>
      <span class="badge">LLMs / RAG</span>
      <span class="badge">GenAI</span>
    </div>
  </div>

  <div class="skill-group">
    <h3>Languages &amp; Data</h3>
    <div class="skill-badges">
      <span class="badge">Python</span>
      <span class="badge">SQL</span>
      <span class="badge">JavaScript</span>
      <span class="badge">Pandas</span>
      <span class="badge">NumPy</span>
      <span class="badge">Power BI</span>
      <span class="badge">Tableau</span>
    </div>
  </div>

  <div class="skill-group">
    <h3>Cloud &amp; MLOps</h3>
    <div class="skill-badges">
      <span class="badge">AWS</span>
      <span class="badge">Azure</span>
      <span class="badge">GCP</span>
      <span class="badge">MLflow</span>
      <span class="badge">Docker</span>
      <span class="badge">Git / GitHub</span>
      <span class="badge">Jupyter</span>
    </div>
  </div>

  <div class="skill-group">
    <h3>Systems &amp; Platforms</h3>
    <div class="skill-badges">
      <span class="badge">Core Banking Systems</span>
      <span class="badge">ERP</span>
      <span class="badge">ServiceNow (ITSM)</span>
      <span class="badge">IBM GBM</span>
      <span class="badge">FreeRTOS</span>
      <span class="badge">ESP32</span>
    </div>
  </div>
</section>

<!-- ── Projects ── -->
<section id="projects" class="section reveal">
  <h2 class="section-heading">Projects</h2>

  <div class="projects-grid">

    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="fas fa-brain"></i></div>
        <div class="project-links">
          <a href="https://github.com/AhmedMelaih/NLP_Tweets_Sentiment_Classification" target="_blank" rel="noopener" aria-label="View on GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <h3 class="project-title">Tweet Sentiment Classification (NLP)</h3>
      <p class="project-desc">End-to-end NLP pipeline classifying tweet sentiment using a bidirectional LSTM trained on GloVe word embeddings. Applied aggressive text cleaning, class-balancing, and SHAP token-level attribution to explain which words drove each prediction — making the model auditable, not just accurate.</p>
      <div class="project-metrics">
        <span class="metric"><strong>F1</strong> 0.89 (val)</span>
        <span class="metric"><strong>Stack</strong> Keras · LSTM · GloVe · SHAP</span>
      </div>
      <div class="project-tags">
        <span class="tag">LSTM</span><span class="tag">Keras</span><span class="tag">GloVe</span><span class="tag">SHAP</span><span class="tag">NLP</span><span class="tag">Python</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="fas fa-shield-alt"></i></div>
        <div class="project-links">
          <a href="https://github.com/AhmedMelaih/XGBoost_Fraud_Detection" target="_blank" rel="noopener" aria-label="View on GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <h3 class="project-title">Credit Card Fraud Detection</h3>
      <p class="project-desc">Tackled one of financial ML's hardest challenges: extreme class imbalance where fraud accounts for under 0.2% of transactions. Used XGBoost with custom class weighting, stratified cross-validation, and PR-AUC as the primary metric. SHAP analysis revealed the three most predictive signals — transaction amount, inter-transaction time delta, and merchant risk score.</p>
      <div class="project-metrics">
        <span class="metric"><strong>PR-AUC</strong> 0.84</span>
        <span class="metric"><strong>Stack</strong> XGBoost · SHAP · imbalanced-learn</span>
      </div>
      <div class="project-tags">
        <span class="tag">XGBoost</span><span class="tag">SHAP</span><span class="tag">Imbalanced Learning</span><span class="tag">Stratified CV</span><span class="tag">Python</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-header">
        <div class="project-icon"><i class="fas fa-chart-line"></i></div>
        <div class="project-links">
          <a href="https://github.com/AhmedMelaih/Bank_Stock_Price_Analysis_For_GitHub" target="_blank" rel="noopener" aria-label="View on GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <h3 class="project-title">Bank Stock Price Analysis</h3>
      <p class="project-desc">Comparative performance and correlation analysis across major U.S. bank tickers using live data from yfinance. Built rolling-mean smoothing, cumulative return curves, and a Seaborn correlation heatmap. Identified highly-correlated pairs (|ρ| &gt; 0.8) and periods of divergence — useful as a foundation for pairs-trading strategies.</p>
      <div class="project-metrics">
        <span class="metric"><strong>Max correlation</strong> |ρ| &gt; 0.8</span>
        <span class="metric"><strong>Stack</strong> yfinance · Pandas · Seaborn</span>
      </div>
      <div class="project-tags">
        <span class="tag">Python</span><span class="tag">yfinance</span><span class="tag">Pandas</span><span class="tag">Seaborn</span><span class="tag">Finance</span>
      </div>
    </div>

  </div>

  <a href="https://github.com/AhmedMelaih" target="_blank" rel="noopener" class="view-all-link">
    View all projects on GitHub <i class="fas fa-arrow-right"></i>
  </a>
</section>

<!-- ── Experience ── -->
<section id="experience" class="section reveal">
  <h2 class="section-heading">Experience</h2>

  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-date">Jul 2020 — Present</div>
      <div class="timeline-body">
        <h3>Sr. System Analyst — Core Systems</h3>
        <div class="timeline-company">Ministry of Information (GBM–IBM) · Bahrain</div>
        <ul>
          <li>Led API integration, upgrade, and maintenance of mission-critical national broadcasting systems, maintaining <strong>99.999% uptime</strong>.</li>
          <li>Architected and delivered integration of a new digital archiving platform, reducing asset retrieval time by <strong>40%</strong>.</li>
          <li>Managed multi-vendor relationships and SLA compliance across enterprise infrastructure.</li>
          <li>Introduced data monitoring dashboards enabling proactive incident detection before SLA breach.</li>
        </ul>
        <div class="timeline-tags">
          <span class="badge">IBM</span><span class="badge">API Integration</span><span class="badge">SLA Management</span><span class="badge">Digital Archiving</span>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Jan 2025 — Aug 2025</div>
      <div class="timeline-body">
        <h3>Data Scientist — Advanced Skills Programme</h3>
        <div class="timeline-company">SkillsUnion</div>
        <ul>
          <li>Intensive training covering advanced ML, deep learning, NLP, and GenAI pipelines.</li>
          <li>Studied data strategy, governance frameworks, and compliance in regulated industries.</li>
          <li>Built portfolio projects applying XGBoost, LSTM, and LLM techniques to real datasets.</li>
        </ul>
        <div class="timeline-tags">
          <span class="badge">ML</span><span class="badge">Deep Learning</span><span class="badge">GenAI</span><span class="badge">Data Governance</span>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Jan 2020 — Jun 2020</div>
      <div class="timeline-body">
        <h3>ERP System Analyst</h3>
        <div class="timeline-company">Almoayyed Computers · Bahrain</div>
        <ul>
          <li>Analyzed ERP data flows and translated complex client requirements into integration specs.</li>
          <li>Optimized internal delivery processes, improving efficiency and customer satisfaction scores.</li>
          <li>Led cross-functional coordination for project delivery and issue escalation.</li>
        </ul>
        <div class="timeline-tags">
          <span class="badge">ERP</span><span class="badge">Data Analysis</span><span class="badge">Process Optimization</span>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Jan 2017 — Dec 2019</div>
      <div class="timeline-body">
        <h3>IT Engineer</h3>
        <div class="timeline-company">GWC Ltd · Bahrain</div>
        <ul>
          <li>Supported continuity of banking system operations; tier-2/3 support for enterprise financial and logistics clients.</li>
          <li>Delivered system upgrades, patch management, and automation of IT operations.</li>
          <li>Authored SOPs and support documentation to standardize and accelerate resolution times.</li>
        </ul>
        <div class="timeline-tags">
          <span class="badge">Banking Systems</span><span class="badge">Enterprise IT</span><span class="badge">Automation</span>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Jan 2017 — Jun 2017</div>
      <div class="timeline-body">
        <h3>IT Support — Dealing Room</h3>
        <div class="timeline-company">BNP Paribas MEA · Bahrain</div>
        <ul>
          <li>Provided end-user and infrastructure support directly on the trading floor under high-pressure conditions.</li>
          <li>Managed IT hardware inventory and incident tickets through ServiceNow in line with BNP's global ITSM governance.</li>
        </ul>
        <div class="timeline-tags">
          <span class="badge">ServiceNow</span><span class="badge">Trading Floor</span><span class="badge">ITSM</span><span class="badge">BNP Paribas</span>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ── Education ── -->
<section id="education" class="section reveal">
  <h2 class="section-heading">Education</h2>

  <div class="edu-list">
    <div class="edu-item">
      <div class="edu-date">2025</div>
      <div class="edu-body">
        <h3>Data Science, Analytics &amp; AI</h3>
        <div class="edu-institution">SkillsUnion</div>
      </div>
    </div>
    <div class="edu-item">
      <div class="edu-date">2016</div>
      <div class="edu-body">
        <h3>B.Sc. Computer Science</h3>
        <div class="edu-institution">University of Bahrain</div>
      </div>
    </div>
  </div>
</section>

<!-- ── Footer ── -->
<footer class="footer reveal">
  <p>Designed &amp; built by <strong style="color:var(--lightest-slate)">Ahmed Melaih</strong> · <a href="mailto:ahmedemlaih@gmail.com">ahmedemlaih@gmail.com</a> · Bahrain</p>
</footer>
