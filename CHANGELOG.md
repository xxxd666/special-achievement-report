# Changelog

本项目的所有重要变更都记录在此文件。格式参考 [Keep a Changelog](https://keepachangelog.com/)，版本遵循语义化版本。

## [2.0.0] - 2026-06

### Added
- 新增**八大类汇报方法论**（在麦肯锡基线之外）：BCG、Bain、普华永道、德勤、亚马逊、谷歌 OKR、桥水/名人、金字塔之外（BLUF / STAR / Duarte 故事弧），每类独立文件、可插拔。
- 麦肯锡基线扩展为 **9 种 / 3 子类（叙事 / 结构 / 分析）组合使用**，默认组合 `SCQA + 金字塔 + MECE + 空雨伞`。
- 新增 `references/framework-selector.md`：按「汇报对象 × 场合 × 想要什么」推荐方法论组合，含拟人引导话术。
- 新增 `references/palette-preview.md` + **本地「配色总览参考」机制**：首次选配色时本地生成可视化样张，直观挑色。
- 新增 **Step 0 用户画像**：首次使用记录行业/岗位，存技能目录外的 `.md`（重装不丢），后续复用、不再重复问。
- 工作流新增「选方法论组合」一步，并新增「深度汇报版」横向 16:9 形态（与 PPT 同尺寸）。
- 新增 GitHub 发布物料：README、LICENSE、CHANGELOG、.gitignore。

### Changed
- 定位从「以麦肯锡为核心、面向职能部门」扩展为「**九大类方法论、面向所有管理者**」。
- `SKILL.md` 方法论章节由内联详解**收敛为九类速览表**，正文迁入 `references/frameworks/`，缓解上下文膨胀。
- `references/frameworks.md` 由麦肯锡深度参考**收敛为九大类总索引**；麦肯锡正文迁至 `references/frameworks/mckinsey.md`。
- `references/ppt-styles.md` 第三节补充**各方法论产物 → 版式映射**，并加「未装 guizang 时降级到深度汇报版」提示。

### Principles（确立两条最高优先级原则）
- **卖点是汇报思维，不是配色**：视觉是末端、可单独优化。
- **去 AI 味**：全程像资深汇报顾问，不堆术语、不暴露内部机制。

### Compatibility
- **向后兼容**：用户不指定方法论时，默认仍走麦肯锡基线组合，行为不变。

## [1.0.0]
- 初始版本：麦肯锡五件套（金字塔 / MECE / SCQA / 空雨伞 / 议题树）+ 三种输出形态（深度阅读 HTML / 电子杂志风 PPT / 瑞士风 PPT）。
