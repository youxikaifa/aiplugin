# AI Agent Assistant for Android Studio

Bring the AI Agent workflow to Android Studio and IntelliJ IDEA.

## One-line Introduction

AI Agent Assistant is an AI coding assistant plugin for Android Studio and IntelliJ IDEA. It brings AI chat, project context understanding, code generation, file change review, and task history into a right-side IDE tool window, so developers can handle daily coding assistance without leaving the current project.

## Who It Is For

- Android developers who want to explain code, fix bugs, generate classes, and get refactoring suggestions inside Android Studio.
- JetBrains IDE users who want to keep native IDE editing, Undo, safe writes, and project context.
- Teams that want AI-generated file changes to be reviewed before developers apply them.

## Highlights

- Multiple providers: DeepSeek, OpenAI, Claude, and Ollama.
- Cursor-style right-side workspace: task home, chat details, task history, and bottom composer.
- Markdown preview: headings, lists, quotes, code blocks, tables, and links are rendered in a document-like style.
- Project context: current file, selected code, PSI structure, module information, and recently opened files.
- Action Engine: supports `insert_code`, `modify_file`, and `create_file`; writes use IntelliJ WriteAction and CommandProcessor, with Undo support.
- Safety boundaries: rejects absolute paths and path traversal; unified diff application validates context.
- License key: validates the license before sending messages and guides users to the license portal when no key is configured.

## Why Try It

Many AI coding tools hide code context and file writes inside a black box. AI Agent Assistant takes a more conservative approach: the model can suggest changes and generate actions, but before anything is written to the workspace, developers can inspect the action summary, target file, and diff payload.

It is designed for everyday engineering tasks: reading code, asking about architecture, adding tests, generating boilerplate, and performing small refactors. The plugin prioritizes native IDE capabilities instead of bypassing project structure and writing files directly.

## Quick Start

1. Install the plugin and open the right-side `AI Agent Assistant` tool window.
2. Click the settings icon and configure Provider, Model, API Key, and Base URL.
3. Fill in the license key and license service URL in the `License` section.
4. Ask questions in the current project, then review and apply AI-generated file operations when needed.

## Suggested Prompts

```text
Explain the responsibility of the current file and point out what can be simplified.
```

```text
Add a minimal unit test for the current class and generate only the necessary code.
```

```text
Check whether this Activity has potential lifecycle issues.
```

## Project Links

- GitHub: Add the actual repository URL on the repository homepage
- License portal: https://aiplugin.metoolkits.com
