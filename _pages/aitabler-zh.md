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
    <h2 class="section-title">项目介绍</h2>
    <p style="font-size: 1.05em; line-height: 1.75; color: #444;">
      真实文档中的表格很少能够脱离上下文独立被理解。表格里可能包含关键数值，但 caption、周围段落、指标定义、实验设置、假设条件和解释性评论往往散落在页面其他位置。对于金融报告、科研论文和政策文档来说，这不是简单的版面问题，而是直接决定系统能否正确解释证据的核心问题。
    </p>
    <p style="font-size: 1.05em; line-height: 1.75; color: #444;">
      <strong>AITabler</strong> 正是为这个场景设计的。它不再把表格和附近文本粗略地判断为"相关 / 不相关"，而是进一步追问：<em>这段文本与这张表之间究竟是哪一种语义关系？</em> 系统首先重建 PDF 版面结构，检索空间相关的上下文，然后用五级语义层次对表格-文本关系进行分级。这些细粒度关联进一步支撑表格中心的文档理解与下游 Table-QA。
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">五级语义层次</h2>
    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-quote-right"></i> L1. Caption Reference</h3>
        <p>文本通过表题或显式引用直接指向该表，例如 "as shown in Table 3"。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-table-cells"></i> L2. Content Alignment</h3>
        <p>文本讨论表格 body-cell 中的具体数值、比较、趋势或可追溯到表格的结果。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-tags"></i> L3. Topical Match</h3>
        <p>文本与行列标题、数据集、指标、方法或 schema-level 概念存在主题重合。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-circle-nodes"></i> L4. Peripheral Context</h3>
        <p>文本在语义上相关，但不满足 L1-L3 的结构性标准，例如背景信息或方法上下文。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-ban"></i> L5. Unrelated</h3>
        <p>文本与表格没有可识别的语义关系，不应被注入下游推理过程。</p>
      </div>
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
    <h2 class="section-title">资源状态</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444;">
      Camera-ready PDF 现在已经可以访问。正式论文页面和海报发布后，我会把它们链接到这里；因此目前 <strong>论文</strong> 和 <strong>海报</strong> 按钮会先以 coming soon 的灰色状态显示。
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
