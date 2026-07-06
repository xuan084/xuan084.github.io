---
permalink: /aitabler/
title: "AITabler"
author_profile: false
lang: en
lang_alt: /zh/aitabler/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">

<div class="project-container">

  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> ICDAR 2026</div>
    <h1 class="project-title">Meaning Lies in Structure: Fine-Grained Table-Centric Document Semantic Parsing</h1>
    <div class="project-subtitle">Fine-grained table-text semantic alignment for reliable document understanding</div>

    <p class="pp-hero-tagline">
      Tables carry decision-critical quantitative evidence, but their meaning often lives in surrounding text. <strong>AITabler</strong> models table-text relationships as a <strong>five-level semantic hierarchy</strong>, integrating PDF structural reconstruction, layout-aware context retrieval, and LLM-based reasoning for table-centric document parsing and question answering.
    </p>

    <div class="project-authors">
      <a href="https://xuan084.github.io"><strong>Xuan Li</strong></a>,
      Mengfei Xiao,
      Jingtian Wei,
      Jialiang Dong,
      Raymond Wong<sup>*</sup>
    </div>
    <div class="affiliations">
      University of New South Wales, Australia &nbsp;|&nbsp;
      University of Technology Sydney, Australia &nbsp;|&nbsp;
      University of Wollongong, Australia &nbsp;|&nbsp;
      <sup>*</sup>Corresponding author
    </div>

    <div class="links-bar">
      <span class="btn-arxiv btn-disabled"><i class="fas fa-file-alt"></i> Paper</span>
      <a href="/files/aitabler-paper.pdf" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <span class="btn-pdf btn-disabled"><i class="fas fa-image"></i> Poster</span>
      <a href="https://github.com/xuan084/Meaning-Lies-in-Structure-Fine-Grained-Table-Centric-Document-Semantic-Parsing" class="btn-code" target="_blank"><i class="fab fa-github"></i> Code</a>
    </div>
  </header>

  <section class="teaser-section">
    <img src="{{ '/images/aitabler-thumb.png' | relative_url }}" alt="AITabler overall workflow" class="teaser-image">
    <div class="teaser-caption">
      <strong>Figure 1:</strong> Overall workflow of AITabler. The system reconstructs PDF structure, retrieves layout-aware spatial context, performs fine-grained table-text semantic relevance grading, and uses the recognized associations to improve downstream table question answering.
    </div>
  </section>

  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> Abstract</div>
    <div class="abstract-text">
      Tables encode quantitative evidence for financial reporting, risk assessment, and policy evaluation. In these settings, automated analysis depends on accurate semantic integration between tabular data and explanatory text; misalignment can distort interpretation and downstream decisions.
      <br><br>
      Existing PDF table research focuses mostly on visual structure recovery, while fine-grained semantic alignment across document components remains underexplored. We address this gap by formulating table-text semantic alignment as a <strong>five-level hierarchical framework</strong> and propose <strong>AITabler</strong>, an end-to-end system that integrates PDF structural reconstruction, layout-aware spatial context modeling, and LLM-based semantic reasoning.
      <br><br>
      We construct two benchmarks: a fine-grained relevance corpus with <strong>29,138 annotated pairs</strong> and a Table-QA dataset with <strong>6,000 questions</strong>, derived from over <strong>3,000 PDF pages</strong>. Experiments show consistent improvements in relevance grading and substantial gains in downstream Table-QA.
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Key Contributions</h2>
    <div class="pp-contrib-grid pp-fadeup-stagger">
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">01</div>
        <h3 class="pp-contrib-title">Five-Level Semantic Alignment</h3>
        <p class="pp-contrib-text">We model table-text relationships as a structured hierarchy, capturing caption reference, content alignment, topical match, contextual relevance, and unrelated context beyond coarse binary relevance.</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">02</div>
        <h3 class="pp-contrib-title">End-to-End AITabler Pipeline</h3>
        <p class="pp-contrib-text">AITabler combines PDF structural reconstruction, spatial context retrieval, and LLM-based reasoning to recover table-text semantic associations at document scale.</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">03</div>
        <h3 class="pp-contrib-title">Benchmarks for Parsing and QA</h3>
        <p class="pp-contrib-text">We release a fine-grained table-text relevance corpus and a purpose-built Table-QA dataset to support reproducible table-centric document analysis research.</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Method</h2>
    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-sitemap"></i> 1. Document Structural Reconstruction</h3>
        <p>PDF pages are parsed into layout blocks so that tables, captions, and surrounding paragraphs can be represented as structured document components.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-map-marker-alt"></i> 2. Spatial Context Retrieval</h3>
        <p>AITabler retrieves nearby candidate paragraphs using layout-aware spatial cues, reducing the search space before semantic grading.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-layer-group"></i> 3. Five-Level Relevance Grading</h3>
        <p>LLM-based reasoning assigns each table-text pair to one of five relevance levels, producing fine-grained associations instead of a single related/unrelated label.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-question-circle"></i> 4. Semantic-Enhanced Table-QA</h3>
        <p>The recognized associations provide high-value context for downstream table question answering, improving accuracy without indiscriminately adding noisy paragraphs.</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Dataset &amp; Results</h2>
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">29,138</div>
        <div class="result-label">Annotated table-text pairs</div>
      </div>
      <div class="result-item">
        <div class="result-number">6,000</div>
        <div class="result-label">Table-QA questions</div>
      </div>
      <div class="result-item">
        <div class="result-number">3,000+</div>
        <div class="result-label">PDF pages used to derive benchmarks</div>
      </div>
    </div>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 22px;">
      Experiments show that AITabler reaches over <strong>98%</strong> accuracy on strongly related samples, exceeds <strong>75%</strong> on weakly related cases, and achieves more than <strong>70%</strong> accuracy on complex QA tasks, substantially outperforming coarse-grained retrieval baselines.
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Citation</h2>
    <div class="bibtex-box">
<pre>@inproceedings{li2026aitabler,
  title={Meaning Lies in Structure: Fine-Grained Table-Centric Document Semantic Parsing},
  author={Li, Xuan and Xiao, Mengfei and Wei, Jingtian and Dong, Jialiang and Wong, Raymond},
  booktitle={International Conference on Document Analysis and Recognition},
  year={2026}
}</pre>
    </div>
  </section>

</div>
