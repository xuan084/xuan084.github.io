---
permalink: /zh/dotabler/
title: "DoTabler"
author_profile: false
lang: zh
lang_alt: /dotabler/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">

<div class="project-container">

  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> ECAI 2025</div>
    <h1 class="project-title">从表层到语义：面向表格中心的文档结构语义解析</h1>
    <div class="project-subtitle">以表格为锚点，深入文档的上下文语义理解</div>

    <p class="pp-hero-tagline">
      现有的 PDF 解析方法停留在<em>表层</em>的版面分析与 OCR。<strong>DoTabler</strong> 再深一层 —— 以表格为锚点，找回与之语义关联的上下文段落，实现以表格为核心的文档解析与领域定向表格检索，并且<strong>比 GPT-4o 快两个数量级</strong>。
    </p>

    <div class="project-authors">
      <a href="https://xuan084.github.io"><strong>Xuan Li</strong></a>,
      Jialiang Dong<sup>*</sup>,
      Raymond Wong<sup>*</sup>
    </div>
    <div class="affiliations">
      新南威尔士大学，悉尼，澳大利亚 &nbsp;|&nbsp;
      <sup>*</sup>通讯作者
    </div>

    <div class="links-bar">
      <a href="#" class="btn-arxiv" target="_blank"><i class="fas fa-file-alt"></i> 论文</a>
      <a href="#" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <a href="https://github.com/xuan084/DoTabler2025" class="btn-code" target="_blank"><i class="fab fa-github"></i> 代码</a>
    </div>
  </header>

  <section class="teaser-section">
    <img src="{{ '/images/dotabler-pipeline.png' | relative_url }}" alt="DoTabler 总体工作流" class="teaser-image">
    <div class="teaser-caption">
      <strong>图 1：</strong>DoTabler 的总体工作流。文档结构预处理产出版面块；关系标注流水线构建表格–文本数据集；TTAM 在该数据上训练，并支撑下游两项能力 —— 表格中心的文档结构解析与领域定向表格检索。
    </div>
  </section>

  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> 摘要</div>
    <div class="abstract-text">
      文档是金融、医疗、科研等领域的核心信息载体，而表格是其中承载结构化数据的主要媒介。现有研究多聚焦于版面分析、表格检测、数据抽取等表层任务，缺乏对表格及其上下文关联的<em>深层语义解析</em>，这限制了跨段落数据解读、上下文一致性分析等高阶任务。
      <br><br>
      为此，我们提出 <strong>DoTabler</strong> —— 一个以表格为核心的语义级文档解析框架，致力于挖掘表格与上下文之间的深层语义关联。DoTabler 借助自建数据集与领域微调的预训练模型，串联起完整的解析流水线，识别出与每张表语义相关的上下文段落。在此基础上，DoTabler 实现两项核心能力：<strong>表格中心的文档结构解析</strong> 与 <strong>领域定向表格检索</strong>。
      <br><br>
      在来自真实 PDF、近 <strong>4,000 页、超过 1,000 张表</strong>的数据上评估，DoTabler 取得 <strong>超过 90% 的精确率与 F1</strong>，在表格–上下文语义分析任务上全面优于 GPT-4o、Gemini-2.0 与 Claude-3.5，并且<strong>速度快两个数量级</strong>。
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">两个应用场景</h2>
    <div class="figure-block">
      <img src="{{ '/images/dotabler-usecase-parsing.png' | relative_url }}" alt="表格中心解析示例">
      <div class="figure-caption">
        <strong>图 2a — 表格中心解析。</strong>给定一页 PDF，DoTabler 识别其中的表格块，并找回周围对该表进行描述或解释的段落。
      </div>
    </div>
    <div class="figure-block">
      <img src="{{ '/images/dotabler-usecase-retrieval.png' | relative_url }}" alt="领域定向表格检索示例">
      <div class="figure-caption">
        <strong>图 2b — 领域定向表格检索。</strong>给定一句自然语言查询，DoTabler 从文档中返回语义相关的表格及其上下文。
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">核心贡献</h2>
    <div class="pp-contrib-grid pp-fadeup-stagger">
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">01</div>
        <h3 class="pp-contrib-title">首个表格中心的语义级数据集</h3>
        <p class="pp-contrib-text">构建首个面向 PDF 表格中心结构的语义级数据集，并训练 <strong>表格–文本关联模型 TTAM</strong>，对表格与上下文的细粒度关联进行建模。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">02</div>
        <h3 class="pp-contrib-title">DoTabler 框架</h3>
        <p class="pp-contrib-text">端到端流水线整合了预处理（分页、版面、OCR）与 TTAM，在同一框架内同时实现 <strong>文档结构解析</strong> 与 <strong>领域定向表格检索</strong>。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">03</div>
        <h3 class="pp-contrib-title">大规模真实评估</h3>
        <p class="pp-contrib-text">在来自 arXiv 与 PubMed Central 的近 <strong>4,000 页、1,000+ 张表格</strong>上评估，准确率全面超过 GPT-4o、Gemini-2.0、Claude-3.5，并且<em>快出数量级</em>。</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">方法</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 25px;">
      DoTabler 把表格中心的语义解析拆成三段式流水线，每个模块都可替换 —— 可以换用更强的预训练编码器，也可以扩展到新的文档领域。
    </p>

    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-cogs"></i> 1. 文档结构预处理</h3>
        <p>每个 PDF 被渲染为图片、按页切分，送入在 <code>PubLayNet</code> 上微调的 Faster R-CNN 进行版面检测；Tesseract OCR 抽取 <em>Text</em>、<em>List</em>、<em>Title</em>、<em>Table</em> 块的文字。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-link"></i> 2. 表格–文本关联模型（TTAM）</h3>
        <p>基于预训练编码器（BERT / BART / RoBERTa）的 sentence-pair 二分类器。对每对 <code>(table, text)</code>，TTAM 输出"相关 / 无关"，使用平衡的正负样本与交叉熵损失训练。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-stream"></i> 3a. 表格中心的语义解析</h3>
        <p>遍历文档中每张 Table 块，TTAM 对所有候选 Text/List 块打分，输出与该表语义相关的子集，得到一份结构化的 <code>(table, related_paragraphs)</code> 视图。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-search"></i> 3b. 领域定向表格检索</h3>
        <p>用微调后的 RoBERTa cross-encoder 联合编码 <code>(query, table)</code>，输出相关性得分，按分排序后返回 top-K 表及其上下文。训练采用 margin-based ranking loss。</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">数据集与实验设置</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 20px;">
      该任务此前没有公开数据集，因此我们自建了首个表格中心的语义级标注数据。文档来自 arXiv 与 PubMed Central；两位资深标注员独立标注表格–文本关联，对分歧通过专家共识机制对齐。
    </p>

    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">227</div>
        <div class="result-label">PDF（arXiv + PubMed Central）</div>
      </div>
      <div class="result-item">
        <div class="result-number">3,952</div>
        <div class="result-label">页 · 解析并标注</div>
      </div>
      <div class="result-item">
        <div class="result-number">1,061</div>
        <div class="result-label">表格块 · 1,624 文本块</div>
      </div>
    </div>

    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 25px;">
      <strong>数据划分。</strong>TTAM 评估：3,248 个均衡的表格–文本对，按 7:3 划分为 2,273 训练 / 975 测试。检索评估：200 个查询–表格对，过滤不完整样本后得到 129 训练 / 53 测试。<strong>基线。</strong>GPT-4o、Gemini-2.0 Flash、Claude-3.5，使用相同任务提示以保证公平比较。
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">结果</h2>

    <h3 style="margin-top: 8px; margin-bottom: 14px;">表格–文本关联分类（TTAM）</h3>
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">90.01%</div>
        <div class="result-label">F1（基于 RoBERTa 的 TTAM）</div>
      </div>
      <div class="result-item">
        <div class="result-number">+10 分</div>
        <div class="result-label">高出最强 LLM 基线（Gemini-2.0）</div>
      </div>
      <div class="result-item">
        <div class="result-number">+41 分</div>
        <div class="result-label">高出 GPT-4o（48.48 → 90.01）</div>
      </div>
    </div>

    <h3 style="margin-top: 32px; margin-bottom: 14px;">文档级解析与检索效果</h3>
    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">128 / 193</div>
        <div class="result-label">完全正确的文档数（LLM 基线为 109–114）</div>
      </div>
      <div class="result-item">
        <div class="result-number">71.7%</div>
        <div class="result-label">检索 Recall@1（K=3 时为 88.7%）</div>
      </div>
      <div class="result-item">
        <div class="result-number">~270×</div>
        <div class="result-label">比 GPT-4o 快（0.0035s vs 0.80s）</div>
      </div>
    </div>

    <div class="figure-block" style="margin-top: 28px;">
      <img src="{{ '/images/dotabler-latency.png' | relative_url }}" alt="时延对比">
      <div class="figure-caption">
        <strong>图 3：</strong>每对 (table, text) 的平均与中位耗时，跨 10 个均匀划分的测试组。DoTabler 始终贴近零线，三个 LLM 基线则在 0.6–1.7 秒之间波动。
      </div>
    </div>

    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 25px;">
      <strong>为何 DoTabler 胜出。</strong>解码器为主的 LLM 偏向流畅生成，决策上趋于保守 —— 精确率尚可但漏判很多真实关联。RoBERTa 的双向编码器在新数据集上微调后，能更好地刻画细粒度上下文依赖，对幻觉也更鲁棒，正中此任务的核心。
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">引用</h2>
    <div class="bibtex-section">
      <button class="bibtex-copy-btn" onclick="navigator.clipboard.writeText(this.nextElementSibling.innerText);this.textContent='已复制!';setTimeout(()=>this.textContent='复制',2000);">复制</button>
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
      <strong>致谢：</strong>本工作完成于新南威尔士大学。感谢标注员在表格–文本关联数据集构建过程中的细致工作。
    </p>
  </section>

</div>

{% include project-page-enhance.html %}
