# Paper Novelty Design

`paper-novelty-design-v1` 是一个用于论文创新点设计与审查的 Codex / Claude Skill。

它适合以下场景：

1. 把模糊研究想法整理成 `Problem-Method-Insight`
2. 判断一个想法是否接近伪创新
3. 设计可证伪命题与对应实验
4. 生成正式的 contribution statement
5. 维护创新点演化日志

## 目录结构

- `SKILL.md`：Skill 主工作流
- `agents/openai.yaml`：显示名与默认提示
- `references/`：审查规则与写作模板
- `example/`：输入模板、输出模板、合并示例和真实 PDF 案例
- `使用说明-v1.md`：中文使用说明

## 快速开始

显式调用示例：

```text
Use $paper-novelty-design-v1 to rewrite my idea into Problem-Method-Insight and pressure-test its novelty.
```

中文调用示例：

```text
使用 $paper-novelty-design-v1，帮我把下面的论文想法整理成 Problem-Method-Insight，
并检查它是否属于伪创新、是否可证伪、是否能写成正式 contribution。
```

## 作者

lavineleo
