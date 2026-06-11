# HTML 汇报页面设计系统

> **适用范围**：本文件专属于**输出形态 ① 深度阅读版**（纵向滚动单文件 HTML）。
> 横向翻页网页 PPT（形态 ② 电子杂志风 / ③ 瑞士风）的设计规范在 `references/ppt-styles.md`，复用 guizang-ppt-skill 的模板。
>
> 本文档定义了深度阅读版 HTML 页面的设计规范、组件库和代码模板。

---

## 1. 整体架构

```
┌─────────────────────────────────────────┐
│  HERO / 封面                             │  ← 标题 + 3 个核心数字
│  背景：深蓝渐变 + 微妙的几何图案          │
├─────────────────────────────────────────┤
│  SECTION 1: Executive Summary            │  ← 一句话结论 + 3 大成果卡片
│  背景：浅灰 #f7fafc                      │
├─────────────────────────────────────────┤
│  SECTION 2: 结果全景                      │  ← 目标 vs 实际 + 里程碑
│  背景：白色                               │
├─────────────────────────────────────────┤
│  SECTION 3: 过程拆解                      │  ← 关键举措 + 议题树展开
│  背景：浅灰 #f7fafc                      │
├─────────────────────────────────────────┤
│  SECTION 4: 洞察与经验沉淀                │  ← 空雨伞发现卡片
│  背景：白色                               │
├─────────────────────────────────────────┤
│  SECTION 5: 未来展望与努力方向            │  ← 3 个主攻方向 + 时间轴
│  背景：深蓝 #1a365d（区分感）            │
├─────────────────────────────────────────┤
│  FOOTER: 汇报信息                         │
│  背景：深灰                               │
└─────────────────────────────────────────┘
```

---

## 2. 设计系统

### 色彩规范

```css
:root {
  /* 主色系 */
  --primary-dark: #1a365d;    /* 深蓝 - Hero 背景、重点 Section */
  --primary: #2b6cb0;         /* 中蓝 - 按钮、链接、强调 */
  --primary-light: #ebf4ff;   /* 浅蓝 - 卡片背景、hover */

  /* 中性色 */
  --gray-50: #f7fafc;         /* Section 交替背景 */
  --gray-100: #edf2f7;        /* 卡片边框 */
  --gray-200: #e2e8f0;        /* 分割线 */
  --gray-400: #a0aec0;        /* 次要文字 */
  --gray-600: #4a5568;        /* 正文 */
  --gray-800: #1a202c;        /* 标题 */
  --gray-900: #0f1419;        /* Hero 文字 */

  /* 数据色板 */
  --data-blue: #3182ce;       /* 趋势、完成率 */
  --data-green: #38a169;      /* 正向、达标 */
  --data-orange: #dd6b20;     /* 预警、进行中 */
  --data-purple: #805ad5;     /* 创新、亮点 */
  --data-red: #e53e3e;        /* 下降、预警（慎用） */

  /* 状态色 */
  --success: #38a169;
  --warning: #d69e2e;
  --danger: #e53e3e;
  --info: #3182ce;

  /* 排版 */
  --font-heading: 'Noto Sans SC', 'Inter', -apple-system, sans-serif;
  --font-body: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC',
               'Microsoft YaHei', sans-serif;
  --font-mono: 'SF Mono', 'Cascadia Code', 'Consolas', monospace;
}
```

### 字体层级

| 层级 | 字号 | 字重 | 用途 |
|------|------|------|------|
| H0 | 2.75rem (44px) | 800 | Hero 超大标题 |
| H1 | 1.875rem (30px) | 700 | Section 标题 |
| H2 | 1.5rem (24px) | 700 | 子标题 |
| H3 | 1.25rem (20px) | 600 | 卡片标题 |
| Body L | 1.125rem (18px) | 400 | 正文大 |
| Body | 1rem (16px) | 400 | 正文 |
| Body S | 0.875rem (14px) | 400 | 辅助说明 |
| Caption | 0.75rem (12px) | 400 | 标签、脚注 |
| KPI Number | 3rem (48px) | 800 | 核心 KPI 数字 |
| KPI Unit | 0.875rem (14px) | 400 | KPI 单位 |

---

## 3. 核心组件

### 3.1 Hero 封面

```html
<header class="hero">
  <div class="hero-bg-pattern"></div> <!-- CSS 几何图案 -->
  <div class="hero-content">
    <p class="hero-period">2025 年度 · 行政与园区运营部</p>
    <h1 class="hero-title">成果汇报</h1>
    <p class="hero-subtitle">服务创新 · 降本增效 · 体验升级</p>
    <div class="hero-kpis">
      <div class="hero-kpi">
        <div class="kpi-number">98.5<span class="kpi-unit">%</span></div>
        <div class="kpi-label">服务满意度</div>
      </div>
      <div class="hero-kpi">
        <div class="kpi-number">1,280<span class="kpi-unit">万</span></div>
        <div class="kpi-label">年度降本</div>
      </div>
      <div class="hero-kpi">
        <div class="kpi-number">0<span class="kpi-unit">事故</span></div>
        <div class="kpi-label">安全运营</div>
      </div>
    </div>
  </div>
</header>
```

### 3.2 KPI 数字卡片

```html
<div class="kpi-card">
  <div class="kpi-card-icon">📊</div>
  <div class="kpi-card-value">
    <span class="kpi-number">28<span class="kpi-unit">分钟</span></span>
    <span class="kpi-trend up">↓35%</span>
  </div>
  <div class="kpi-card-label">工单平均响应时间</div>
  <div class="kpi-card-desc">较2024年缩短15分钟，行业前20%</div>
</div>
```

### 3.3 目标 vs 实际对比条

```html
<div class="progress-item">
  <div class="progress-header">
    <span class="progress-label">工单解决率</span>
    <span class="progress-value">
      <span class="actual">97.2%</span>
      <span class="target">目标：95%</span>
    </span>
  </div>
  <div class="progress-bar">
    <div class="progress-fill" style="width: 97.2%"></div>
    <div class="progress-target-marker" style="left: 95%"></div>
  </div>
</div>
```

### 3.4 议题树展开面板

```html
<div class="issue-tree">
  <div class="tree-root">核心举措：三管齐下降本增效</div>
  <div class="tree-branches">
    <div class="tree-branch">
      <div class="branch-header" onclick="toggleBranch(this)">
        <span class="branch-icon">🔧</span>
        <span>空间改造</span>
        <span class="branch-stat">节省 520 万</span>
        <span class="chevron">▾</span>
      </div>
      <div class="branch-details">
        <p>完成 3,200㎡ 办公空间改造...</p>
        <ul>
          <li>开放工位占比从 30% → 65%</li>
          <li>新增工位 280 个，避免外租 2,000㎡</li>
          <li>人均面积优化：5.2㎡ → 4.5㎡</li>
        </ul>
      </div>
    </div>
    <!-- 更多分支... -->
  </div>
</div>
```

### 3.5 空雨伞洞察卡片

```html
<div class="insight-card">
  <div class="insight-sky">
    <span class="insight-label">空 · 事实</span>
    <p>2025年能耗费用同比 ↑8%，电费占比 62%</p>
  </div>
  <div class="insight-arrow">↓</div>
  <div class="insight-rain">
    <span class="insight-label">雨 · 解读</span>
    <p>员工增长 40% + 24h 数据机房是主因，非管理失效</p>
  </div>
  <div class="insight-arrow">↓</div>
  <div class="insight-umbrella">
    <span class="insight-label">伞 · 行动</span>
    <p>2026年推进机房独立计量 + 余热回收，目标回落至 2024 水平</p>
  </div>
</div>
```

### 3.6 未来展望时间轴

```html
<div class="outlook-section">
  <h2>2026 年展望：三个主攻方向</h2>
  <div class="outlook-timeline">
    <div class="timeline-item priority-high">
      <div class="timeline-marker">P0</div>
      <div class="timeline-content">
        <h3>智慧园区 2.0</h3>
        <p>从"有系统"到"系统好用"，打通数据孤岛</p>
        <div class="timeline-meta">
          <span>Q1-Q2 上线</span>
          <span>预期节省 300 万</span>
        </div>
      </div>
    </div>
    <div class="timeline-item priority-mid">
      <div class="timeline-marker">P1</div>
      <div class="timeline-content">
        <h3>服务产品化</h3>
        <p>建立行政服务目录 + SLA 承诺，让服务可量化</p>
        <div class="timeline-meta">
          <span>Q2 完成</span>
          <span>覆盖 100% 服务项</span>
        </div>
      </div>
    </div>
    <div class="timeline-item priority-mid">
      <div class="timeline-marker">P2</div>
      <div class="timeline-content">
        <h3>绿色办公认证</h3>
        <p>推进 LEED O+M 认证，支撑公司 ESG 战略</p>
        <div class="timeline-meta">
          <span>Q3 提交</span>
          <span>行业标杆</span>
        </div>
      </div>
    </div>
  </div>
</div>
```

---

## 4. 响应式断点

```css
/* 桌面端优先 */
.container { max-width: 1200px; margin: 0 auto; padding: 0 2rem; }

/* 1440px+ (大屏) */
@media (min-width: 1440px) {
  .container { max-width: 1320px; }
  .kpi-number { font-size: 3.5rem; }
}

/* 1366px (标准笔记本) */
@media (max-width: 1366px) {
  .container { max-width: 1100px; }
}

/* 1024px (小屏笔记本 / 平板横屏) */
@media (max-width: 1024px) {
  .hero-kpis { grid-template-columns: repeat(3, 1fr); }
  .insight-card { flex-direction: column; }
}

/* 768px (平板竖屏) */
@media (max-width: 768px) {
  .container { padding: 0 1rem; }
  .hero-kpis { grid-template-columns: 1fr; }
  .kpi-number { font-size: 2.25rem; }
}
```

---

## 5. 打印样式

```css
@media print {
  @page { size: A4; margin: 2cm; }
  body { font-size: 11pt; color: #000; background: #fff; }
  .hero { background: #fff !important; color: #000 !important; }
  .hero-kpis { border: 2px solid #000; }
  section { page-break-inside: avoid; }
  .outlook-section { background: #f0f0f0 !important; }
}
```

---

## 6. 动效规范

- **入场动画**：使用 `Intersection Observer` 驱动，Section 进入视口时触发
- **动画类型**：仅使用 `fadeInUp`（上移+淡入），保持职业感
- **动画时长**：`600ms ease-out`
- **禁止**：弹跳、旋转、缩放等花哨动画
- **数据数字**：支持 `countUp` 效果（进入视口时从 0 滚动到目标值）

```css
.animate-on-scroll {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 600ms ease-out, transform 600ms ease-out;
}
.animate-on-scroll.visible {
  opacity: 1;
  transform: translateY(0);
}
```

---

## 7. HTML 骨架模板

完整 HTML 模板的结构如下（生成时按实际内容填充）：

```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>2025年度成果汇报 - 行政与园区运营部</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;600;700;800&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <script src="https://unpkg.com/lucide@latest"></script>
  <style>
    /* 所有 CSS 内联 */
  </style>
</head>
<body>
  <!-- Hero -->
  <!-- Section 1-5 -->
  <!-- Footer -->
  <script>
    // Intersection Observer
    // CountUp
    // 议题树展开/收起
    // Lucide 图标渲染
  </script>
</body>
</html>
```
