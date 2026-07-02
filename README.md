<div align="center">

# Hi, I'm YaoKai

**AI Agent Runtime / Multimodal AI / Enterprise AI Assistant**

我关注如何把大模型能力做成真正可运行、可治理、可评测、可落地的 AI 系统：既能进入企业工作流，也能处理多模态交互、知识检索、风险识别和长期任务协作。

[![AI Agent](https://img.shields.io/badge/AI-Agent%20Runtime-6f42c1)](#)
[![Multimodal](https://img.shields.io/badge/Multimodal-AI%20Application-0f766e)](#)
[![Spring AI](https://img.shields.io/badge/Spring%20AI-Backend%20Agents-22c55e)](#)
[![TypeScript](https://img.shields.io/badge/TypeScript-Agent%20Platform-3178c6)](#)
[![Evaluation](https://img.shields.io/badge/Evaluation-Replay%20%26%20Scorecard-b45309)](#)

</div>

---

## About Me

我主要在做两类 AI 工程实践：

- **企业级 Agent Runtime**：让 AI 不只是在终端里回答问题，而是可以进入 IM、Dashboard、任务流、工具链、权限治理和成本中心，成为可协作的 AI 同事。
- **多模态 AI 应用**：把文本、语音、视觉、RAG、心理风险评估和工具调用组合到真实业务流程里，关注产品闭环与安全边界。

我喜欢把 AI 项目做成“可验证的系统”，而不是只展示一次漂亮回复。对我来说，Agent 项目应该同时具备：

- 清晰的 runtime 边界
- 可恢复的状态与记忆
- 可治理的权限与审计
- 可观测的 token 与成本
- 可回放的证据链
- 可评测的 benchmark / scorecard
- 能被普通用户理解的产品界面

---

## Featured Projects

### XiaoBa CLI

> 一个活在 IM、Dashboard 和本地工作区里的企业级 AI 同事运行时。

XiaoBa CLI 是一套面向企业 Agent 落地的本地优先运行时。它把飞书/微信/CLI/Dashboard/桌宠入口、AI 角色、Skill、Tool、Memory、Evidence、Cost、Audit、Benchmark 组织成一个可以持续演进的工程系统。

**我在这个项目里重点解决的问题：**

- 让 Agent 从“单次模型回复”升级为“有角色、有任务、有证据、有验收”的 AI 同事。
- 让不同 AI 同事承担不同职责：EngineerCat 负责实现，ReviewerCat 负责审查，InspectorCat 负责巡检，ResearcherCat 负责研究。
- 为企业落地补齐权限、成本、审计、状态外部化和评测闭环。
- 用 Dashboard 把 Issue Tracker、Skill Factory、Cost Center、Governance 和 Agent 工位卡做成可操作的控制台。

**核心能力：**

| 模块 | 能力 |
| --- | --- |
| IM-native Runtime | 支持 CLI、飞书、微信、Dashboard、桌宠等入口，任务从真实聊天场景发起。 |
| AI 同事体系 | EngineerCat、ReviewerCat、InspectorCat、ResearcherCat 等角色分工协作。 |
| Issue Tracker | 可配置任务阶段、任务类型模板、活动流、Agent DM prompt 和工位卡。 |
| Skill Factory | Skill 生产、测评、scorecard、发布、回滚、自进化草稿。 |
| Governance | tenant/workspace/user 身份贯穿、RBAC/ABAC、Tool 黑白名单、审计检索。 |
| Cost Center | token/cost 聚合、预算策略、异常告警、Skill/Role 质量指标。 |
| State Backends | Redis Session、MySQL Memory/Evidence/Audit、readiness check。 |
| Evaluation | product replay、skill eval、scorecard、SWE-bench pilot。 |

**技术栈：**

```text
TypeScript / Node.js / Electron / Express
AgentSession / ConversationRunner / ToolManager
Redis / MySQL / JSONL Evidence / Dashboard
Feishu / Weixin / CLI / Desktop Pet
Benchmarks / Replay / Scorecard / SWE-bench Pilot
```

---

### MultimodalAgent

> 一个面向校园心理健康场景的 Spring Boot 多模态 AI 助手。

MultimodalAgent 更偏业务应用层：它把聊天、心理风险识别、Agentic RAG、多模态输入和工具接口组合成一个校园心理健康助手原型。相比 XiaoBa 更偏 runtime/platform，这个项目更偏“多模态 AI + 后端业务系统 + 风险辅助决策”。

**项目关注点：**

- 面向校园心理健康问答、风险识别和辅助评估。
- 文本聊天、知识检索、心理测评、风险路由形成主业务链路。
- 结合 Spring AI、Ollama/OpenAI、Chroma、Redis、MySQL 等组件。
- 预留 Whisper 语音识别、MediaPipe 视觉分析、多模态输入与 MCP 工具接口。
- 使用 SSE 支持流式对话体验。

**核心链路：**

```text
用户输入
  -> ChatController
  -> ChatService
  -> 意图识别
  -> Agentic RAG / 心理评估 / 多模态风险信号
  -> LLM 生成
  -> SSE 流式返回
  -> 报告 / 记录 / 后续干预
```

**技术栈：**

```text
Java 17 / Spring Boot 3 / WebFlux / Spring Security
Spring AI / Ollama / OpenAI
JPA / Redis / MySQL / Chroma / Mailpit
SSE Chat / Agentic RAG / MCP-style Tools
WhisperClient / MediaPipeClient / Psychological Assessment
```

**工程价值：**

- 把多模态能力放进真实业务流程，而不是停留在单点 demo。
- 将 RAG、风险评估、短期记忆、报告生成和外部工具组织成可维护的后端服务。
- 关注心理健康类应用的安全边界、权限暴露、默认账号、MCP 暴露面和测试覆盖问题。

---

## Technical Focus

```text
AI Agent Runtime
Enterprise AI Assistant
Multimodal AI Application
Spring AI / LLM Backend
RAG / Knowledge Retrieval
Tool Calling / MCP
RBAC / ABAC / Audit
Token Cost Observability
Benchmark / Replay / Scorecard
```

---

## Engineering Style

- **先建 runtime，再接模型**：模型负责推理，runtime 负责状态、工具、权限、证据和恢复。
- **先有边界，再做能力**：Tool、Skill、Role、Tenant、User、Resource 都要有清晰边界。
- **先能评测，再谈优化**：复杂 Agent 任务必须能 replay、能打分、能回归。
- **先落业务，再做炫技**：多模态能力要进入真实链路，例如风险识别、报告生成、知识检索和人工干预。
- **先可观测，再长时间运行**：token、成本、日志、状态、错误和审计都要能被看见。

---

## What I'm Building Next

- XiaoBa 的多租户 Issue Tracker 和审批流
- Agent 工位卡与企业 IM / iOS 的实时同步
- Skill Factory 的可视化生产流水线
- 更强的 SWE-bench / product benchmark 自动修复能力
- 多模态 Agent 的安全治理、评测集和生产部署闭环
- Docker 安全沙箱与远程 Tool 执行隔离

---

## Contact

如果你也在关注 AI Agent、企业 AI 助手、多模态 AI 应用、Spring AI、RAG、Skill Factory 或 Agent 评测体系，欢迎交流。

</div>
