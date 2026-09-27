# TC-photo-skills

可扩展的照片艺术化 Skill 集合。每个风格可独立安装，集合入口保留可选风格列表与选择流程。每张输入照片独立输出一张作品，不做多图拼贴。

## 当前可选风格

| 调用名 | 风格 | 画幅 | 是否包含原片 |
| --- | --- | --- | --- |
| [tc-photo-postcard-1](skills/tc-photo-postcard-1/SKILL.md) | 钢笔淡彩旅行手账 | 原图比例 | 否 |
| [tc-photo-postcard-2](skills/tc-photo-postcard-2/SKILL.md) | 独立动态版画 | 3:4 竖版 | 否 |
| [tc-photo-postcard-3](skills/tc-photo-postcard-3/SKILL.md) | 独立艺术重绘 | 3:4 竖版 | 否 |
| [tc-photo-postcard-4](skills/tc-photo-postcard-4/SKILL.md) | 超简记忆版画 | 3:4 竖版 | 否 |
| [tc-photo-postcard-5](skills/tc-photo-postcard-5/SKILL.md) | 原片＋动态版画对半海报 | 3:4 竖版 | 是，上半部 50% |

[完整风格选择说明](STYLES.md) · [机器可读目录](styles.json)

2 与 5 使用同一动态版画思路，区别是是否保留上方原片。3 保留较多细节；4 是进一步收简的版本。默认尊重用户已确定的“只要明信片”偏好，不把原片自动拼回成品。

## 安装与使用

向支持 Skill 的助手发送：

> 请安装 https://github.com/241428871-cell/TC-photo-skills 中的 tc-photo-skills 集合入口。

集合入口在仓库根目录，安装 path 为 `.`，name 为 `tc-photo-skills`，需保留内置子目录。单独安装某个风格时使用 `skills/tc-photo-postcard-N`（N 为 1–5）。

上传照片后可以说：

- “使用 $tc-photo-skills，列出可选风格。”
- “使用 $tc-photo-postcard-2，只生成独立动态版画明信片。”
- “使用 $tc-photo-postcard-3，保留较丰富的层次进行独立重绘。”
- “使用 $tc-photo-postcard-4，处理成超简版画。”
- “使用 $tc-photo-postcard-5，生成原片与版画各占一半的海报。”

需要支持参考图编辑的图像生成工具。本项目提供提示词与工作流，不包含模型、API 密钥或绘图程序。没有图像工具时，助手应交付提示词并说明未生成。

## 设计原则

- 用户的明确要求和持续偏好优先于默认值。
- 画幅、配色、文字及是否包含原片由所选风格决定，不混用不同风格的限制。
- 每张照片分别查看、提炼和生成，示例主体不能固定套用。
- 重绘不保证细节、尺寸和排版逐像素精确；需要精确原片保留时须核验实际成品。

## 添加新风格

在 `skills/<style-id>/SKILL.md` 编写独立技能；在 styles.json 登记 ID、描述、路径、关键词与适用场景，并同步本页及 STYLES.md。校验路径与技能格式，保留现有 ID。

## 来源与许可

1 基于用户提供的钢笔淡彩提示词。2 与 5 基于用户提供的超现实动态版画提示词；5 的 SKILL.md 完整保留本次原始提示词。3 与 4 将本次独立重绘和进一步收简的生成经验整理为可复用提示词，其视觉探索参考了 [wnby/photo-relic-editorial](https://github.com/wnby/photo-relic-editorial) 的照片记忆版画思路。这里是本项目重新编写的技能，不捆绑上游技能文件，也不依赖其安装。

本集合按 [MIT License](LICENSE) 开源。上游项目保留其自身许可。仓库不附带用户原始照片、定位信息或私有素材。
