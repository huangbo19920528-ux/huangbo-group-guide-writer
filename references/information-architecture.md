# Information Architecture

## Default placement

Use a small number of top-level learning-platform folders. A practical default is:

```text
01 入学须知
02 科研入门
03 项目申报
04 求职与职业发展
05 案例与拓展资料
```

Adapt the names to the user’s current structure instead of duplicating similar branches.

Examples:

- Course-selection advice and basic group norms usually belong under 入学须知.
- VPN, GPT, literature management, Origin, research-document formatting, experiment methods, and academic writing usually belong under 科研入门.
- Project application guidance belongs under 项目申报, while a student resume guide belongs under 求职与职业发展.

## Splitting a large subject

When a subject grows, use four layers:

1. One overview document that explains the whole process and links the parts.
2. Focused guides for tasks that students perform independently.
3. Reusable templates and checklists.
4. Cases and optional references stored separately from required instructions.

Do not create a separate folder for every short note. A new branch is justified when the material has its own users, inputs, operating steps, or deliverable.

## Academic writing example

```text
学术论文写作
├─ 01 SCI论文写作总目录与写作流程
├─ 02 SCI论文各部分写作
│  ├─ 论文故事与图表规划
│  ├─ Methods写作
│  ├─ Results写作
│  ├─ Discussion写作
│  ├─ Introduction写作
│  ├─ Conclusion写作
│  └─ Title Abstract与Keywords写作
├─ 03 论文整合检查与投稿
│  ├─ 英文学术表达与段落修改
│  ├─ 图表格式与全文排版
│  ├─ 引用与参考文献
│  ├─ SCI论文提交前检查
│  ├─ 期刊选择与投稿
│  └─ 回复SCI审稿意见
└─ 04 案例与拓展资料
```

Specific experiment and characterization guides such as XRD and SEM should live in a separate 实验与表征方法 branch. Link them from Methods, Results, and Discussion rather than embedding the full procedures in the writing guide.
