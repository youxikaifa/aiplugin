# AI Agent Assistant for Android Studio

把AI Agent 工作流带到 Android Studio / IntelliJ IDEA。

## 一句话介绍

AI Agent Assistant 是一款面向 Android Studio / IntelliJ IDEA 的 AI 编码助手插件。它把常见 AI 对话、项目上下文理解、代码生成、文件修改审核和历史任务管理整合到 IDE 右侧工具窗口中，让开发者不用离开当前工程就能完成日常辅助编码。

## 适合谁

- Android 开发者：希望在 Android Studio 内完成解释代码、修复 Bug、生成类和重构建议。
- JetBrains IDE 用户：希望保留 IDE 原生编辑、Undo、安全写入和项目上下文。
- 团队开发者：希望 AI 生成的文件变更先进入审核，再由开发者确认应用。

## 亮点

- 多 Provider：DeepSeek、OpenAI、Claude、Ollama。
- Cursor 风格右侧工作台：任务首页、聊天详情、历史任务、底部 composer。
- Markdown 预览：标题、列表、引用、代码块、表格、链接均按文档风格渲染。
- 项目上下文：当前文件、选区、PSI 结构、模块信息、最近打开文件。
- Action Engine：支持 `insert_code`、`modify_file`、`create_file`，写入走 IntelliJ WriteAction 和 CommandProcessor，可 Undo。
- 安全边界：限制绝对路径和路径穿越，unified diff 应用会校验上下文。
- 授权码：发送消息前校验授权码，未配置时引导用户获取授权。

## 为什么值得试

很多 AI 编码工具会把代码上下文和文件写入流程藏在黑盒里。AI Agent Assistant 的思路更保守：模型可以给建议和生成操作，但真正写入工作区前，开发者能看到 action 摘要、文件路径和 diff payload。

它更适合日常工程场景：读代码、问架构、补测试、生成样板代码、做小范围重构。插件优先遵循 IDE 的原生能力，而不是绕过项目结构直接改文件。

## 快速开始

1. 安装插件并打开右侧 `AI Agent Assistant` 工具窗口。
2. 点击设置图标，配置 Provider、Model、API Key / Base URL。
3. 在 `授权` 分区填写授权码和授权服务地址。
4. 在当前项目中提问，必要时审核并应用 AI 生成的文件操作。

## 推荐示例提示词

```text
解释当前文件的职责，并指出可以简化的地方。
```

```text
为当前类补充一个最小单元测试，只生成必要代码。
```

```text
检查这个 Activity 的生命周期使用是否有潜在问题。
```

## 项目链接

- GitHub: 在仓库首页补充实际地址
- 授权获取: https://aiplugin.metoolkits.com
