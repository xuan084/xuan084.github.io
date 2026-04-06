---
permalink: /cast/
title: "CAST"
author_profile: true
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>
.project-page { max-width: 900px; margin: 0 auto; }
.project-title { font-size: 1.8em; font-weight: 700; line-height: 1.3; margin-bottom: 0.3em; }
.project-subtitle { font-size: 1.1em; color: #666; margin-bottom: 1.2em; }
.project-venue { display: inline-block; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: #fff; padding: 4px 14px; border-radius: 20px; font-size: 0.85em; font-weight: 600; margin-bottom: 1.2em; }
.project-authors { font-size: 1.05em; margin-bottom: 1.5em; line-height: 1.6; }
.project-authors a { color: #667eea; text-decoration: none; }
.project-authors a:hover { text-decoration: underline; }
.project-links { display: flex; gap: 12px; flex-wrap: wrap; margin-bottom: 2em; }
.project-links a { display: inline-flex; align-items: center; gap: 6px; padding: 8px 18px; border-radius: 8px; font-size: 0.9em; font-weight: 600; text-decoration: none; color: #fff; transition: transform 0.2s, box-shadow 0.2s; }
.project-links a:hover { transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.15); }
.btn-arxiv { background: #b31b1b; }
.btn-pdf { background: #d4451a; }
.btn-code { background: #333; }
.btn-bibtex { background: #2d6a4f; }
.project-figure { margin: 2em 0; text-align: center; }
.project-figure img { max-width: 100%; border-radius: 8px; box-shadow: 0 2px 12px rgba(0,0,0,0.1); }
.project-figure figcaption { margin-top: 0.8em; font-size: 0.9em; color: #666; }
.project-section { margin-bottom: 2em; }
.project-section h2 { font-size: 1.4em; border-bottom: 2px solid #667eea; padding-bottom: 0.3em; margin-bottom: 0.8em; }
.project-abstract { line-height: 1.8; font-size: 1em; text-align: justify; }
.project-highlights { list-style: none; padding: 0; }
.project-highlights li { padding: 8px 0 8px 28px; position: relative; line-height: 1.6; }
.project-highlights li::before { content: "✦"; position: absolute; left: 0; color: #667eea; font-size: 0.9em; }
.bibtex-box { background: #f6f8fa; border: 1px solid #e1e4e8; border-radius: 8px; padding: 16px; font-family: Monaco, Consolas, "Lucida Console", monospace; font-size: 0.82em; line-height: 1.6; overflow-x: auto; white-space: pre-wrap; word-break: break-all; position: relative; }
.bibtex-copy { position: absolute; top: 8px; right: 8px; background: #667eea; color: #fff; border: none; padding: 4px 10px; border-radius: 4px; cursor: pointer; font-size: 0.8em; }
.bibtex-copy:hover { background: #5a6fd6; }
</style>

<div class="project-page">

  <div class="project-title">CAST: Achieving Stable LLM-based Text Analysis for Data Analytics</div>

  <span class="project-venue"><i class="fas fa-award"></i>&nbsp; ACL 2026 Findings</span>

  <div class="project-authors">
    <a href="https://jxtse.github.io"><strong>Jinxiang Xie</strong></a>,
    Zihao Li,
    Wei He,
    Rui Ding,
    Shi Han,
    Dongmei Zhang
  </div>

  <div class="project-links">
    <a href="https://arxiv.org/abs/2602.15861" class="btn-arxiv" target="_blank"><i class="fas fa-file-alt"></i> ArXiv</a>
    <a href="https://arxiv.org/pdf/2602.15861" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
    <!-- <a href="#" class="btn-code" target="_blank"><i class="fab fa-github"></i> Code</a> -->
  </div>

  <figure class="project-figure">
    <img src="{{ '/images/TADA-pipeline.jpg' | relative_url }}" alt="CAST Framework Architecture">
    <figcaption>Overview of the CAST framework: Algorithmic Prompting + Thinking-before-Speaking for stable LLM-based text analysis.</figcaption>
  </figure>

  <div class="project-section">
    <h2><i class="fas fa-align-left"></i> Abstract</h2>
    <p class="project-abstract">
      Text analysis of tabular data relies on two core operations: <em>summarization</em> for corpus-level theme extraction and <em>tagging</em> for row-level labeling. A critical limitation of employing large language models (LLMs) for these tasks is their inability to meet the high standards of output stability demanded by data analytics. To address this challenge, we introduce <strong>CAST</strong> (<strong>C</strong>onsistency via <strong>A</strong>lgorithmic Prompting and <strong>S</strong>table <strong>T</strong>hinking), a framework that enhances output stability by constraining the model's latent reasoning path. CAST combines (i) <em>Algorithmic Prompting</em> to impose a procedural scaffold over valid reasoning transitions and (ii) <em>Thinking-before-Speaking</em> to enforce explicit intermediate commitments before final generation. To measure progress, we introduce <strong>CAST-S</strong> and <strong>CAST-T</strong>, stability metrics for bulleted summarization and tagging, and validate their alignment with human judgments. Experiments across publicly available benchmarks on multiple LLM backbones show that CAST consistently achieves the best stability among all baselines, improving Stability Score by up to <strong>16.2%</strong>, while maintaining or improving output quality.
    </p>
  </div>

  <div class="project-section">
    <h2><i class="fas fa-star"></i> Highlights</h2>
    <ul class="project-highlights">
      <li>First systematic study of <strong>output stability</strong> in LLM-based text analysis for data analytics</li>
      <li>Novel <strong>CAST</strong> framework combining Algorithmic Prompting and Thinking-before-Speaking to constrain latent reasoning paths</li>
      <li>New stability metrics <strong>CAST-S</strong> and <strong>CAST-T</strong> for summarization and tagging, validated with human judgments</li>
      <li>Up to <strong>16.2% improvement</strong> in Stability Score across multiple LLM backbones while maintaining output quality</li>
    </ul>
  </div>

  <div class="project-section">
    <h2><i class="fas fa-quote-left"></i> BibTeX</h2>
    <div class="bibtex-box" id="bibtex">@inproceedings{xie2026cast,
  title={Achieving Stable LLM-based Text Analysis for Data Analytics},
  author={Xie, Jinxiang and Li, Zihao and He, Wei and Ding, Rui and Han, Shi and Zhang, Dongmei},
  booktitle={Findings of the 64th Annual Meeting of the Association for Computational Linguistics (ACL 2026)},
  year={2026}
}</div>
    <button class="bibtex-copy" onclick="navigator.clipboard.writeText(document.getElementById('bibtex').innerText);this.textContent='Copied!';setTimeout(()=>this.textContent='Copy',2000);">Copy</button>
  </div>

</div>
