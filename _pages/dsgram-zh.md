---
permalink: /zh/dsgram/
title: "DSGram"
author_profile: false
lang: zh
lang_alt: /dsgram/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">

<div class="project-container">

  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> AAAI 2025</div>
    <h1 class="project-title">DSGram：面向大语言模型时代语法纠错的动态加权子指标</h1>

    <p class="pp-hero-tagline">
      像 BLEU 这类基于参考的指标在 LLM 语法纠错系统上失效了。<strong>DSGram</strong> 提出一个动态加权框架与三个新子指标，<strong>显著更贴近人工判断</strong>。
    </p>

    <div class="project-authors">
      <a href="https://jxtse.github.io">谢锦祥</a><sup>1,2</sup>,
      李怡霖<sup>1</sup>,
      尹勋健<sup>1</sup>,
      <a href="https://wanxiaojun.github.io/">万小军</a><sup>1</sup>
    </div>
    <div class="affiliations">
      <sup>1</sup>北京大学 &nbsp;|&nbsp;
      <sup>2</sup>北京交通大学
    </div>

    <div class="links-bar">
      <a href="https://arxiv.org/abs/2412.12832" class="btn-arxiv" target="_blank"><i class="fas fa-file-alt"></i> 论文</a>
      <a href="https://arxiv.org/pdf/2412.12832" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <a href="https://github.com/jxtse/GEC-Metrics-DSGram" class="btn-code" target="_blank"><i class="fab fa-github"></i> 代码</a>
    </div>
  </header>

  <section class="teaser-section">
    <img src="{{ '/images/dsgram-fig2-architecture.png' | relative_url }}" alt="DSGram 框架结构" class="teaser-image">
    <div class="teaser-caption">
      <strong>图 1：</strong>DSGram 方法架构。输入为句对（原句与纠正句），LLM 生成动态权重，并通过判断矩阵与一致性检查精炼。归一化后的权重用于对子指标打分，最终得到整体评分。
    </div>
  </section>

  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> 摘要</div>
    <div class="abstract-text">
      评估语法纠错（GEC）模型变得越来越困难，因为基于 LLM 的 GEC 系统经常给出与黄金参考不一致的修改。这种偏差让传统基于参考的评估指标的可靠性大打折扣。
      <br><br>
      本工作提出一种新的 GEC 评估框架 <strong>DSGram</strong>，整合<strong>语义连贯性（Semantic Coherence）</strong>、<strong>修改程度（Edit Level）</strong> 与<strong>流畅度（Fluency）</strong>，并采用<strong>动态加权机制</strong>。我们用层次分析法（AHP）配合大语言模型来确定不同评估准则的相对重要性，并构建了一个包含人工标注与 LLM 模拟句子的数据集，用于验证算法和微调更经济的模型。
      <br><br>
      实验表明，本方法显著提升了 GEC 模型评估的有效性。
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">研究动机</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 20px;">
      传统 GEC 评估指标在面对 LLM 系统时存在明显短板。如下图所示，BLEU 无法区分过度修改与修改不足，SOME 则无法捕捉过度修改。DSGram 用一个综合性框架解决了这些问题。
    </p>
    <div class="figure-block">
      <img src="{{ '/images/dsgram-fig1-examples.png' | relative_url }}" alt="动机示例">
      <div class="figure-caption">
        <strong>图 2：</strong>现有指标在示例上的评估结果。BLEU 无法区分过度与不足修改，SOME 无法捕捉过度修改。蓝色为过度修改，红色为流畅度欠佳。
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">核心贡献</h2>
    <div class="pp-contrib-grid pp-fadeup-stagger">
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">01</div>
        <h3 class="pp-contrib-title">重新设计的子指标</h3>
        <p class="pp-contrib-text">引入面向 GEC 评估重新设计的三个子指标 —— <strong>语义连贯性</strong>、<strong>修改程度</strong>、<strong>流畅度</strong>，针对性地解决 LLM GEC 系统的过度修改问题。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">02</div>
        <h3 class="pp-contrib-title">基于 AHP 的动态加权</h3>
        <p class="pp-contrib-text">将 <strong>层次分析法（AHP）</strong> 与 LLM 结合，根据上下文动态确定各评估准则的相对重要性。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">03</div>
        <h3 class="pp-contrib-title">评估数据集</h3>
        <p class="pp-contrib-text">发布 <strong>DSGram-Eval</strong>（人工标注）与 <strong>DSGram-LLMs</strong>（GPT-4 模拟），均基于 CoNLL-2014 与 BEA-2019 测试集，便于严谨评估。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">04</div>
        <h3 class="pp-contrib-title">更高的相关性</h3>
        <p class="pp-contrib-text">在 SEEDA 基准上，DSGram 与人工评分的相关性<strong>超过所有传统基于参考与无参考的指标</strong>。</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">方法</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 25px;">
      DSGram 由两部分组成：<strong>分数生成</strong> 与 <strong>权重生成</strong>。将上下文相关的权重应用到生成的分数上，得到整体评估分。
    </p>

    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-chart-bar"></i> 三个子指标</h3>
        <p><strong>语义连贯性：</strong>原意被保留的程度。<strong>修改程度：</strong>修改是否必要、是否得当。<strong>流畅度：</strong>语法正确性与自然度。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-balance-scale"></i> 基于 AHP 的动态加权</h3>
        <p>用 LLM 为每个句子构造成对比较矩阵，配合一致性检查与特征向量归一化。正式文本侧重修改程度，口语文本侧重流畅度。</p>
      </div>
    </div>

    <div class="figure-block">
      <img src="{{ '/images/dsgram-fig5-score-computation.png' | relative_url }}" alt="分数计算">
      <div class="figure-caption">
        <strong>图 3：</strong>两种不同句子的 DSGram 分数计算。句 (a) 为口语化对话，更看重流畅度；句 (b) 为正式表达，修改程度权重更高。
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">子指标分析</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 20px;">
      我们重新设计了子指标以减少冗余、扩大覆盖。原 SOME 的 Grammaticality 与 Fluency 之间相关性高达 0.89；新子指标的相关性分布更均衡。
    </p>

    <div class="results-grid">
      <div class="result-item">
        <img src="{{ '/images/dsgram-fig3-heatmap-some.png' | relative_url }}" alt="SOME 热图" style="max-width: 100%; border-radius: 8px;">
        <div class="result-label" style="margin-top: 12px;"><strong>SOME 子指标：</strong>Grammaticality 与 Fluency 高度相关（0.89）</div>
      </div>
      <div class="result-item">
        <img src="{{ '/images/dsgram-fig4-heatmap-ours.png' | relative_url }}" alt="DSGram 热图" style="max-width: 100%; border-radius: 8px;">
        <div class="result-label" style="margin-top: 12px;"><strong>DSGram 子指标：</strong>相关性分布更均衡</div>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">结果</h2>

    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">0.8764</div>
        <div class="result-label">与人工评分的 Pearson 相关性（AHP 动态加权）</div>
      </div>
      <div class="result-item">
        <div class="result-number">0.8544</div>
        <div class="result-label">与人工评分的 Pearson 相关性（平均加权基线）</div>
      </div>
      <div class="result-item">
        <div class="result-number">12</div>
        <div class="result-label">在 SEEDA 基准上评估的 GEC 系统数</div>
      </div>
    </div>

    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-top: 25px;">
      DSGram 与人工反馈的相关性超过所有传统基于参考的指标（M²、ERRANT、BLEU）和无参考指标（GLEU、Scribendi Score）。在 DSGram-LLMs 数据集上微调的 LLaMA3-8B 与 LLaMA2-13B 也优于其 few-shot 版本，证明该框架在经济模型上同样可用。
    </p>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">引用</h2>
    <div class="bibtex-section">
      <button class="bibtex-copy-btn" onclick="navigator.clipboard.writeText(this.nextElementSibling.innerText);this.textContent='已复制!';setTimeout(()=>this.textContent='复制',2000);">复制</button>
      <div class="bibtex-code">@misc{xie2025dsgramdynamicweightingsubmetrics,
      title={DSGram: Dynamic Weighting Sub-Metrics for Grammatical Error Correction in the Era of Large Language Models},
      author={Jinxiang Xie and Yilin Li and Xunjian Yin and Xiaojun Wan},
      year={2025},
      eprint={2412.12832},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      doi={https://doi.org/10.1609/aaai.v39i24.34746},
      url={https://arxiv.org/abs/2412.12832},
}</div>
    </div>
  </section>

  <section class="project-section" style="margin-top: 50px; padding-top: 30px; border-top: 1px solid #e1e4e8;">
    <p style="font-size: 0.9em; color: #666; line-height: 1.6;">
      <strong>致谢：</strong>本工作完成于作者在北京大学实习期间。感谢万小军教授及王选计算机研究所同事的悉心指导与支持。
    </p>
  </section>

</div>

{% include project-page-enhance.html %}
