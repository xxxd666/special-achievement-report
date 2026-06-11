# 发布到 GitHub：怎么获得更多关注

> 这份是给作者（你）看的发布攻略，不随技能功能影响用户。核心思路：**降低理解门槛 + 放大"我也需要"的共鸣 + 让人一眼看到成品。**

## 一、发布前清单（必做）

- [ ] 确认 README 里 guizang-ppt 依赖地址正确（https://github.com/op7418/guizang-ppt-skill）
- [ ] 截图：`docs/banner.html` → `banner.png`（1280×640）；实际生成一份汇报，截封面/KPI 页 → `docs/screenshots/`
- [ ] 取消 README「📸 截图」里的图片注释
- [ ] GitHub 仓库 Settings → **Social preview** 上传 banner.png（分享时显示大图，点击率翻倍）
- [ ] 设置仓库 **About**：一句话描述 + Topics 标签
- [ ] 确认 `.gitignore` 生效，没把个人数据/画像传上去

## 二、仓库名 & 一句话描述（决定第一眼）

- 名称建议：`special-achievement-report`（英文，利于搜索）或加中文副标。
- About 一句话（直接抄）：
  > 让任何人都能做出咨询公司级的成果汇报 · 9 大方法论 · 一个 Claude 技能

## 三、Topics 标签（GitHub 靠这个被搜到，尽量填满）

```
claude  claude-skill  anthropic  ai  productivity  presentation
report  storytelling  mckinsey  consulting  pyramid-principle
okr  chinese  办公  汇报  ppt
```

## 四、README 的黄金前三屏（已实现，保持）

1. **一句话价值** + badges + banner
2. **30 秒上手**（复制即用的 prompt）
3. **先看效果**（成品截图）→ 让人马上看到产出，而不是读说明

> 经验：开发者仓库靠功能，**工具类/效率类仓库靠"我也需要"的共鸣 + 成品截图**。把 banner 和成品截图放在最显眼处。

## 五、扩散渠道（按性价比排序）

1. **即刻/小红书/朋友圈**：发一张 banner + 一句"做了个让任何人都能写出咨询级汇报的工具"，附成品截图。视觉类内容在这些平台传播最快。
2. **V2EX / 少数派 / 即刻「AI」圈**：写一篇"我怎么把年终汇报从 2 天压到 2 小时"的过程贴，技能作为结尾自然带出。
3. **Twitter/X #ClaudeSkills #AI**：英文一句话 + banner + 仓库链接。
4. **Reddit r/ClaudeAI**：发成品截图 + 简介。
5. **Anthropic / Claude 技能相关的 awesome-list**：提 PR 把自己加进去。

## 六、内容钩子（标题党但真实）

- "做得多 ≠ 说得清：我用 9 套咨询方法论做了个汇报神器"
- "年终汇报从 2 天到 2 小时：一个 Claude 技能"
- "麦肯锡、BCG、亚马逊怎么做汇报？我把它们做成了一个工具"

## 七、可持续维护（留住 Star）

- CHANGELOG 持续更新，让人看到在迭代。
- Issues 模板：让用户提"想要哪个行业的案例 / 哪套方法论"。
- 每加一个行业案例或方法论，发一次更新动态。
