---
permalink: /zh/aitabler/
title: "AITabler"
author_profile: false
lang: zh
lang_alt: /aitabler/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">

<div class="project-container">

  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> ICDAR 2026</div>
    <h1 class="project-title">结构承载语义：面向表格中心文档的细粒度语义解析</h1>
    <div class="project-subtitle">面向可靠文档理解的细粒度表格-文本语义对齐</div>

    <p class="pp-hero-tagline">
      表格承载着财务报告、风险评估与政策分析中的关键定量证据，但其真正含义往往隐藏在周围文本中。<strong>AITabler</strong> 将表格-文本关系建模为<strong>五级语义层次</strong>，结合 PDF 结构重建、版面感知上下文检索与基于 LLM 的语义推理，实现表格中心的文档解析与问答。
    </p>

    <div class="project-authors">
      <a href="https://xuan084.github.io"><strong>Xuan Li</strong></a>,
      Mengfei Xiao,
      Jingtian Wei,
      Jialiang Dong,
      Raymond Wong<sup>*</sup>
    </div>
    <div class="affiliations">
      新南威尔士大学，澳大利亚 &nbsp;|&nbsp;
      悉尼科技大学，澳大利亚 &nbsp;|&nbsp;
      伍伦贡大学，澳大利亚 &nbsp;|&nbsp;
      <sup>*</sup>通讯作者
    </div>

    <div class="links-bar">
      <span class="btn-arxiv btn-disabled"><i class="fas fa-file-alt"></i> 论文</span>
      <a href="/files/aitabler-paper.pdf" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <span class="btn-pdf btn-disabled"><i class="fas fa-image"></i> 海报</span>
      <a href="https://github.com/xuan084/Meaning-Lies-in-Structure-Fine-Grained-Table-Centric-Document-Semantic-Parsing" class="btn-code" target="_blank"><i class="fab fa-github"></i> 代码</a>
    </div>
  </header>

  <section class="teaser-section">
    <img src="{{ '/images/aitabler-thumb.png' | relative_url }}" alt="AITabler 总体工作流" class="teaser-image">
    <div class="teaser-caption">
      <strong>图 1：</strong>AITabler 的总体工作流。系统重建 PDF 文档结构，检索版面感知的空间上下文，进行细粒度表格-文本语义相关性分级，并利用识别出的关联提升下游表格问答能力。
    </div>
  </section>

  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> 摘要</div>
    <div class="abstract-text">
      表格在财务报告、风险评估和政策分析中承载关键定量证据。在这些场景中，自动化分析的可靠性依赖于表格数据与解释性文本之间准确的语义整合；一旦关联错位，就可能扭曲解释结果和下游决策。
      <br><br>
      现有 PDF 表格研究主要关注视觉结构恢复，而对文档组件之间的细粒度语义对齐关注不足。为弥补这一空白，我们将表格-文本语义对齐形式化为一个<strong>五级层次框架</strong>，并提出端到端系统 <strong>AITabler</strong>，整合 PDF 结构重建、版面感知空间上下文建模与基于 LLM 的语义推理。
      <br><br>
      我们构建了两个 benchmark：包含 <strong>29,138 个标注样本对</strong>的细粒度相关性语料库，以及包含 <strong>6,000 个问题</strong>的 Table-QA 数据集，二者来自超过 <strong>3,000 页 PDF 文档</strong>。实验表明，AITabler 在相关性分级和下游 Table-QA 中均带来稳定提升。
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">核心贡献</h2>
    <div class="pp-contrib-grid pp-fadeup-stagger">
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">01</div>
        <h3 class="pp-contrib-title">五级语义对齐框架</h3>
        <p class="pp-contrib-text">将表格-文本关系建模为层次结构，覆盖 caption reference、content alignment、topical match、contextual relevance 与 unrelated context，突破粗粒度二分类相关性。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">02</div>
        <h3 class="pp-contrib-title">端到端 AITabler 流水线</h3>
        <p class="pp-contrib-text">AITabler 结合 PDF 结构重建、空间上下文检索与基于 LLM 的推理，在文档级别恢复表格与文本之间的语义关联。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">03</div>
        <h3 class="pp-contrib-title">解析与问答 benchmark</h3>
        <p class="pp-contrib-text">构建细粒度表格-文本相关性语料库与专门设计的 Table-QA 数据集，支持可复现的表格中心文档分析研究。</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">方法</h2>
    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-sitemap"></i> 1. 文档结构重建</h3>
        <p>将 PDF 页面解析为版面块，使表格、标题、段落等组件能够以结构化方式表示。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-map-marker-alt"></i> 2. 空间上下文检索</h3>
        <p>利用版面空间线索检索候选上下文段落，在语义分级前缩小搜索空间。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-layer-group"></i> 3. 五级相关性分级</h3>
        <p>通过基于 LLM 的推理，将每个表格-文本对分到五个相关性等级之一，得到比"相关/无关"更细的语义关联。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-question-circle"></i> 4. 语义增强 Table-QA</h3>
        <p>识别出的高价值上下文被用于下游表格问答，在避免无关段落噪声的同时提升回答准确率。</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">数据集与结果</h2>
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">29,138</div>
        <div class="result-label">标注的表格-文本样本对</div>
      </div>
      <div class="result-item">
        <div class="result-number">6,000</div>
        <div class="result-label">Table-QA 问题</div>
      </div>
      <div class="result-item">
        <div class="result-number">3,000+</div>
        <div class="result-label">用于构建 benchmark 的 PDF 页面</div>
      </div>
    </div>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 22px;">
      实验显示，AITabler 在强相关样本上准确率超过 <strong>98%</strong>，在弱相关样本上超过 <strong>75%</strong>，并在复杂 QA 任务上达到超过 <strong>70%</strong> 的准确率，显著优于粗粒度检索基线。
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">引用</h2>
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
