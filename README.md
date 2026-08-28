# align-business-delivery

面向存量业务系统和复杂业务功能的 AI 交付对齐 Skill。它帮助 AI 在开始实现前核对现有系统事实，持续区分需求、原型、业务契约、代码和验证证据，减少范围漂移、原型丢失和多线程交接偏航。

## 它解决什么问题

- 需求、原型和现有页面逐步演进后，执行线程误用旧口径。
- 长线程中断或派生后，AI 丢失当前任务边界和最新纠偏。
- 多个模块、客户端或仓库并行开发时，前置依赖和完成状态混淆。
- 代码、编译、运行服务和页面验收被错误地当成同一层完成证据。
- 新项目没有文档，或旧项目文档失修，使用者不知道应维护哪些最小有效材料。

## 它不替代什么

本 Skill 不替代通用 TDD、调试、代码审查、Git 工作流、任务调度、项目管理或专业产品设计能力。它补充的是业务事实核查、来源裁决、原型/代码对齐、范围控制、交接恢复和真实交付证据。

## 快速安装

```powershell
git clone --branch v0.3.0-rc.1 https://github.com/RidingWind18/align-business-delivery.git
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { "$env:USERPROFILE\.codex" }
Copy-Item -Recurse -Force `
  .\align-business-delivery\skills\align-business-delivery `
  "$codexHome\skills\align-business-delivery"
```

安装后重新打开 Codex 会话，或按当前工具的 Skill 刷新方式重新加载。

其他 AI 工具可以读取 `skills/align-business-delivery/SKILL.md` 和 `references/` 作为规则材料，但 `agents/openai.yaml` 和自动发现行为属于 Codex 侧元数据。

## 最小使用示例

```text
$align-business-delivery

请基于当前项目现有代码、页面和文档分析这个功能，先判断是局部修复、模块改造还是跨模块变更；对不确定内容分类，不要自行扩大范围。
```

复杂功能仍应提供项目路径、现有页面或原型、已确认口径和明确排除项；Skill 会根据风险选择轻量或完整路径。

## 文档

- `skills/align-business-delivery/`：可安装 Skill。
- [`docs/zh-CN/使用与方法说明.md`](docs/zh-CN/使用与方法说明.md)：中文使用场景、能力边界和文档基线诊断说明。
- `CHANGELOG.md`：版本变化。
- `SOURCE.md`：公开仓库与私有演进源的关系。
- `CONTRIBUTING.md`：问题反馈和贡献边界。

## 版本

公开仓库使用语义化版本和 GitHub Release。当前候选版本为 `v0.3.0-rc.1`。安装时建议固定到 tag，不要直接跟随 `main`。

## License

本项目使用 [MIT License](LICENSE)。
