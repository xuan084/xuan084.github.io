---
permalink: /zh/skills/
title: "科研技能库"
author_profile: false
lang: zh
lang_alt: /skills/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link rel="stylesheet" href="{{ '/assets/css/project-page.css' | relative_url }}">
<link rel="stylesheet" href="{{ '/assets/css/skills-page.css' | relative_url }}">

<div class="project-container srs-page">

  <!-- =========================== HERO =========================== -->
  <header class="srs-hero srs-hero--video">
    <div class="srs-hero-video-wrap">
      <img
        class="srs-hero-video"
        src="{{ '/assets/videos/skills-hero-poster.jpg' | relative_url }}"
        alt="科研技能库 —— 6 个由工作流串联起来的 skill"
        loading="eager">
      <div class="srs-hero-video-fade"></div>
    </div>

    <div class="srs-hero-overlay">
      <p class="srs-hero-tagline">
        面向 AI 编码 Agent 的高阶研究方法论技能库。<br>
        <em>不是又一份工具清单 —— 每个 skill 封装了一套花数月才能内化的研究工作流。</em>
      </p>

      <div class="srs-hero-stats">
        <a class="srs-stat" href="https://github.com/jxtse/scientific-research-skills" target="_blank" rel="noopener">
          <i class="fab fa-github"></i> jxtse/scientific-research-skills
        </a>
        <span class="srs-stat">
          <img src="https://img.shields.io/github/stars/jxtse/scientific-research-skills?style=flat-square&label=Stars&color=181717" alt="GitHub stars">
        </span>
        <span class="srs-stat">
          <img src="https://img.shields.io/github/last-commit/jxtse/scientific-research-skills?style=flat-square&label=Updated&color=2980b9" alt="Last commit">
        </span>
      </div>

      <div class="srs-hero-cta">
        <a href="#install" class="srs-btn srs-btn-primary"><i class="fas fa-download"></i> 安装</a>
        <a href="#skills-grid" class="srs-btn srs-btn-ghost"><i class="fas fa-th"></i> 浏览 6 个 skill</a>
        <a href="#workflow" class="srs-btn srs-btn-ghost"><i class="fas fa-project-diagram"></i> 查看工作流</a>
        <a href="https://github.com/jxtse/scientific-research-skills" target="_blank" rel="noopener" class="srs-btn srs-btn-ghost"><i class="fab fa-github"></i> GitHub</a>
      </div>
    </div>
  </header>

  <!-- =========================== PHILOSOPHY =========================== -->
  <section class="srs-philosophy srs-fadeup">
    <div class="srs-pull-quote">
      <i class="fas fa-quote-left"></i>
      现有 AI-for-research 仓库罗列的是数百个<strong>工具</strong>。本仓库编码的是经验丰富的研究者花数年内化的<strong>决策过程</strong> —— <em>什么时候</em>该速读、什么时候该精读，<em>如何</em>定位贡献，<em>哪个</em>引擎适合哪种查询。
    </div>
    <div class="srs-principles">
      <div class="srs-principle"><i class="fas fa-robot"></i><span><strong>面向 AI，不为展示</strong> —— 写法即 agent 指令</span></div>
      <div class="srs-principle"><i class="fas fa-layer-group"></i><span><strong>方法论 &gt; 工具调用</strong> —— 高阶优先</span></div>
      <div class="srs-principle"><i class="fas fa-puzzle-piece"></i><span><strong>模块化</strong> —— 按需安装</span></div>
      <div class="srs-principle"><i class="fas fa-globe"></i><span><strong>跨平台</strong> —— OpenClaw / Claude Code / Codex</span></div>
    </div>
  </section>

  <!-- =========================== SKILLS GRID =========================== -->
  <section id="skills-grid" class="srs-section">
    <h2 class="srs-section-title"><i class="fas fa-th-large"></i> 六个核心 Skill</h2>
    <p class="srs-section-sub">
      <span class="srs-tag srs-tag-tool"><i class="fas fa-plug"></i> 工具集成型</span> 需要外部 API &nbsp;·&nbsp;
      <span class="srs-tag srs-tag-method"><i class="fas fa-book"></i> 方法论型</span> 纯工作流、无依赖
    </p>

    <div class="srs-grid srs-fadeup-stagger">

      <a class="srs-card" href="https://github.com/jxtse/scientific-research-skills/tree/main/skills/literature-search" target="_blank" rel="noopener">
        <div class="srs-card-head">
          <div class="srs-card-icon" style="background:#e8f0fe;color:#1967d2"><i class="fas fa-search"></i></div>
          <span class="srs-tag srs-tag-tool">工具集成型</span>
        </div>
        <h3 class="srs-card-title">literature-search</h3>
        <p class="srs-card-desc">多引擎学术检索，自适应选择 Semantic Scholar、arXiv、Tavily、Exa、Gemini、AMiner。</p>
        <div class="srs-card-foot">
          <span class="srs-chip">Semantic Scholar</span>
          <span class="srs-chip">arXiv</span>
          <span class="srs-chip">Tavily / Exa</span>
          <span class="srs-chip">Gemini</span>
        </div>
      </a>

      <a class="srs-card" href="https://github.com/jxtse/scientific-research-skills/tree/main/skills/paper-reading" target="_blank" rel="noopener">
        <div class="srs-card-head">
          <div class="srs-card-icon" style="background:#e6f4ea;color:#137333"><i class="fas fa-book-open"></i></div>
          <span class="srs-tag srs-tag-method">方法论型</span>
        </div>
        <h3 class="srs-card-title">paper-reading</h3>
        <p class="srs-card-desc">三级阅读工作流（速读 2 分钟 → 标准 10 分钟 → 精读 30 分钟），输出包含隐含假设与可复现性备注的结构化笔记。</p>
        <div class="srs-card-foot">
          <span class="srs-chip">速读</span>
          <span class="srs-chip">标准</span>
          <span class="srs-chip">精读</span>
        </div>
      </a>

      <a class="srs-card" href="https://github.com/jxtse/scientific-research-skills/tree/main/skills/social-media-paper-triage" target="_blank" rel="noopener">
        <div class="srs-card-head">
          <div class="srs-card-icon" style="background:#fce8e6;color:#c5221f"><i class="fas fa-bullhorn"></i></div>
          <span class="srs-tag srs-tag-tool">工具集成型</span>
        </div>
        <h3 class="srs-card-title">social-media-paper-triage</h3>
        <p class="srs-card-desc">从小红书 / 微信公众号 / Twitter / Bilibili 提取论文推荐 → 找到 arXiv 原文 → 在收藏前判断相关性。</p>
        <div class="srs-card-foot">
          <span class="srs-chip">小红书</span>
          <span class="srs-chip">微信</span>
          <span class="srs-chip">Twitter/X</span>
          <span class="srs-chip">Jina Reader</span>
        </div>
      </a>

      <a class="srs-card" href="https://github.com/jxtse/scientific-research-skills/tree/main/skills/related-work-survey" target="_blank" rel="noopener">
        <div class="srs-card-head">
          <div class="srs-card-icon" style="background:#fef7e0;color:#b06000"><i class="fas fa-sitemap"></i></div>
          <span class="srs-tag srs-tag-method">方法论型</span>
        </div>
        <h3 class="srs-card-title">related-work-survey</h3>
        <p class="srs-card-desc">系统性综述：定义维度 → 按轴检索 → 构建分类法 → 找出 gap → 产出 Related Work 章节的定位叙事。</p>
        <div class="srs-card-foot">
          <span class="srs-chip">分类法</span>
          <span class="srs-chip">空白分析</span>
          <span class="srs-chip">定位叙事</span>
        </div>
      </a>

      <a class="srs-card" href="https://github.com/jxtse/scientific-research-skills/tree/main/skills/zotero-management" target="_blank" rel="noopener">
        <div class="srs-card-head">
          <div class="srs-card-icon" style="background:#f3e8fd;color:#8430ce"><i class="fas fa-book-bookmark"></i></div>
          <span class="srs-tag srs-tag-tool">工具集成型</span>
        </div>
        <h3 class="srs-card-title">zotero-management</h3>
        <p class="srs-card-desc">通过本地 + Web API 进行结构化文献管理：Inbox / 进行中项目 / 背景资料 / 阅读队列 / 归档，含项目、状态、优先级标签。</p>
        <div class="srs-card-foot">
          <span class="srs-chip">Zotero 本地</span>
          <span class="srs-chip">Web API</span>
          <span class="srs-chip">标签体系</span>
        </div>
      </a>

      <a class="srs-card" href="https://github.com/jxtse/scientific-research-skills/tree/main/skills/academic-figure-generation" target="_blank" rel="noopener">
        <div class="srs-card-head">
          <div class="srs-card-icon" style="background:#fff1e6;color:#c2410c"><i class="fas fa-image"></i></div>
          <span class="srs-tag srs-tag-tool">工具集成型</span>
        </div>
        <h3 class="srs-card-title">academic-figure-generation</h3>
        <p class="srs-card-desc">通过多 agent 流水线（PaperBanana）从方法描述生成可发表级图表，输出 ACL / NeurIPS / ICML / EMNLP 投稿可用的 PNG/PDF。</p>
        <div class="srs-card-foot">
          <span class="srs-chip">PaperBanana</span>
          <span class="srs-chip">多 agent</span>
          <span class="srs-chip">投稿可用</span>
        </div>
      </a>

    </div>
  </section>

  <!-- =========================== WORKFLOW DIAGRAM =========================== -->
  <section id="workflow" class="srs-section">
    <h2 class="srs-section-title"><i class="fas fa-project-diagram"></i> 各 Skill 如何组合</h2>
    <p class="srs-section-sub">一次端到端的研究 session 通常会按顺序用上其中 4–6 个。</p>

    <div class="srs-flow-wrap srs-fadeup">
      <svg viewBox="0 0 1100 520" class="srs-flow" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <marker id="srs-arrow-zh" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
            <path d="M 0 0 L 10 5 L 0 10 z" fill="#5b6b7d"/>
          </marker>
          <linearGradient id="srs-grad-input-zh" x1="0" x2="1" y1="0" y2="1">
            <stop offset="0%" stop-color="#dbe9ff"/>
            <stop offset="100%" stop-color="#b6d2ff"/>
          </linearGradient>
          <linearGradient id="srs-grad-process-zh" x1="0" x2="1" y1="0" y2="1">
            <stop offset="0%" stop-color="#fff4d6"/>
            <stop offset="100%" stop-color="#ffe39a"/>
          </linearGradient>
          <linearGradient id="srs-grad-output-zh" x1="0" x2="1" y1="0" y2="1">
            <stop offset="0%" stop-color="#d8f5e3"/>
            <stop offset="100%" stop-color="#a5e8c0"/>
          </linearGradient>
        </defs>

        <text x="110" y="36" class="srs-stage-label">发现</text>
        <text x="475" y="36" class="srs-stage-label">理解</text>
        <text x="840" y="36" class="srs-stage-label">整理与产出</text>

        <line x1="330" y1="55" x2="330" y2="495" stroke="#e3e9f0" stroke-dasharray="4 6"/>
        <line x1="700" y1="55" x2="700" y2="495" stroke="#e3e9f0" stroke-dasharray="4 6"/>

        <g class="srs-node">
          <rect x="40" y="100" width="260" height="80" rx="14" fill="url(#srs-grad-input-zh)" stroke="#3b82f6"/>
          <text x="170" y="135" class="srs-node-title">social-media-paper-triage</text>
          <text x="170" y="158" class="srs-node-sub">小红书 / 微信 / Twitter → arXiv</text>
        </g>
        <g class="srs-node">
          <rect x="40" y="220" width="260" height="80" rx="14" fill="url(#srs-grad-input-zh)" stroke="#3b82f6"/>
          <text x="170" y="255" class="srs-node-title">literature-search</text>
          <text x="170" y="278" class="srs-node-sub">多引擎论文检索</text>
        </g>
        <g class="srs-node">
          <rect x="40" y="340" width="260" height="80" rx="14" fill="url(#srs-grad-input-zh)" stroke="#3b82f6"/>
          <text x="170" y="375" class="srs-node-title">related-work-survey</text>
          <text x="170" y="398" class="srs-node-sub">定义维度 → 分类法</text>
        </g>

        <g class="srs-node">
          <rect x="410" y="220" width="260" height="80" rx="14" fill="url(#srs-grad-process-zh)" stroke="#d97706"/>
          <text x="540" y="255" class="srs-node-title">paper-reading</text>
          <text x="540" y="278" class="srs-node-sub">三级笔记（速读 / 标准 / 精读）</text>
        </g>

        <g class="srs-node">
          <rect x="780" y="160" width="260" height="80" rx="14" fill="url(#srs-grad-output-zh)" stroke="#15803d"/>
          <text x="910" y="195" class="srs-node-title">zotero-management</text>
          <text x="910" y="218" class="srs-node-sub">分类、打标、入队</text>
        </g>
        <g class="srs-node">
          <rect x="780" y="280" width="260" height="80" rx="14" fill="url(#srs-grad-output-zh)" stroke="#15803d"/>
          <text x="910" y="315" class="srs-node-title">academic-figure-generation</text>
          <text x="910" y="338" class="srs-node-sub">投稿级图表（PaperBanana）</text>
        </g>

        <path d="M 300 140 C 360 140, 380 230, 410 250" fill="none" stroke="#5b6b7d" stroke-width="2" marker-end="url(#srs-arrow-zh)"/>
        <path d="M 300 260 L 410 260" fill="none" stroke="#5b6b7d" stroke-width="2" marker-end="url(#srs-arrow-zh)"/>
        <path d="M 300 380 C 360 380, 380 290, 410 270" fill="none" stroke="#5b6b7d" stroke-width="2" marker-end="url(#srs-arrow-zh)"/>

        <path d="M 670 250 C 730 230, 740 200, 780 200" fill="none" stroke="#5b6b7d" stroke-width="2" marker-end="url(#srs-arrow-zh)"/>
        <path d="M 670 270 C 730 290, 740 320, 780 320" fill="none" stroke="#5b6b7d" stroke-width="2" marker-end="url(#srs-arrow-zh)"/>

        <path d="M 780 180 C 600 60, 200 60, 110 220" fill="none" stroke="#94a3b8" stroke-width="1.6" stroke-dasharray="5 5" marker-end="url(#srs-arrow-zh)"/>
        <text x="540" y="82" class="srs-edge-label">阅读队列回流到下一轮检索</text>
      </svg>

      <div class="srs-flow-legend">
        <span><span class="srs-dot" style="background:#b6d2ff"></span> 发现 —— 找到候选论文</span>
        <span><span class="srs-dot" style="background:#ffe39a"></span> 理解 —— 把论文转化为知识</span>
        <span><span class="srs-dot" style="background:#a5e8c0"></span> 整理与产出 —— 入库或交付成果</span>
      </div>
    </div>
  </section>

  <!-- =========================== INSTALL =========================== -->
  <section id="install" class="srs-section">
    <h2 class="srs-section-title"><i class="fas fa-download"></i> 安装</h2>
    <p class="srs-section-sub">每个 skill 是一个独立目录，含遵循 <a href="https://agentskills.io/" target="_blank" rel="noopener">开放 agent skills 标准</a>的 <code>SKILL.md</code>。放到任意 skills 目录后会被自动发现，无需重启。</p>

    <div class="srs-tabs srs-fadeup" id="srs-install-tabs-zh">
      <div class="srs-tabbar">
        <button class="srs-tab is-active" data-target="openclaw">OpenClaw</button>
        <button class="srs-tab" data-target="claude">Claude Code</button>
        <button class="srs-tab" data-target="codex">Codex</button>
      </div>

      <pre class="srs-code is-active" data-tab="openclaw"><code># 克隆
git clone https://github.com/jxtse/scientific-research-skills.git
cd scientific-research-skills

# 全部安装（用户级）
cp -r skills/* ~/.openclaw/skills/

# 或选择性安装
cp -r skills/literature-search ~/.openclaw/skills/
cp -r skills/paper-reading     ~/.openclaw/skills/</code></pre>

      <pre class="srs-code" data-tab="claude"><code># 克隆
git clone https://github.com/jxtse/scientific-research-skills.git
cd scientific-research-skills

# 用户级（所有项目可用）
cp -r skills/* ~/.claude/skills/

# 或项目级（仅当前仓库）
cp -r skills/* .claude/skills/</code></pre>

      <pre class="srs-code" data-tab="codex"><code># 克隆
git clone https://github.com/jxtse/scientific-research-skills.git
cd scientific-research-skills

# 用户级（所有仓库可用）
cp -r skills/* ~/.agents/skills/

# 或项目级
cp -r skills/* .agents/skills/</code></pre>
    </div>
  </section>

  <!-- =========================== DEPENDENCIES =========================== -->
  <section class="srs-section">
    <h2 class="srs-section-title"><i class="fas fa-key"></i> 依赖一览</h2>
    <p class="srs-section-sub">方法论型 skill 开箱即用；工具集成型 skill 需要先做配置。</p>

    <div class="srs-table-wrap srs-fadeup">
      <table class="srs-table">
        <thead>
          <tr><th>Skill</th><th>需要配置</th><th>从哪获取</th><th>是否必需</th></tr>
        </thead>
        <tbody>
          <tr>
            <td><code>literature-search</code></td>
            <td>任一：<code>TAVILY_API_KEY</code>、<code>EXA_API_KEY</code>、<code>GEMINI_API_KEY</code>、<code>AMINER_API_KEY</code></td>
            <td>Semantic Scholar 与 arXiv 无需 key</td>
            <td><span class="srs-pill srs-pill-recommend">推荐</span></td>
          </tr>
          <tr>
            <td><code>paper-reading</code></td>
            <td>无</td>
            <td>—</td>
            <td><span class="srs-pill srs-pill-none">无</span></td>
          </tr>
          <tr>
            <td><code>social-media-paper-triage</code></td>
            <td>Jina Reader（无需 key）覆盖大部分链接；X / 小红书 / 微信需 <a href="https://github.com/Panniantong/Agent-Reach" target="_blank" rel="noopener">Agent Reach</a></td>
            <td>Jina Reader / xreach / Agent Reach</td>
            <td><span class="srs-pill srs-pill-optional">可选</span></td>
          </tr>
          <tr>
            <td><code>related-work-survey</code></td>
            <td>沿用 literature-search 的配置</td>
            <td>—</td>
            <td><span class="srs-pill srs-pill-optional">先配检索</span></td>
          </tr>
          <tr>
            <td><code>zotero-management</code></td>
            <td><code>ZOTERO_API_KEY</code> + <code>ZOTERO_USER_ID</code></td>
            <td><a href="https://www.zotero.org/settings/keys" target="_blank" rel="noopener">zotero.org/settings/keys</a></td>
            <td><span class="srs-pill srs-pill-required">必需</span></td>
          </tr>
          <tr>
            <td><code>academic-figure-generation</code></td>
            <td>本地部署 <a href="https://github.com/paperbanana/PaperBanana" target="_blank" rel="noopener">PaperBanana</a></td>
            <td>详见 SKILL.md</td>
            <td><span class="srs-pill srs-pill-required">必需</span></td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="srs-callout">
      <i class="fas fa-info-circle"></i>
      <div>
        <strong>配置规范已内置在 skill 中。</strong>当 AI agent 帮你安装这些 skill 时，会被指示：先检查已有环境变量；逐个 skill 引导你；把 <code>export</code> 写到 shell profile（而不是只写到当前会话）；逐个 key 做冒烟测试后再继续。绝不会把密钥写到受 git 追踪的文件里。
      </div>
    </div>
  </section>

  <!-- =========================== FOOTER =========================== -->
  <section class="srs-footer-section">
    <div class="srs-footer-card srs-fadeup">
      <h3><i class="fas fa-code-branch"></i> 贡献新 Skill</h3>
      <p>新 skill 会随研究工作流的成熟陆续加入。新建 <code>skills/&lt;name&gt;/SKILL.md</code>（YAML 头 + Markdown 正文），重点写清<em>何时用</em>、<em>为何用</em>（而非仅"如何用"），用一段话描述工作流后提交 PR。</p>
      <a class="srs-btn srs-btn-primary" href="https://github.com/jxtse/scientific-research-skills" target="_blank" rel="noopener"><i class="fab fa-github"></i> GitHub 仓库</a>
      <a class="srs-btn srs-btn-ghost" href="https://github.com/jxtse/scientific-research-skills/blob/main/LICENSE" target="_blank" rel="noopener"><i class="fas fa-balance-scale"></i> MIT 许可证</a>
    </div>
  </section>

</div>

<script>
(function() {
  var tabs = document.querySelectorAll('#srs-install-tabs-zh .srs-tab');
  var panes = document.querySelectorAll('#srs-install-tabs-zh .srs-code');
  tabs.forEach(function(btn) {
    btn.addEventListener('click', function() {
      var target = btn.getAttribute('data-target');
      tabs.forEach(function(b){ b.classList.toggle('is-active', b === btn); });
      panes.forEach(function(p){ p.classList.toggle('is-active', p.getAttribute('data-tab') === target); });
    });
  });

  if ('IntersectionObserver' in window) {
    var io = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible');
          io.unobserve(entry.target);
        }
      });
    }, {threshold: 0.15, rootMargin: '0px 0px -12% 0px'});
    document.querySelectorAll('.srs-fadeup, .srs-fadeup-stagger').forEach(function(el) {
      io.observe(el);
    });
  } else {
    document.querySelectorAll('.srs-fadeup, .srs-fadeup-stagger').forEach(function(el) {
      el.classList.add('is-visible');
    });
  }
})();
</script>
