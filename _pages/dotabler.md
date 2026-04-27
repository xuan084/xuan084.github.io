---
permalink: /dotabler/
title: "DoTabler"
author_profile: false
lang: en
lang_alt: /zh/dotabler/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">

<div class="project-container">

  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> ECAI 2025</div>
    <h1 class="project-title">From Surface to Semantics: Semantic Structure Parsing for Table-Centric Document Analysis</h1>
    <div class="project-subtitle">A table-anchored framework for deep, context-aware document understanding</div>

    <p class="pp-hero-tagline">
      Existing PDF analysis stops at <em>surface-level</em> layout and OCR. <strong>DoTabler</strong> goes one layer deeper — using tables as anchors to recover their semantically associated text, enabling table-centric document parsing and domain-specific table retrieval at <strong>orders-of-magnitude lower latency than GPT-4o</strong>.
    </p>

    <div class="project-authors">
      <a href="https://xuan084.github.io"><strong>Xuan Li</strong></a>,
      Jialiang Dong<sup>*</sup>,
      Raymond Wong<sup>*</sup>
    </div>
    <div class="affiliations">
      University of New South Wales, Sydney, Australia &nbsp;|&nbsp;
      <sup>*</sup>Corresponding authors
    </div>

    <div class="links-bar">
      <a href="https://arxiv.org/abs/2508.10311" class="btn-arxiv" target="_blank"><i class="fas fa-file-alt"></i> Paper</a>
      <a href="/files/dotabler-paper.pdf" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <a href="/files/dotabler-poster.pdf" class="btn-pdf" target="_blank"><i class="fas fa-image"></i> Poster</a>
      <a href="https://github.com/xuan084/DoTabler2025" class="btn-code" target="_blank"><i class="fab fa-github"></i> Code</a>
    </div>
  </header>

  <section class="teaser-section">
    <img src="{{ '/images/dotabler-pipeline.png' | relative_url }}" alt="DoTabler overall workflow" class="teaser-image">
    <div class="teaser-caption">
      <strong>Figure 1:</strong> Overall workflow of DoTabler. Document Structure Preprocessing produces parsed blocks; Relation-Aware Annotation builds a table-text dataset; the Table-Text Association Model (TTAM) is trained on this data and powers two downstream capabilities — Table-Centric Semantic Parsing and Domain-Specific Table Retrieval.
    </div>
  </section>

  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> Abstract</div>
    <div class="abstract-text">
      Documents are core carriers of information across finance, healthcare, and scientific research, with tables being the primary medium for structured data. Existing studies focus on surface-level tasks — layout analysis, table detection, data extraction — and stop short of <em>deep semantic parsing</em> of tables and their contextual associations. This limits advanced tasks such as cross-paragraph data interpretation and context-consistent analysis.
      <br><br>
      We propose <strong>DoTabler</strong>, a table-centric semantic document parsing framework designed to uncover deep semantic links between tables and their context. DoTabler leverages a custom-built dataset and domain-specific fine-tuning of pretrained models, integrating a complete parsing pipeline that identifies the context segments semantically tied to each table. Built on this semantic understanding, DoTabler delivers two core functionalities: <strong>table-centric document structure parsing</strong> and <strong>domain-specific table retrieval</strong>.
      <br><br>
      Evaluated on nearly <strong>4,000 pages with over 1,000 tables</strong> from real-world PDFs, DoTabler achieves <strong>over 90% Precision and F1</strong>, outperforming GPT-4o, Gemini-2.0, and Claude-3.5 in table-context semantic analysis while running <strong>two orders of magnitude faster</strong>.
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Two Use Cases</h2>
    <div class="figure-block">
      <img src="{{ '/images/dotabler-usecase-parsing.png' | relative_url }}" alt="Table-centric parsing example">
      <div class="figure-caption">
        <strong>Figure 2a — Table-Centric Parsing.</strong> Given a PDF page, DoTabler identifies each table block and recovers the surrounding paragraphs that semantically describe or interpret it.
      </div>
    </div>
    <div class="figure-block">
      <img src="{{ '/images/dotabler-usecase-retrieval.png' | relative_url }}" alt="Domain-specific table retrieval example">
      <div class="figure-caption">
        <strong>Figure 2b — Domain-Specific Table Retrieval.</strong> Given a natural-language query, DoTabler returns the tables in a document that are semantically relevant, together with their associated context.
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Key Contributions</h2>
    <div class="pp-contrib-grid pp-fadeup-stagger">
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">01</div>
        <h3 class="pp-contrib-title">First Table-Centric Semantic Dataset</h3>
        <p class="pp-contrib-text">A new PDF semantic-level dataset modeled around table-centric structures, paired with the <strong>Table-Text Association Model (TTAM)</strong> for fine-grained table–context relation analysis.</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">02</div>
        <h3 class="pp-contrib-title">DoTabler Framework</h3>
        <p class="pp-contrib-text">An end-to-end pipeline that combines preprocessing (segmentation, layout, OCR) with TTAM, enabling both <strong>document structure parsing</strong> and <strong>domain-specific table retrieval</strong> in a single framework.</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">03</div>
        <h3 class="pp-contrib-title">Comprehensive Evaluation</h3>
        <p class="pp-contrib-text">Evaluated on nearly <strong>4,000 pages with 1,000+ tables</strong> from arXiv and PubMed Central, beating GPT-4o, Gemini-2.0, and Claude-3.5 on accuracy <em>and</em> running orders of magnitude faster.</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Method</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 25px;">
      DoTabler decomposes table-centric semantic parsing into a three-stage pipeline. Each stage is modular and replaceable, making the framework extensible to new pretrained encoders or document domains.
    </p>

    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-cogs"></i> 1. Document Structure Preprocessing</h3>
        <p>Each PDF is rendered to images, segmented into pages, and passed through a Faster R-CNN layout detector fine-tuned on <code>PubLayNet</code>. Tesseract OCR extracts text from <em>Text</em>, <em>List</em>, <em>Title</em>, and <em>Table</em> blocks.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-link"></i> 2. Table-Text Association Model (TTAM)</h3>
        <p>A sentence-pair classifier built on a pretrained encoder (BERT / BART / RoBERTa). For each <code>(table, text)</code> pair, TTAM outputs a binary "related / unrelated" label, trained with cross-entropy over balanced positive/negative pairs.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-stream"></i> 3a. Table-Centric Semantic Parsing</h3>
        <p>For every Table block in a document, TTAM scores all candidate Text/List blocks and returns the semantically associated subset, yielding a structured <code>(table, related_paragraphs)</code> view of the document.</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-search"></i> 3b. Domain-Specific Table Retrieval</h3>
        <p>A fine-tuned RoBERTa cross-encoder jointly encodes <code>(query, table)</code> pairs and produces a relevance score; tables are ranked and the top-K returned with their context. Trained with margin-based ranking loss.</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Dataset &amp; Experimental Setup</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 20px;">
      No public dataset existed for document-level semantic structure analysis with table-centric anchors, so we built the first one. Documents were sampled from arXiv and PubMed Central; two senior annotators independently labeled table-text relations and reconciled disagreements via expert consensus.
    </p>

    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">227</div>
        <div class="result-label">Source PDFs (arXiv + PubMed Central)</div>
      </div>
      <div class="result-item">
        <div class="result-number">3,952</div>
        <div class="result-label">Pages parsed and annotated</div>
      </div>
      <div class="result-item">
        <div class="result-number">1,061</div>
        <div class="result-label">Table blocks · 1,624 Text blocks</div>
      </div>
    </div>

    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 25px;">
      <strong>Splits.</strong> TTAM evaluation: 3,248 balanced table-text pairs split 7:3 (2,273 train / 975 test). Retrieval evaluation: 200 query-table pairs filtered to 129 train / 53 test. <strong>Baselines.</strong> GPT-4o, Gemini-2.0 Flash, Claude-3.5 — all prompted with the same task instruction so the comparison is fair.
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Results</h2>

    <h3 style="margin-top: 8px; margin-bottom: 14px;">Table-Text Relation Classification (TTAM)</h3>
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">90.01%</div>
        <div class="result-label">F1 on table–text linking (RoBERTa-based TTAM)</div>
      </div>
      <div class="result-item">
        <div class="result-number">+10 pts</div>
        <div class="result-label">F1 over the strongest LLM baseline (Gemini-2.0)</div>
      </div>
      <div class="result-item">
        <div class="result-number">+41 pts</div>
        <div class="result-label">F1 over GPT-4o (48.48 → 90.01)</div>
      </div>
    </div>

    <h3 style="margin-top: 32px; margin-bottom: 14px;">Document-Level &amp; Retrieval Performance</h3>
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">128 / 193</div>
        <div class="result-label">Documents fully correct (vs. 109–114 for LLM baselines)</div>
      </div>
      <div class="result-item">
        <div class="result-number">71.7%</div>
        <div class="result-label">Retrieval Recall@1 (88.7% at K=3)</div>
      </div>
      <div class="result-item">
        <div class="result-number">~270×</div>
        <div class="result-label">Faster than GPT-4o (0.0035s vs 0.80s avg)</div>
      </div>
    </div>

    <div class="figure-block" style="margin-top: 28px;">
      <img src="{{ '/images/dotabler-latency.png' | relative_url }}" alt="Latency comparison">
      <div class="figure-caption">
        <strong>Figure 3:</strong> Mean and median time overhead per (table, text) pair, batched across 10 evenly-split test groups. DoTabler stays flat near zero while the three LLM baselines fluctuate around 0.6–1.7s.
      </div>
    </div>

    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 25px;">
      <strong>Why DoTabler wins.</strong> Decoder-only LLMs are tuned for fluent generation and adopt conservative decision strategies — they keep precision high but produce many false negatives, missing real table–text associations. RoBERTa's bidirectional encoder, fine-tuned on the new dataset, captures fine-grained contextual dependencies and is far less prone to hallucination, which is exactly what this task rewards.
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">Citation</h2>
    <div class="bibtex-section">
      <button class="bibtex-copy-btn" onclick="navigator.clipboard.writeText(this.nextElementSibling.innerText);this.textContent='Copied!';setTimeout(()=>this.textContent='Copy',2000);">Copy</button>
      <div class="bibtex-code">@inproceedings{li2025dotabler,
  title={From Surface to Semantics: Semantic Structure Parsing for Table-Centric Document Analysis},
  author={Li, Xuan and Dong, Jialiang and Wong, Raymond},
  booktitle={Proceedings of the 28th European Conference on Artificial Intelligence (ECAI)},
  year={2025}
}</div>
    </div>
  </section>

  <section class="project-section" style="margin-top: 50px; padding-top: 30px; border-top: 1px solid #e1e4e8;">
    <p style="font-size: 0.9em; color: #666; line-height: 1.6;">
      <strong>Acknowledgments:</strong> This work was conducted at the University of New South Wales. We thank our annotators for their careful work on the table–text association dataset.
    </p>
  </section>

</div>

{% include project-page-enhance.html %}
