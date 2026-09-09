# 黄博课题组指南写作 Skill

用于统一黄博课题组学生指南、操作教程和培养资料的内容风格与 Word 排版。适用范围包括入学须知、科研入门、软件使用、项目申报、简历、SCI 论文写作、实验方法及相关学习通材料。

## 主要约定

- 第一页顶部只出现一次“黄博课题组内部资料 请勿外传”。
- 内容务实、直接，先说明学生要做什么，再解释必要原因。
- 保留学生和合作团队材料中的具体经验，同时修正逻辑、重复和过时信息。
- 不虚构政策、奖励、日期、引用、实验结果或软件操作步骤。
- Word 默认白底黑字；中文楷体，英文与数字 Times New Roman；正文 12 pt；普通中文段落首行缩进 2 字符。
- 截图按真实操作顺序编排，每张图配 1–2 句话说明动作和预期结果。

完整规则见 [SKILL.md](SKILL.md) 及 `references/`。

## 安装

将仓库克隆到 Codex 的个人 Skills 目录：

```powershell
git clone https://github.com/huangbo19920528-ux/huangbo-group-guide-writer.git "$env:USERPROFILE\.codex\skills\huangbo-group-guide-writer"
```

安装后重新打开 Codex。创建或修改团队指南时，可以直接说明任务，也可以显式写：

```text
请使用 $huangbo-group-guide-writer 整理这份学生指南，并生成 Word。
```

## 同步更新

在每台电脑的 Skill 目录内运行：

```powershell
git pull
```

如果需要修改规范，应优先更新本仓库，再在其他电脑执行 `git pull`，避免不同电脑上的版本逐渐分叉。

## Word 生成器

仓库包含一个通用 DOCX 生成器，可根据 JSON 内容生成符合课题组版式的 Word 文件：

```powershell
python scripts/build_guide.py guide.json output.docx
```

JSON 结构见 [references/spec-schema.md](references/spec-schema.md)。生成后仍需渲染并逐页检查，确认没有重叠、孤行、异常分页或字体遗漏。


