---
permalink: /zh/cast/
title: "CAST"
author_profile: false
lang: zh
lang_alt: /cast/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">

<div class="project-container">

  <header class="project-header">
    <div class="project-venue-badge"><i class="fas fa-award"></i> ACL 2026 Findings</div>
    <h1 class="project-title">CAST：面向数据分析的稳定 LLM 文本分析方法</h1>
    <div class="project-subtitle">基于算法化提示与稳定思维的输出一致性框架</div>

    <p class="pp-hero-tagline">
      LLM 做文本分析时跑两次结果不一样 —— 这对数据分析是致命伤。<strong>CAST</strong> 通过约束模型的潜在推理路径，在不牺牲质量的前提下提供接近确定性的稳定输出。
    </p>

    <div class="project-authors">
      <a href="https://jxtse.github.io">谢锦祥</a><sup>1</sup>,
      李子豪<sup>2</sup>,
      何威<sup>3</sup>,
      丁睿<sup>4</sup>,
      韩石<sup>4</sup>,
      张冬梅<sup>4</sup>
    </div>
    <div class="affiliations">
      <sup>1</sup>南京大学 &nbsp;|&nbsp;
      <sup>2</sup>清华大学 &nbsp;|&nbsp;
      <sup>3</sup>北京大学 &nbsp;|&nbsp;
      <sup>4</sup>微软亚洲研究院
    </div>

    <div class="links-bar">
      <a href="https://arxiv.org/abs/2602.15861" class="btn-arxiv" target="_blank"><i class="fas fa-file-alt"></i> 论文</a>
      <a href="https://arxiv.org/pdf/2602.15861" class="btn-pdf" target="_blank"><i class="fas fa-file-pdf"></i> PDF</a>
      <a href="https://github.com/jxtse/CAST-text-analysis" class="btn-code" target="_blank"><i class="fab fa-github"></i> 代码</a>
    </div>
  </header>

  <section class="teaser-section">
    <img src="{{ '/images/cast-fig2-framework.png' | relative_url }}" alt="CAST 框架总览" class="teaser-image">
    <div class="teaser-caption">
      <strong>图 1：</strong>CAST 框架总览。传统方法（左）推理路径不受约束，输出分布宽且高熵；CAST（右）通过算法化提示与"先想后说"将生成过程压缩为高度集中的输出分布。
    </div>
  </section>

  <section class="abstract-section">
    <div class="abstract-title"><i class="fas fa-align-left"></i> 摘要</div>
    <div class="abstract-text">
      表格数据的文本分析依赖两个核心操作：用于语料级主题抽取的 <strong>summarization（摘要）</strong> 和用于行级标签的 <strong>tagging（打标）</strong>。直接用大语言模型（LLM）做这两件事的核心障碍是：它们的<em>输出稳定性</em>无法满足数据分析对一致性的高要求。
      <br><br>
      为此我们提出 <strong>CAST</strong>（<strong>C</strong>onsistency via <strong>A</strong>lgorithmic Prompting and <strong>S</strong>table <strong>T</strong>hinking），一个通过约束模型潜在推理路径来增强输出稳定性的框架。CAST 由两部分组成：（i）<strong>算法化提示（Algorithmic Prompting）</strong>，为合法的推理转移提供过程式骨架；（ii）<strong>先想后说（Thinking-before-Speaking）</strong>，强制模型在最终生成前显式承诺中间状态。
      <br><br>
      为衡量进展，我们提出了 <strong>CAST-S</strong> 和 <strong>CAST-T</strong> 两个针对要点式摘要和打标的稳定性指标，并验证了它们与人工判断的一致性。在多个公开基准与 LLM 主干上的实验表明，CAST 在所有基线中取得了最佳稳定性，Stability Score 最高提升 <strong>16.2%</strong>，同时保持甚至提升了输出质量。
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">核心贡献</h2>
    <div class="pp-contrib-grid pp-fadeup-stagger">
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">01</div>
        <h3 class="pp-contrib-title">TADA 范式的形式化</h3>
        <p class="pp-contrib-text">我们将"面向数据分析的文本分析（TADA）"形式化为以表格为中心的范式，强调将概率性 LLM 输出接入确定性 OLAP 工作流时，<strong>稳定性是功能性必要条件</strong>。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">02</div>
        <h3 class="pp-contrib-title">CAST 框架</h3>
        <p class="pp-contrib-text">通过<strong>算法化提示</strong>与中间状态承诺约束生成，在不依赖昂贵搜索方法的情况下降低潜在路径熵。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">03</div>
        <h3 class="pp-contrib-title">稳定性评估指标</h3>
        <p class="pp-contrib-text">提出 <strong>CAST-S</strong> 与 <strong>CAST-T</strong>，结合语义匹配与顺序敏感（Kendall's Tau），更贴近人类感知的一致性判断。</p>
      </div>
      <div class="pp-contrib-card">
        <div class="pp-contrib-num">04</div>
        <h3 class="pp-contrib-title">实证效果显著</h3>
        <p class="pp-contrib-text">在多个 LLM 主干上 Stability Score 最高提升 <strong>16.2%</strong>，准确率不退化。</p>
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">方法</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 25px;">
      CAST 通过两个互补机制约束 LLM 的潜在推理轨迹，从而缓解不稳定问题：
    </p>

    <div class="method-grid">
      <div class="method-card">
        <h3><i class="fas fa-sitemap"></i> 算法化提示</h3>
        <p>为任务指定一个算法骨架，把传统的确定性工作流翻译成结构化的提示序列。该骨架作为对合法推理转移的强先验，有效裁剪掉高熵路径。</p>
      </div>
      <div class="method-card">
        <h3><i class="fas fa-brain"></i> 先想后说</h3>
        <p>强制模型在产出最终结果前先明确写出中间状态（领域、主题模式、聚类等）。通过对这些状态的承诺，模型沿着更稳定的推理路径前进。</p>
      </div>
    </div>

    <div class="figure-block">
      <img src="{{ '/images/cast-fig1-tada.png' | relative_url }}" alt="TADA 操作示意">
      <div class="figure-caption">
        <strong>图 2：</strong>TADA 中 summarization 与 tagging 操作的示意。这两个原子操作可以在更复杂的 TADA 任务中被组合复用。
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">实证观察</h2>
    <p style="font-size: 1.05em; line-height: 1.7; color: #444; margin-bottom: 20px;">
      实验显示，要求模型先生成相关的中间状态会显著锐化输出分布。如下图所示，CAST 产出的分布最尖锐、最集中，意味着多次运行之间的稳定性大幅提升。
    </p>

    <div class="figure-block">
      <img src="{{ '/images/cast-fig3-kde.png' | relative_url }}" alt="输出长度稳定性">
      <div class="figure-caption">
        <strong>图 3：</strong>不同提示策略下的输出长度稳定性。KDE 平滑后的摘要长度分布对比：(i) 直接提示，(ii) 不相关中间状态，(iii) 相关中间状态，(iv) 完整 CAST 提示。CAST 给出的分布最尖锐，输出紧密聚集在一个中心值附近。
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">结果</h2>

    <div class="results-grid">
      <div class="result-item">
        <div class="result-number">16.2%</div>
        <div class="result-label">Stability Score 最大提升</div>
      </div>
      <div class="result-item">
        <div class="result-number">32</div>
        <div class="result-label">数据集–查询对评估</div>
      </div>
      <div class="result-item">
        <div class="result-number">5,100+</div>
        <div class="result-label">覆盖 4 个领域的样本数</div>
      </div>
    </div>

    <div class="figure-block">
      <img src="{{ '/images/cast-fig4-tagging.png' | relative_url }}" alt="打标流水线">
      <div class="figure-caption">
        <strong>图 4：</strong>打标任务的 CAST 流水线。从查询分解与领域识别开始，引导核心算法化提示阶段，最终由输出验证收尾。
      </div>
    </div>
  </section>

  <section class="project-section pp-fadeup">
    <h2 class="section-title">引用</h2>
    <div class="bibtex-section">
      <button class="bibtex-copy-btn" onclick="navigator.clipboard.writeText(this.nextElementSibling.innerText);this.textContent='已复制!';setTimeout(()=>this.textContent='复制',2000);">复制</button>
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

  <section class="project-section" style="margin-top: 50px; padding-top: 30px; border-top: 1px solid #e1e4e8;">
    <p style="font-size: 0.9em; color: #666; line-height: 1.6;">
      <strong>致谢：</strong>本工作完成于作者在微软亚洲研究院实习期间。感谢 DKI 组所有同事与导师的支持与宝贵反馈。
    </p>
  </section>

</div>

{% include project-page-enhance.html %}
