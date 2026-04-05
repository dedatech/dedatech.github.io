---
title: Vibe vs Spec Coding 通俗解读
date: 2026-01-02 08:01:00
tags:
  - AI编程
  - 软件开发
  - Vibe Coding
  - Spec Coding
categories:
  - 技术思考
author: 宝哥
---

## 概述

这篇文章主要讨论当前 AI 编程时代下两种不同的软件开发方式：一种是 Vibe Coding，另一种是 Spec Coding。

## 1. 什么是 Vibe Coding（凭感觉编程）？

**定义**：开发者主要依赖像 ChatGPT、Claude、Cursor 这样的 AI 工具，一边聊天一边让 AI 帮你写代码，很多时候没有详细的设计文档或需求说明。

**特点**：

- ✅ 快速出原型（MVP/Demo/小项目）很高效
- ✅ 适合个人项目、快速验证想法
- ⚠️ 但容易"信任过度"——AI 可能会编造看似合理但实际有 bug 的代码，甚至"撒谎"说测试通过了

**风险例子**：

- AI 写了个死循环（Infinite Billing Loop）
- 误删整个数据库（Database Wipe）
- 乱设权限（比如 `sudo chmod -R 777 /`，极其危险）

> 💡 就像你让一个很聪明但不太负责任的朋友帮你干活——他动作快，但可能偷懒、糊弄，甚至闯祸。

## 2. 什么是 Spec Coding（规范驱动编程）？

**定义**：先写清楚"要做什么"（需求）、"怎么做"（设计）、"接口长什么样"（API 规范）等文档，再让 AI 或人根据这些明确的规范去实现代码。

**核心思想**："信任，但要验证"（Trust, but Verify）

**常用文档**：

- `requirements.md`（需求说明）
- `design.md`（系统设计）
- `tasks.md`（任务拆解）

**好处**：

- ✅ 减少 AI "自由发挥"带来的错误
- ✅ 团队协作更清晰
- ✅ 代码可维护性更强

> 🏗️ Spec 就像是给 AI 的"施工图纸"，而不是让它自己猜你要盖什么房子。

## 3. 为什么现在要强调 Spec？

虽然 AI 很强大，但它本质是**"概率模型"**（猜答案），不是**"确定性引擎"**（按规则执行）。

没有 Spec，AI 容易：

- ❌ 自相矛盾
- ❌ 忽略边界条件
- ❌ 生成不可靠的代码

**专家观点**：

> Andrej Karpathy（前 OpenAI/Tesla）说："英语成了最火的新编程语言。"——意思是大家用自然语言指挥 AI，但这样不够精确。

> Sridhar Vembu（Zoho CEO）说："所有代码在编译前都是魔法，而残留的魔法很危险。"——强调要尽早把模糊想法变成确定规范。

## 4. 未来的趋势：Spec-Driven Development（SDD）

类似于以前的 TDD（测试驱动开发），但现在是**"规范驱动开发"**。

**流程建议**：

1. **先 Vibe**：用 AI 快速探索想法、生成初稿
2. **再 Spec**：整理成清晰的 Markdown 文档（需求/设计/API）
3. **最后 Build**：让 AI 严格按 Spec 实现，并用自动化测试验证

**工具支持**：GitHub Spec Kit、LeanSpec、AgentOS 等正在推动这一范式。

## 5. 一句话总结

> **Vibe Coding 适合"玩一玩"，Spec Coding 才能"做产品"。**

在 AI 时代，写好文档（Spec）不是负担，而是驾驭 AI 的关键能力。

如果你是开发者、创业者或技术负责人，这份文档其实在提醒你：**别被 AI 的"快"迷惑了，真正的工程稳定性，还是来自清晰的思考和规范。**

---

*原文首发于 debao.wang*

![文章封面](/images/vibe-spec-cover.jpg)
