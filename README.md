# Rough Handwriting Notes

将笔记或作业图片转换为 **黑底白字、稚拙或明显潦草的学生手写风格** 的 Codex skill。

“再丑一点”会增加字形不均衡、基线起伏、间距差异和徒手线条感；公式、表格与图的语义需要单独核对。它不是解题工具，也不把“字体变丑”当作内容可以出错的理由。

## 安装

将本仓库复制到宿主扫描的 skills 目录。Codex 默认示例（目标不存在时）：

```bash
git clone https://github.com/Melon1234123/rough-handwriting-notes.git ~/.codex/skills/rough-handwriting-notes
```

如设置了 CODEX_HOME，改用该目录下的 skills。已有同名目录时先比较版本，不要直接覆盖。安装文件后，新开会话或刷新 skills 清单。

本 skill 也收录在 [Skillls](https://github.com/Melon1234123/Skillls/tree/main/skills/rough-handwriting-notes)。

## 使用

附上要修改的图片，然后说：

> 使用 $rough-handwriting-notes，把这几张改成黑底白字，重新排版，像小学生写的。保留原文和状态图。

如果太漂亮：

> 还是太美了，再丑一点。字大小不一、歪一些，圈和箭头也不那么规整，但内容不变。

## 能力与边界

- 支持多页、中文与数学符号、表格、状态图，以及程度调整。
- 优先使用宿主内置的图片编辑能力；不会自动配置密钥或启用付费 API。
- 生成工具可能漏掉双圈、节点、标签或箭头尖；流程包含逐项视觉核对和局部修复，不能保证生成过程天然无误。
- 不自动纠正原答案，不模仿某个特定人的笔迹，不提交作业或公开用户输入。

仓库只包含可复用的指令和模板，不包含本次会话的原始截图、聊天记录或机器路径。

## 文件

- [SKILL.md](SKILL.md)：使用入口与执行流程
- [提示词模板](references/prompts.md)：初次编辑、加重潦草、局部修复
- [内容核对表](references/content-check.md)：文字、公式和有向图检查
- [agents/openai.yaml](agents/openai.yaml)：Codex 显示名称与示例提示
