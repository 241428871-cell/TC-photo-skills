# 可选风格

| 调用名 | 风格 | 画幅 | 是否包含原片 |
| --- | --- | --- | --- |
| [tc-photo-postcard-1](skills/tc-photo-postcard-1/SKILL.md) | 钢笔淡彩旅行手账 | 原图比例 | 否 |
| [tc-photo-postcard-2](skills/tc-photo-postcard-2/SKILL.md) | 独立动态版画 | 原图比例 | 否 |
| [tc-photo-postcard-3](skills/tc-photo-postcard-3/SKILL.md) | 独立艺术重绘 | 原图比例 | 否 |
| [tc-photo-postcard-4](skills/tc-photo-postcard-4/SKILL.md) | 超简记忆版画 | 原图比例 | 否 |
| [tc-photo-postcard-5](skills/tc-photo-postcard-5/SKILL.md) | 原片＋动态版画对半海报 | 3:4 竖版 | 是，上半部 50% |

## 怎么选

- 钢笔淡彩、手写英文和四色卡：1。
- 小主体配庞大动态场、两至三色印刷：2。
- 保留较多景物结构与前后层次的独立重绘：3。
- 极少笔触、几何化主体与大留白：4。
- 明确要求原片和版画上下各半：5。

选择后使用对应的 `$tc-photo-postcard-N`；集合入口可用 `$tc-photo-skills`。只要明信片时，不默认启用 5。连续修改沿用用户已确定的风格及“只输出明信片”等偏好；用户明确选择其他版式时再切换。

机器目录见 [styles.json](styles.json)。后续新增风格继续编号，不改变既有 ID。
