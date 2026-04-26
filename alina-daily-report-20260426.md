<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>📋 Obsidian 大脑 · 本周信息汇报 | 4.20 - 4.26</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  
  :root {
    --bg-primary: #0f0f1a;
    --bg-card: #1a1a2e;
    --bg-card-hover: #222240;
    --accent-gold: #f0c040;
    --accent-cyan: #40d9f0;
    --accent-green: #4ade80;
    --accent-red: #f87171;
    --accent-orange: #fb923c;
    --accent-purple: #c084fc;
    --text-primary: #f1f5f9;
    --text-secondary: #94a3b8;
    --text-muted: #64748b;
    --border-color: rgba(255,255,255,0.08);
    --glow-gold: rgba(240,192,64,0.15);
    --glow-cyan: rgba(64,217,240,0.12);
  }
  
  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Hiragino Sans GB', sans-serif;
    background: var(--bg-primary);
    color: var(--text-primary);
    line-height: 1.7;
    min-height: 100vh;
    -webkit-font-smoothing: antialiased;
  }

  /* Header */
  .header {
    text-align: center;
    padding: 40px 20px 30px;
    background: linear-gradient(135deg, rgba(240,192,64,0.08) 0%, rgba(64,217,240,0.05) 50%, rgba(192,132,252,0.06) 100%);
    border-bottom: 1px solid var(--border-color);
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle at 30% 40%, rgba(240,192,64,0.06) 0%, transparent 50%),
                radial-gradient(circle at 70% 60%, rgba(64,217,240,0.04) 0%, transparent 50%);
    pointer-events: none;
  }
  .header-emoji { font-size: 48px; margin-bottom: 12px; display: block; }
  .header h1 {
    font-size: 22px;
    font-weight: 700;
    letter-spacing: 1px;
    background: linear-gradient(135deg, var(--accent-gold), var(--accent-cyan));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
  }
  .header-sub {
    font-size: 13px;
    color: var(--text-muted);
    margin-top: 8px;
    letter-spacing: 0.5px;
  }
  .header-date {
    display: inline-block;
    margin-top: 10px;
    padding: 4px 16px;
    background: rgba(240,192,64,0.1);
    border: 1px solid rgba(240,192,64,0.2);
    border-radius: 20px;
    font-size: 12px;
    color: var(--accent-gold);
    position: relative;
  }

  /* Container */
  .container {
    max-width: 640px;
    margin: 0 auto;
    padding: 20px 16px 40px;
  }

  /* Stats Bar */
  .stats-bar {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    margin-bottom: 24px;
  }
  .stat-item {
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: 14px;
    padding: 16px 12px;
    text-align: center;
  }
  .stat-num {
    font-size: 26px;
    font-weight: 800;
    display: block;
  }
  .stat-label {
    font-size: 11px;
    color: var(--text-muted);
    margin-top: 2px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }
  .stat-num.gold { color: var(--accent-gold); }
  .stat-num.cyan { color: var(--accent-cyan); }
  .stat-num.green { color: var(--accent-green); }

  /* Section */
  .section {
    margin-bottom: 24px;
  }
  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 14px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border-color);
  }
  .section-icon {
    width: 32px;
    height: 32px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    flex-shrink: 0;
  }
  .section-icon.product { background: rgba(240,192,64,0.15); }
  .section-icon.sop { background: rgba(64,217,240,0.12); }
  .section-icon.team { background: rgba(192,132,252,0.12); }
  .section-icon.student { background: rgba(74,222,128,0.12); }
  .section-icon.content { background: rgba(251,146,60,0.12); }
  .section-icon.idea { background: rgba(248,113,113,0.12); }
  .section-icon.alert { background: rgba(248,113,113,0.15); }
  .section-title {
    font-size: 16px;
    font-weight: 700;
  }
  .section-badge {
    margin-left: auto;
    padding: 2px 10px;
    border-radius: 10px;
    font-size: 11px;
    font-weight: 600;
  }
  .badge-high { background: rgba(248,113,113,0.15); color: var(--accent-red); }
  .badge-mid { background: rgba(251,146,60,0.15); color: var(--accent-orange); }
  .badge-low { background: rgba(74,222,128,0.12); color: var(--accent-green); }
  .badge-new { background: rgba(240,192,64,0.15); color: var(--accent-gold); }

  /* Cards */
  .card {
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: 14px;
    padding: 18px;
    margin-bottom: 12px;
    transition: all 0.2s ease;
  }
  .card:hover {
    border-color: rgba(255,255,255,0.15);
    background: var(--bg-card-hover);
  }
  .card-title {
    font-size: 15px;
    font-weight: 700;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .card-title .tag {
    font-size: 10px;
    padding: 2px 8px;
    border-radius: 6px;
    font-weight: 600;
    flex-shrink: 0;
  }
  .tag-pending { background: rgba(251,146,60,0.15); color: var(--accent-orange); }
  .tag-done { background: rgba(74,222,128,0.12); color: var(--accent-green); }
  .tag-hot { background: rgba(248,113,113,0.15); color: var(--accent-red); }
  .tag-v2 { background: rgba(192,132,252,0.15); color: var(--accent-purple); }
  .card-body {
    font-size: 13.5px;
    color: var(--text-secondary);
    line-height: 1.75;
  }
  .card-body p { margin-bottom: 8px; }
  .card-body p:last-child { margin-bottom: 0; }

  /* List styles */
  .detail-list {
    list-style: none;
    padding: 0;
  }
  .detail-list li {
    padding: 6px 0;
    padding-left: 18px;
    position: relative;
    font-size: 13px;
    color: var(--text-secondary);
    border-bottom: 1px dashed rgba(255,255,255,0.04);
  }
  .detail-list li:last-child { border-bottom: none; }
  .detail-list li::before {
    content: '›';
    position: absolute;
    left: 0;
    color: var(--accent-cyan);
    font-weight: bold;
  }
  .highlight { 
    color: var(--accent-gold); 
    font-weight: 600; 
  }
  .highlight-cyan { 
    color: var(--accent-cyan); 
    font-weight: 500; 
  }
  .highlight-green { 
    color: var(--accent-green); 
    font-weight: 500; 
  }
  .highlight-red { 
    color: var(--accent-red); 
    font-weight: 600; 
  }

  /* SOP Table */
  .sop-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 12.5px;
    margin-top: 8px;
  }
  .sop-table th {
    text-align: left;
    padding: 8px 10px;
    background: rgba(255,255,255,0.03);
    color: var(--text-muted);
    font-weight: 600;
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 1px solid var(--border-color);
  }
  .sop-table td {
    padding: 10px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    vertical-align: top;
  }
  .sop-table tr:last-child td { border-bottom: none; }
  .priority-high { color: var(--accent-red); font-weight: 700; }
  .priority-mid { color: var(--accent-orange); font-weight: 600; }
  .priority-low { color: var(--accent-green); font-weight: 500; }

  /* Blind Spot Alert Box */
  .alert-box {
    background: linear-gradient(135deg, rgba(248,113,113,0.08), rgba(251,146,60,0.06));
    border: 1px solid rgba(248,113,113,0.2);
    border-radius: 14px;
    padding: 20px;
    margin-top: 28px;
  }
  .alert-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 14px;
  }
  .alert-icon { font-size: 22px; }
  .alert-title {
    font-size: 16px;
    font-weight: 800;
    color: var(--accent-red);
  }
  .alert-item {
    background: rgba(0,0,0,0.2);
    border-radius: 10px;
    padding: 14px 16px;
    margin-bottom: 10px;
  }
  .alert-item:last-child { margin-bottom: 0; }
  .alert-item-title {
    font-size: 14px;
    font-weight: 700;
    margin-bottom: 6px;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .alert-item-body {
    font-size: 13px;
    color: var(--text-secondary);
    line-height: 1.7;
  }

  /* Footer */
  .footer {
    text-align: center;
    padding: 24px 0 10px;
    border-top: 1px solid var(--border-color);
    margin-top: 32px;
  }
  .footer-text {
    font-size: 11px;
    color: var(--text-muted);
    line-height: 1.8;
  }
  .footer-text span { color: var(--accent-cyan); }

  /* Inline tag */
  .inline-tag {
    display: inline-block;
    padding: 1px 7px;
    border-radius: 5px;
    font-size: 11px;
    font-weight: 600;
    margin-right: 4px;
  }

  /* Divider */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border-color), transparent);
    margin: 20px 0;
  }

  /* Price highlight */
  .price { 
    font-family: 'SF Mono', Monaco, monospace;
    background: rgba(240,192,64,0.1);
    padding: 1px 6px;
    border-radius: 4px;
    color: var(--accent-gold);
    font-weight: 700;
    font-size: 12px;
  }

  /* Check/unchecked items */
  .check-item {
    padding-left: 22px;
    position: relative;
    margin: 4px 0;
    font-size: 13px;
    color: var(--text-secondary);
  }
  .check-item::before {
    content: '☐';
    position: absolute;
    left: 0;
    color: var(--text-muted);
    font-size: 13px;
  }

  @media (max-width: 480px) {
    .header h1 { font-size: 19px; }
    .stats-bar { gap: 6px; }
    .stat-item { padding: 12px 8px; }
    .stat-num { font-size: 22px; }
    .card { padding: 14px; }
    .sop-table { font-size: 11.5px; }
    .sop-table td { padding: 8px 6px; }
  }
</style>
</head>
<body>

<!-- Header -->
<div class="header">
  <span class="header-emoji">🧠</span>
  <h1>Obsidian 大脑 · 本周信息汇报</h1>
  <div class="header-sub">Alina 霖子 | 一人公司知识大脑扫描结果</div>
  <div class="header-date">📅 2026年4月20日 ~ 4月26日（周日）</div>
</div>

<div class="container">

  <!-- Stats -->
  <div class="stats-bar">
    <div class="stat-item">
      <span class="stat-num gold">45+</span>
      <span class="stat-label">本周变更文件</span>
    </div>
    <div class="stat-item">
      <span class="stat-num cyan">5</span>
      <span class="stat-label">内容分类</span>
    </div>
    <div class="stat-item">
      <span class="stat-num green">3</span>
      <span class="stat-label">待处理事项</span>
    </div>
  </div>

  <!-- ========== 1. 产品策划 ========== -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon product">🎯</div>
      <span class="section-title">产品策划灵感</span>
      <span class="section-badge badge-new">NEW</span>
    </div>

    <div class="card">
      <div class="card-title">
        AI 一人公司操作系统
        <span class="tag tag-pending">待深化</span>
      </div>
      <div class="card-body">
        <p><span class="highlight">产品形态：</span>文字课程 | <span class="price">¥3,980</span> | 发布平台：Skool</p>
        <p><span class="highlight">定位：</span>从"创作者→创业者"的转变，面向内向创作者</p>
        <p><span class="highlight">两大核心逻辑：</span></p>
        <ul class="detail-list">
          <li><strong>内容即营销</strong> — 通过文字类型的内容实现自动获客</li>
          <li><strong>内容即交付</strong> — 文字内容本身就是产品，直接用于交付</li>
        </ul>
        <p style="margin-top:10px"><span class="highlight">制作计划：</span></p>
        <ul class="detail-list">
          <li>阶段一：提取所有视频课程的文字稿作为素材库</li>
          <li>阶段二：由 Claude 帮助创作内容初稿和课纲</li>
        </ul>
        <p style="margin-top:10px;color:var(--accent-orange)">⚠️ 尚未展开的关联思考（5项）：</p>
        <div style="margin-left:4px">
          <div class="check-item">与现有产品线的关系？（VIP ¥980 → ¥3,980 → 教练班 ¥9,800 → 合伙人 ¥39,800）</div>
          <div class="check-item">目标学员画像更具体化：内向 vs 内向创作者有何区别？</div>
          <div class="check-item">Skool 平台选型原因？中国用户支付问题？</div>
          <div class="check-item">课纲大致框架是什么？是否需要录制视频？</div>
        </div>
      </div>
    </div>
  </div>

  <!-- ========== 2. SOP & 流程建设 ========== -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon sop">📋</div>
      <span class="section-title">SOP & 流程建设</span>
      <span class="section-badge badge-high">重点</span>
    </div>

    <table class="sop-table card">
      <thead>
        <tr>
          <th style="width:28%">SOP 名称</th>
          <th style="width:12%">优先级</th>
          <th>现状 & 下一步</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>课程逐字稿处理</strong></td>
          <td><span class="priority-high">🔴 最高</span></td>
          <td>SOP 已建立 ✅（8维度提炼框架）。文件夹里已有大量积压文件，<span class="highlight-red">尚未开始批量处理</span></td>
        </tr>
        <tr>
          <td><strong>新合伙人入职</strong></td>
          <td><span class="priority-high">🔴 高</span></td>
          <td>木木有手动版本，<span class="highlight-cyan">需 Alina 发给 Claude 转化为标准 SOP</span></td>
        </tr>
        <tr>
          <td><strong>合伙人续费/到期跟进</strong></td>
          <td><span class="priority-high">🔴 高</span></td>
          <td>目前<span class="highlight-red">完全无流程，靠记忆或偶然发现</span>。规划并入周会SOP</td>
        </tr>
        <tr>
          <td><strong>多平台分发</strong></td>
          <td><span class="priority-mid">🟡 中</span></td>
          <td>仍在磨合中，等平台规则稳定后标准化</td>
        </tr>
        <tr>
          <td><strong>知识大脑整理</strong></td>
          <td><span class="priority-low">🟢 中</span></td>
          <td>规则已定义（更新/覆盖/归档/删除），<span class="highlight-cyan">待 Alina 确认后写入正式 SOP</span></td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- ========== 3. AI 团队架构 ========== -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon team">🤖</div>
      <span class="section-title">AI 团队架构更新</span>
      <span class="section-badge tag-v2">v2.0</span>
    </div>

    <div class="card">
      <div class="card-title">
        每周工作流 v2.0
        <span class="tag tag-done">已更新</span>
      </div>
      <div class="card-body">
        <p><span class="highlight-cyan">更新时间：</span>2026.04.24</p>
        <p><span class="highlight-cyan">新增 Skill 集成：</span>topic-radar / alina-video-writer / 多平台分发矩阵</p>
        
        <table style="width:100%;font-size:12px;margin-top:12px;border-collapse:collapse;">
          <tr style="background:rgba(255,255,255,0.02)"><th style="padding:6px 8px;text-align:left;color:var(--text-muted)">#</th><th style="padding:6px;text-align:left;color:var(--text-muted)">职能</th><th style="padding:6px;text-align:left;color:var(--text-muted)">Skill / 方式</th><th style="padding:6px;text-align:left;color:var(--text-muted)">触发时机</th></tr>
          <tr><td style="padding:6px 8px">①</td><td style="padding:6px">选题策划</td><td style="padding:6px"><code style="background:rgba(64,217,240,0.1);padding:1px 5px;border-radius:3px;font-size:11px">topic-radar</code></td><td style="padding:6px">每周一</td></tr>
          <tr><td style="padding:6px 8px">②</td><td style="padding:6px">采编挖素材</td><td style="padding:6px">直接对话</td><td style="padding:6px">每周二</td></tr>
          <tr><td style="padding:6px 8px">③</td><td style="padding:6px">公众号写作</td><td style="padding:6px"><code style="background:rgba(64,217,240,0.1);padding:1px 5px;border-radius:3px;font-size:11px">alina-wechat-writer</code></td><td style="padding:6px">每周三</td></tr>
          <tr><td style="padding:6px 8px">④</td><td style="padding:6px">口播逐字稿</td><td style="padding:6px"><code style="background:rgba(192,132,252,0.12);padding:1px 5px;border-radius:3px;font-size:11px;color:var(--accent-purple)">alina-video-writer 🆕</code></td><td style="padding:6px">每周四</td></tr>
          <tr><td style="padding:6px 8px">⑤</td><td style="padding:6px">品牌策划</td><td style="padding:6px"><code>personal-brand-planner</code></td><td style="padding:6px">按需</td></tr>
          <tr><td style="padding:6px 8px">⑥</td><td style="padding:6px">知识大脑管理</td><td style="padding:6px"><code>consolidate-memory</code></td><td style="padding:6px">按需</td></tr>
          <tr><td style="padding:6px 8px">⑦</td><td style="padding:6px">海报文案</td><td style="padding:6px"><code>poster-copywriter</code></td><td style="padding:6px">按需</td></tr>
          <tr><td style="padding:6px 8px">⑧</td><td style="padding:6px">社群运营</td><td style="padding:6px"><code style="color:var(--accent-purple)">alina-group-forward 🆕</code></td><td style="padding:6px">周五</td></tr>
          <tr><td style="padding:6px 8px">⑨</td><td style="padding:6px">多平台分发</td><td style="padding:6px"><code style="color:var(--accent-purple)">content-matrix 等 🆕</code></td><td style="padding:6px">周五</td></tr>
          <tr><td style="padding:6px 8px">⑩</td><td style="padding:6px">学员反馈分析</td><td style="padding:6px">直接对话</td><td style="padding:6px">周末</td></tr>
        </table>
        
        <p style="margin-top:12px;font-size:12px;color:var(--text-muted)">
          ⚡ 本周同步更新了全部 10 位 AI 员工的档案文件 + 5 个 SOP 文件 + 2 个模板库文件
        </p>
      </div>
    </div>
  </div>

  <!-- ========== 4. 学员档案 ========== -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon student">👥</div>
      <span class="section-title">学员档案动态</span>
      <span class="section-badge badge-mid">17份</span>
    </div>

    <div class="card">
      <div class="card-body">
        <p>本周有 <span class="highlight">17 份</span>学员档案文件被更新/访问，涵盖以下类别：</p>
        <ul class="detail-list" style="margin-top:8px">
          <li><strong>教练班在籍学员：</strong>Jasper、涂涂、山海、慕鸣boom、粥粥、周闯闯、梁芷瑛、慧勤（8人）</li>
          <li><strong>往届学员档案：</strong>Daniel、Leah咖喱、皓月、毛瑾红、嘉一、张聪聪、从心、Sophie（8人）</li>
          <li><strong>督导团队：</strong>娟子、爱米粒、千和、曼珞（4人）</li>
          <li><strong>总览文件：</strong>2023届/2025届教练班汇总 + 教练班总览表</li>
        </ul>
        <p style="margin-top:10px;font-size:12px;color:var(--text-muted)">
          💡 提示：这些文件的更新可能是系统自动触发的元数据刷新（如修改时间戳），不一定是内容层面的重大编辑。建议确认哪些是<span class="highlight-cyan">实际有业务动作的档案</span>。
        </p>
      </div>
    </div>
  </div>

  <!-- ========== 5. 内容输出 ========== -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon content">📝</div>
      <span class="section-title">本周内容产出</span>
      <span class="section-badge badge-done">已完成</span>
    </div>

    <div class="card">
      <div class="card-title">
        AI 情报周报 · 第N期（4月26日版）
      </div>
      <div class="card-body">
        <p><span class="highlight">数据范围：</span>4.19 - 4.26 | <span class="highlight">初筛 60+ 条 → 入选 15 条</span></p>
        <p style="margin-top:8px"><strong>四大板块概览：</strong></p>
        <ul class="detail-list">
          <li><span class="highlight-gold">AI 前沿（3条）：</span>GPT-5.5 发布 / Claude Mythos+降智事件 / Kimi K2.6 开源 + Qwen3.6-Max</li>
          <li><span class="highlight-cyan">实战工作流（5条）：</span>Karpathy LLM Wiki / 自媒体批量内容SOP / 图文批量创作 / GPT-5.5 Agent模式 / 抖音AIGC规范</li>
          <li><span class="highlight-green">对标观察（4条）：</span>你自己 / Dan Koe / Justin Welsh / Pieter Levels 式风潮</li>
          <li><span class="highlight">政策洞察（3条）：</span>AI拟人化互动法规 / AIGC版权保护 / 网络视听报告</li>
        </ul>
        <p style="margin-top:10px;padding:10px;background:rgba(74,222,128,0.06);border-radius:8px;font-size:12.5px">
          <strong>🎯 本周行动建议：</strong><br>
          ✅ 测试：用 Karpathy 的 LLM Wiki 方法升级 Obsidian<br>
          🔁 模仿：Dan Koe "一封信养活全平台" 分发策略<br>
          ❌ 忽略：Claude Mythos（暂不开放，不值得花时间）
        </p>
      </div>
    </div>
  </div>

  <!-- ========== ⚠️ 盲点提醒 ========== -->
  <div class="alert-box">
    <div class="alert-header">
      <span class="alert-icon">⚠️</span>
      <span class="alert-title">Claw 发现的可能盲点</span>
    </div>

    <div class="alert-item">
      <div class="alert-item-title">
        <span>🔴</span> 课程逐字稿积压严重 — 最大效率漏斗
      </div>
      <div class="alert-item-body">
        SOP 已经写好了（8维度提炼框架），但<span class="highlight-red">一份都还没开始批量处理</span>。你的课程逐字稿里藏着最核心的方法论和金句——这是你打造新产品（¥3,980 文字课）的原始素材来源。<br><br>
        <strong>建议：</strong>下周跟 Cowork 对话时，直接触发「帮我处理课程逐字稿」，先跑 3-4 份试水。这步不走通，文字课的产品设计就是空中楼阁。
      </div>
    </div>

    <div class="alert-item">
      <div class="alert-item-title">
        <span>🟠</span> 合伙人续费/到期跟进 = 零流程
      </div>
      <div class="alert-item-body">
        你现在有 300+ 认证学员，但<span class="highlight-red">续费提醒完全靠记忆或偶然发现</span>。这不仅是收入流失风险，更是对合伙人体验的伤害——人家在你这儿花了近 4 万块，到期了你连个主动问候都没有？<br><br>
        <strong>建议：</strong>最简方案：让 Claude 在每次处理周会记录时自动检查 30/60 天内到期的学员并提醒你。不需要单独建系统，<span class="highlight-green">搭进现有的周会 SOP 里就行</span>。
      </div>
    </div>

    <div class="alert-item">
      <div class="alert-item-title">
        <span>🟠</span> AI 一人公司操作系统（¥3,980 产品）— 卡在灵感阶段
      </div>
      <div class="alert-item-body">
        4 月 22 号记下来的产品灵感，到今天还是「⏳ 待深化」状态。<span class="highlight-cyan">5 个关键问题全没回答</span>：产品线关系、学员画像差异、支付方式、课纲框架……<br><br>
        <strong>建议：</strong>这个产品如果要做，它填补的是 VIP ¥980 和教练班 ¥9,800 之间的空白市场（内向创作者转型赛道）。建议安排一次 30 分钟的深度思考会，把 5 个问题过一遍——<span class="highlight">要么推进，要么暂时搁置，不要悬在中间消耗注意力</span>。
      </div>
    </div>

    <div class="alert-item">
      <div class="alert-item-title">
        <span>🟡</span> 收件箱有 2 项待处理 — 小但重要
      </div>
      <div class="alert-item-body">
        <code style="background:rgba(0,0,0,0.2);padding:1px 5px;border-radius:3px;font-size:12px">00_Inbox/待处理/</code> 下有两项：
        <ol style="margin:6px 0 0 18px;font-size:13px;color:var(--text-secondary)">
          <li>AI 一人公司操作系统产品灵感（上面已提到）</li>
          <li>SOP 规划待办清单（5 个方向，部分已在推进中）</li>
        </ol>
        这两个其实已经融入了上面的讨论，可以标记为<span class="highlight-green">"已纳入关注"</span>或在下次整理时移入已处理。
      </div>
    </div>

    <div class="alert-item">
      <div class="alert-item-title">
        <span>🟢</span> 新合伙人入职 SOP — 只差你一步
      </div>
      <div class="alert-item-body">
        木木已经有手动版本了。<span class="highlight-cyan">只等你把文件发给 Claude 就能转成标准 SOP</span>。第 10 期实操营正在进行（20 人目标 50 万冲百万），如果有新人加入合伙人体系，没有标准入职流程会很被动。<br><br>
        <strong>建议：</strong>找木木要一下那个文件，转发给 Claude 处理。10 分钟的事。
      </div>
    </div>
  </div>

  <!-- Footer -->
  <div class="footer">
    <div class="footer-text">
      🤖 由 <span>ClawBot</span> 扫描 Obsidian 大脑自动生成<br>
      数据来源：~/Desktop/Obsidian大脑/ | 扫描时间：2026.04.26 12:04 NZT<br>
      <span style="color:var(--text-muted)">本报告基于文件变更记录归纳整理，非完整内容读取</span>
    </div>
  </div>

</div>

</body>
</html>