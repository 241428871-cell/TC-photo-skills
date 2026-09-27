# TC-photo-skills

可持续扩展的照片艺术化 Skill 集合。每个风格都是独立子 Skill，可单独安装；集合入口负责列出风格、匹配需求并引导选择。

## 当前可选风格

| 风格 | 调用名 | 效果 | 适用场景 |
| --- | --- | --- | --- |
| [TC-photo-postcard-1](skills/tc-photo-postcard-1/SKILL.md) | `tc-photo-postcard-1` | 黑色细钢笔、通透淡彩、自然晕染、手写英文、原图四色卡 | 城市、旅行、日景、夜景与冷暖风景 |

完整选择目录：[STYLES.md](STYLES.md)。当前仅包含一个已实现的绘画风格。

## 安装与使用

向支持 Skill 的助手发送：

> 请安装 https://github.com/241428871-cell/TC-photo-skills 中的 tc-photo-skills 集合入口。

集合入口位于仓库根目录。使用 Codex skill-installer 时，根目录 path 为 `.`，name 为 `tc-photo-skills`。整个目录一起安装后，入口可以读取内置风格目录和子 Skill。

只安装单个风格时，指定路径 `skills/tc-photo-postcard-1`。

上传照片后可以说：

- “使用 $tc-photo-skills，列出当前可选风格。”
- “使用 $tc-photo-skills，选择 TC-photo-postcard-1 处理这张照片。”
- 独立安装后：“使用 $tc-photo-postcard-1，把这张夜景做成钢笔淡彩旅行手账。”

需要支持参考图编辑的图像生成工具。本项目提供提示词与工作流，不包含模型、API 密钥或独立绘图程序。没有可用图像工具时，助手应交付提示词并说明限制。

## 设计原则

- 遵循原图画幅比例，以主体辨识度和整体氛围为锚点。
- 画面与留白自然融合，避免硬边框或上下分区。
- 背景随日夜与冷暖氛围适配；四色卡只取原图主色。
- 用户的新要求优先于风格默认值。
- 生成式重绘不保证场景细节、色卡色值或尺寸逐像素精确。

## 添加新风格

1. 在 `skills/<lowercase-style-id>/SKILL.md` 编写独立风格。
2. 在 [styles.json](styles.json) 登记唯一 ID、显示名、路径、关键词、适用场景和风格摘要。
3. 同步更新 [STYLES.md](STYLES.md) 与本页风格表。
4. 为该风格提供清楚的工具要求、可覆盖默认值与质量检查；确认路径可解析。

新风格不改变旧风格的 ID。未实现的风格不列为可用。

## 来源与许可

TC-photo-postcard-1 根据用户提供并在夜景试作中选定的钢笔淡彩提示词整理。原始文字保存在子 Skill 的 references 中。本集合没有复制 photo-relic-editorial 的实现，也不依赖该 Skill。

MIT License，见 [LICENSE](LICENSE)。仓库不包含用户的原始照片、定位信息或个人素材；使用者应自行确认输入素材的使用权。
