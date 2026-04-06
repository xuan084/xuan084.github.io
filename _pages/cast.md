---
permalink: /cast/
title: "CAST"
author_profile: false
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>
/* Project Page Styles */
.project-container { max-width: 1000px; margin: 0 auto; padding: 0 20px; }

/* Header Section */
.project-header { text-align: center; padding: 40px 0 30px; }
.project-venue-badge { 
  display: inline-block; 
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
  color: #fff; 
  padding: 6px 18px; 
  border-radius: 25px; 
  font-size: 0.9em; 
  font-weight: 600; 
  margin-bottom: 20px;
  box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
}
.project-title { 
  font-size: 2.2em; 
  font-weight: 700; 
  line-height: 1.3; 
  margin-bottom: 15px;
  color: #1a1a1a;
}
.project-subtitle {
  font-size: 1.3em;
  color: #555;
  font-weight: 400;
  margin-bottom: 25px;
}

/* Authors */
.project-authors { 
  font-size: 1.1em; 
  margin-bottom: 10px;
  line-height: 1.8;
}
.project-authors a { 
  color: #667eea; 
  text-decoration: none; 
  font-weight: 500;
}
.project-authors a:hover { text-decoration: underline; }
.affiliations {
  font-size: 0.95em;
  color: #666;
  margin-bottom: 25px;
}
.affiliations sup { color: #667eea; font-weight: 600; }

/* Links Bar */
.links-bar { 
  display: flex; 
  justify-content: center;
  gap: 15px; 
  flex-wrap: wrap; 
  margin-bottom: 30px;
}
.links-bar a { 
  display: inline-flex; 
  align-items: center; 
  gap: 8px; 
  padding: 10px 24px; 
  border-radius: 8px; 
  font-size: 1em; 
  font-weight: 600; 
  text-decoration: none; 
  color: #fff; 
  transition: all 0.2s ease;
}
.links-bar a:hover { 
  transform: translateY(-2px); 
  box-shadow: 0 6px 20px rgba(0,0,0,0.15); 
}
.btn-arxiv { background: #b31b1b; }
.btn-pdf { background: #d4451a; }
.btn-code { background: #24292e; }
.btn-video { background: #ff0000; }

/* Teaser Image */
.teaser-section { margin: 30px 0 40px; text-align: center; }
.teaser-image { 
  max-width: 100%; 
  border-radius: 12px; 
  box-shadow: 0 8px 30px rgba(0,0,0,0.12);
}
.teaser-caption {
  margin-top: 15px;
  font-size: 0.95em;
  color: #555;
  font-style: italic;
}

/* Abstract Section */
.abstract-section {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  border-radius: 12px;
  padding: 30px 35px;
  margin: 40px 0;
}
.abstract-title {
  font-size: 1.4em;
  font-weight: 700;
  margin-bottom: 15px;
  color: #1a1a1a;
}
.abstract-text {
  font-size: 1.05em;
  line-height: 1.8;
  color: #333;
  text-align: justify;
}

/* Section Styling */
.project-section { margin: 50px 0; }
.section-title {
  font-size: 1.6em;
  font-weight: 700;
  color: #1a1a1a;
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 3px solid #667eea;
  display: inline-block;
}

/* Method Cards */
.method-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  margin: 30px 0;
}
.method-card {
  background: #fff;
  border-radius: 12px;
  padding: 25px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  border-left: 4px solid #667eea;
}
.method-card h3 {
  font-size: 1.2em;
  color: #667eea;
  margin-bottom: 12px;
  font-weight: 600;
}
.method-card p {
  font-size: 0.95em;
  line-height: 1.7;
  color: #444;
  margin: 0;
}

/* Figures */
.figure-block {
  margin: 35px 0;
  text-align: center;
}
.figure-block img {
  max-width: 100%;
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.1);
}
.figure-caption {
  margin-top: 12px;
  font-size: 0.9em;
  color: #555;
  line-height: 1.5;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

/* Results Grid */
.results-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin: 30px 0;
}
.result-item {
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 3px 15px rgba(0,0,0,0.06);
  text-align: center;
}
.result-number {
  font-size: 2.5em;
  font-weight: 700;
  color: #667eea;
  line-height: 1;
}
.result-label {
  font-size: 0.95em;
  color: #555;
  margin-top: 8px;
}

/* Highlights List */
.highlights-list {
  list-style: none;
  padding: 0;
  margin: 25px 0;
}
.highlights-list li {
  padding: 14px 0 14px 20px;
  margin-bottom: 8px;
  font-size: 1em;
  line-height: 1.6;
  color: #333;
  border-left: 3px solid #667eea;
}
.highlights-list { list-style: none !important; padding: 0 !important; }
.highlights-list li { list-style: none !important; }

/* BibTeX */
.bibtex-section {
  background: #f6f8fa;
  border-radius: 10px;
  padding: 25px;
  margin: 30px 0;
  position: relative;
}
.bibtex-code {
  font-family: 'SF Mono', Monaco, Consolas, monospace;
  font-size: 0.8em;
  line-height: 1.6;
  color: #24292e;
  overflow-x: auto;
  white-space: pre-wrap;
  word-break: break-all;
}
.bibtex-copy-btn {
  position: absolute;
  top: 15px;
  right: 15px;
  background: #667eea;
  color: #fff;
  border: none;
  padding: 6px 14px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.85em;
  font-weight: 500;
  transition: background 0.2s;
}
.bibtex-copy-btn:hover { background: #5a6fd6; }

/* Responsive */
@media (max-width: 768px) {
  .project-title { font-size: 1.6em; }
  .project-subtitle { font-size: 1.1em; }
  .links-bar a { padding: 8px 18px; font-size: 0.9em; }
  .abstract-section { padding: 20px; }
  .method-grid { grid-template-columns: 1fr; }
}
</style>

<div class="project-container">

  <!-- Header -->
  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> ACL 2026 Findings</div>
    <h1 class="project-title">CAST: Achieving Stable LLM-based Text Analysis for Data Analytics</h1>
    <div class="project-subtitle">Consistency via Algorithmic Prompting and Stable Thinking</div>
    
    <div class="project-authors">
      <a href="https://jxtse.github.io">Jinxiang Xie</a><sup>1</sup>,
      Zihao Li<sup>2</sup>,
      Wei He<sup>3</sup>,
      Rui Ding<sup>4</sup>,
      Shi Han<sup>4</sup>,
      Dongmei Zhang<sup>4</sup>
    </div>
    <div class="affiliations">
      <sup>1</sup>Nanjing University &nbsp;|&nbsp;
      <sup>2</sup>Tsinghua University &nbsp;|&nbsp;
      <sup>3</sup>Peking University &nbsp;|&nbsp;
      <sup>4</sup>Microsoft Research
    </div>

    <div class="links-bar">
      <a href="https://arxiv.org/abs/2602.15861" class="btn-arxiv" target="_blank"><i class="fas fa-file-alt"></i> Paper</a>
      <a href="https://arxiv.org/pdf/2602.15861" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <!-- <a href="#" class="btn-code" target="_blank"><i class="fab fa-github"></i> Code</a> -->
    </div>
  </header>

  <!-- Teaser Figure -->
  <section class="teaser-section">
    <img src="{{ '/images/cast-fig2-framework.png' | relative_url }}" alt="CAST Framework Overview" class="teaser-image">
    <div class="teaser-caption">
      <strong>Figure 1:</strong> Overview of the CAST framework. Traditional methods (left) operate with uncontrolled reasoning paths, resulting in wide, high-entropy output distributions. CAST (right) mitigates instability via Algorithmic Prompting and Thinking-before-Speaking, collapsing the generation process into a sharply concentrated output distribution.
    </div>
  </section>

  <!-- Abstract -->
  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> Abstract</div>
    <div class="abstract-text">
      Text analysis of tabular data relies on two core operations: <strong>summarization</strong> for corpus-level theme extraction and <strong>tagging</strong> for row-level labeling. A critical limitation of employing large language models (LLMs) for these tasks is their inability to meet the high standards of <em>output stability</em> demanded by data analytics.
      <br><br>
      To address this challenge, we introduce <strong>CAST</strong> (<strong>C</strong>onsistency via <strong>A</strong>lgorithmic Prompting and <strong>S</strong>table <strong>T</strong>hinking), a framework that enhances output stability by constraining the model's latent reasoning path. CAST combines (i) <strong>Algorithmic Prompting</strong> to impose a procedural scaffold over valid reasoning transitions and (ii) <strong>Thinking-before-Speaking</strong> to enforce explicit intermediate commitments before final generation.
      <br><br>
      To measure progress, we introduce <strong>CAST-S</strong> and <strong>CAST-T</strong>, stability metrics for bulleted summarization and tagging, and validate their alignment with human judgments. Experiments across publicly available benchmarks on multiple LLM backbones show that CAST consistently achieves the best stability among all baselines, improving Stability Score by up to <strong>16.2%</strong>, while maintaining or improving output quality.
    </div>
  </section>

  <!-- Key Contributions -->
  <section class="project-section">
    <h2 class="section-title">Key Contributions</h2>
    <ul class="highlights-list">
      <li><strong>Formalization of TADA:</strong> We formalize Text Analysis for Data Analysis (TADA) as a tabular-centric paradigm, highlighting stability as a functional necessity for integrating probabilistic LLM outputs into deterministic OLAP workflows.</li>
      <li><strong>CAST Framework:</strong> A novel approach that constrains generation via Algorithmic Prompting and intermediate commitments, reducing the entropy of latent paths without expensive search-based methods.</li>
      <li><strong>Stability Metrics:</strong> We introduce CAST-S and CAST-T, stability-focused evaluation metrics combining semantic matching with order sensitivity (Kendall's Tau) to capture human-perceived consistency.</li>
      <li><strong>Strong Empirical Results:</strong> Up to 16.2% improvement in Stability Score across multiple LLM backbones, with no regression in accuracy.</li>
    </ul>
  </section>

  <!-- Method -->
  <section class="project-section">
    <h2 class="section-title">Method</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 25px;">
      CAST addresses the instability problem by constraining the LLM's latent reasoning trajectory through two complementary mechanisms:
    </p>
    
    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-sitemap"></i> Algorithmic Prompting</h3>
        <p>Specifies an algorithmic scaffold for the task, translating classic deterministic workflows into a structured prompt sequence. This scaffold acts as a strong prior over valid reasoning transitions, effectively pruning high-entropy paths.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-brain"></i> Thinking-before-Speaking</h3>
        <p>Enforces the scaffold by requiring the model to produce well-defined intermediate states (domain, topic schema, clusters) before emitting the final output. By committing to these states, the model follows a more stable reasoning path.</p>
      </div>
    </div>

    <div class="figure-block">
      <img src="{{ '/images/cast-fig1-tada.png' | relative_url }}" alt="TADA Operations">
      <div class="figure-caption">
        <strong>Figure 2:</strong> Illustration of the summarization and tagging operations for TADA. These atomic operations can be composed and reused in complex TADA tasks.
      </div>
    </div>
  </section>

  <!-- Empirical Observation -->
  <section class="project-section">
    <h2 class="section-title">Empirical Observation</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 20px;">
      We empirically demonstrate that requiring relevant intermediate states demonstrably sharpens the model's output distribution. As shown below, CAST produces the sharpest and most concentrated distribution, indicating substantially improved run-to-run stability.
    </p>
    
    <div class="figure-block">
      <img src="{{ '/images/cast-fig3-kde.png' | relative_url }}" alt="Output Length Stability">
      <div class="figure-caption">
        <strong>Figure 3:</strong> Output-length stability under different prompting strategies. KDE-smoothed distributions of summary length compare (i) direct prompting, (ii) irrelevant intermediate states, (iii) relevant intermediate states, and (iv) the full CAST prompt. CAST produces the sharpest distribution with outputs tightly clustered around a central value.
      </div>
    </div>
  </section>

  <!-- Results -->
  <section class="project-section">
    <h2 class="section-title">Results</h2>
    
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">16.2%</div>
        <div class="result-label">Maximum Stability Score Improvement</div>
      </div>
      <div class="result-item">
        <div class="result-number">32</div>
        <div class="result-label">Dataset-Query Pairs Evaluated</div>
      </div>
      <div class="result-item">
        <div class="result-number">5,100+</div>
        <div class="result-label">Items Across 4 Diverse Domains</div>
      </div>
    </div>

    <div class="figure-block">
      <img src="{{ '/images/cast-fig4-tagging.png' | relative_url }}" alt="Tagging Pipeline">
      <div class="figure-caption">
        <strong>Figure 4:</strong> The CAST framework for tagging, illustrating a pipeline that begins with query decomposition and domain identification to guide the core algorithmic prompting stage, and concludes with output validation.
      </div>
    </div>
  </section>

  <!-- Citation -->
  <section class="project-section">
    <h2 class="section-title">Citation</h2>
    <div class="bibtex-section">
      <button class="bibtex-copy-btn" onclick="navigator.clipboard.writeText(this.nextElementSibling.innerText);this.textContent='Copied!';setTimeout(()=>this.textContent='Copy',2000);">Copy</button>
      <div class="bibtex-code">@misc{xie2026castachievingstablellmbased,
      title={CAST: Achieving Stable LLM-based Text Analysis for Data Analytics}, 
      author={Jinxiang Xie and Zihao Li and Wei He and Rui Ding and Shi Han and Dongmei Zhang},
      year={2026},
      eprint={2602.15861},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2602.15861}, 
}</div>
    </div>
  </section>

  <!-- Acknowledgments -->
  <section class="project-section" style="margin-top: 50px; padding-top: 30px; border-top: 1px solid #e1e4e8;">
    <p style="font-size: 0.9em; color: #666; line-height: 1.6;">
      <strong>Acknowledgments:</strong> This work was done during the author's internship at Microsoft Research. We thank all colleagues and mentors from the DKI group for their support and valuable feedback.
    </p>
  </section>

</div>
