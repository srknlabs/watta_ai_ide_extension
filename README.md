<p align="center">Build features, fix bugs, and refactor across files in your editor.<br>
300+ AI models. One account. No separate provider API keys.</p>

<h2 align="center">Try 3 premium AI models for free</h2>
<p align="center">Create your Watta account and get temporary promo access.</p>

<p align="center">
  <a href="https://watta.io/register?utm_source=extension_readme&amp;utm_medium=referral&amp;utm_campaign=ide_promo"><img src="https://watta.io/apps/vscode/screenshots/20261015-readme-buttons/start-free.png" alt="Start for free" width="320"></a><br>
  <sub>No credit card required. Sign up in about a minute.</sub>
</p>
<p align="center"><sub>Quick sign-up with</sub><br>
  <a href="https://watta.io/register?utm_source=extension_readme&amp;utm_medium=referral&amp;utm_campaign=ide_promo_google"><img src="https://watta.io/apps/vscode/screenshots/20261015-readme-buttons/google.png" alt="Sign up with Google" width="196"></a>
  <a href="https://watta.io/register?utm_source=extension_readme&amp;utm_medium=referral&amp;utm_campaign=ide_promo_github"><img src="https://watta.io/apps/vscode/screenshots/20261015-readme-buttons/github.png" alt="Sign up with GitHub" width="196"></a>
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode"><img src="https://img.shields.io/badge/VS_Code-Install-007ACC?style=flat-square" alt="Install from VS Code Marketplace"></a>
  <a href="https://open-vsx.org/extension/watta-ai/watta-ai-vscode"><img src="https://img.shields.io/badge/Open_VSX-Install-a60ee5?style=flat-square" alt="Install from Open VSX"></a>
  <a href="https://watta.io/docs/ide/watta-extension"><img src="https://img.shields.io/badge/Quick_start-Guide-2dd4bf?style=flat-square" alt="Read the setup guide"></a>
</p>

<p align="center">Promo models rotate. Access is temporary and subject to current limits.<br>
Look for <strong>Temp access</strong> in the model picker before starting.</p>

## Get started

1. Open the **Watta** view from the Activity Bar.
2. Select **Connect Watta.io** and finish sign-in in your browser.
3. Open a workspace and write what you need in the composer: **“Describe what you want to build.”**
4. Review the result and keep or undo file changes when you are ready.

<p><a href="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/connect.gif"><img src="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/connect.gif" alt="Connect your Watta account and start a task in the extension." width="100%"></a></p>

<sub>Illustrative demos use the extension chat UI and a sample project. Click any animation to view it full size.</sub>

No provider API keys are needed: model access, subscription, Energy, and credits are handled through your Watta.io account.

## Describe it. Build it. Review it.

Give Watta a task in plain language. It can explore your open project, plan an approach, edit files, and help you verify the result. Review the changes in your editor and keep or undo them.

<p><a href="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/agent.gif"><img src="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/agent.gif" alt="Describe a feature and follow the Watta agent working on project files." width="100%"></a></p>

| Build a feature                       | Fix a problem                                 | Understand your project                  |
| ------------------------------------- | --------------------------------------------- | ---------------------------------------- |
| “Add a contact form with validation.” | “Find why this test fails and fix the cause.” | “Explain how authentication works here.” |

Use **Agent**, **Ask**, or **Plan** in VS Code, VSCodium, Cursor, Windsurf, and compatible editors.

## How editing works

Watta is designed to make code changes understandable and recoverable:

1. The agent reads only the files relevant to your request and reports what it is doing.
2. When it edits a file, the updated content appears in the editor with change highlighting and a compact review in chat.
3. Choose **Accept all** to keep the staged result or **Revert all** to restore the previous content. Per-file controls are also available next to the changed code.
4. Before an agent terminal command runs, Watta asks for approval. You can allow it once or remember the choice for the current workspace.

<p><a href="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/review.gif"><img src="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/review.gif" alt="Inspect the highlighted changes and choose Accept all or Revert all." width="100%"></a></p>

Watta creates a local checkpoint before approved edits. Use **Watta.io: Restore Last Watta Checkpoint** if you need to roll back the last accepted change set.

## Inline code suggestions

**Turn them on once, then keep typing.** Inline suggestions are **off by default** on a fresh installation. Your choice is remembered across VS Code restarts and extension updates.

<p><a href="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/inline.gif"><img src="https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/inline.gif" alt="Enable optional inline suggestions and press Tab to accept suggested code." width="100%"></a></p>

1. Sign in to your Watta.io account.
2. Choose a paid or **Temp access** model in Watta chat. Suggestions are unavailable while a free chat model is selected.
3. Click **Watta** in the bottom status bar to enable suggestions. You can also run **Watta.io: Toggle Inline Suggestions** from the Command Palette.
4. Type in a code file. Suggested code appears as ghost text at your cursor; press **Tab** to accept it with VS Code's default keybindings.

Click **Watta** again to turn suggestions off. If the button opens chat, choose an eligible model there and return to your code.

Successful inline suggestions consume **Watta Energy or wallet credits**, using normal Watta Fim pricing. They appear as **Watta Fim** in [Logs](https://watta.io/dashboard/logs) and [Usage](https://watta.io/dashboard/usage).

Inline completion uses **Watta Fim**, independently of which eligible chat model you choose. It considers code before and after the cursor, the header of a large file, and relevant open files. Suggestions stop when you keep typing, so outdated results do not appear at a moved cursor.

If nothing appears, check that VS Code's **Editor: Inline Suggest: Enabled** setting is on, your workspace is trusted, and you are signed in. Run **Watta.io: Request Inline Suggestion and Show Log** to request a suggestion and open the output channel.

## Built for the project you already have

- **Project-aware AI agent.** Search and read relevant workspace files. Attach files or folders to focus the task where it matters.
- **Edits you can review and undo.** Inspect changes in your editor, accept or revert them, and restore a local checkpoint when needed.
- **Your choice of model.** Switch between Watta models and a catalog of 300+ models in the same account. The picker shows current access, pricing, and supported reasoning levels.
- **Inline code completion.** Get suggestions as you type and press **Tab** to accept. Suggestions are **off by default** and use Energy or wallet credits when enabled. [How suggestions work](#inline-code-suggestions).
- **Ask first, plan first, or build.** Use Ask to understand code, Plan to work through an approach, and Agent for tasks across files.
- **Stay in the flow.** Queue another request while Watta works, follow its progress, and review the result from chat.

Open an HTML file with **Watta.io: Preview Site** to see it inside VS Code, or enter a running localhost URL. Use **Watta.io: Suggest Next Edit** for a small follow-up suggestion you can review before applying.

## Workspace agent, MCP and browser

**Agent tools require Starter, Pro or Max and a compatible model with tool calling.** Free accounts can continue using Ask and eligible chat models, including temporary promo access.

- **Ask:** answers questions; compatible models on paid plans can search and read the project.
- **Plan:** investigates the project with read-only tools and proposes an implementation plan.
- **Agent:** the default mode for a new paid-plan setup. It edits files with reversible review, requests terminal approval, and checks its work. Unfinished or failed verification is reported explicitly.
- **Project rules:** reads `AGENTS.md`, `WATTA.md` and `.watta/rules.md`, including applicable nested `AGENTS.md` files.
- **MCP:** connect local stdio or remote Streamable HTTP servers through **Watta: MCP & Browser Tools**. Servers do not start automatically from repository configuration. External tool actions require approval.
- **Browser:** inspect pages, click, fill fields, read console errors and capture screenshots in an isolated Chrome profile. Screenshots are available only for models enabled for image input. Chrome must be installed on the machine running the extension.
- **Long commands:** local servers and other commands return control after about 1.5 seconds while they keep running. The agent can inspect output, check the final exit code, or stop its own command sessions. Running commands expire after 30 minutes and stop when cancelled or the extension shuts down.

Configure connections in VS Code user settings through the tools command. The model picker has one shared catalog without a separate Agent filter or name suffix. New models and changes to their routing or tool capabilities are checked automatically by the server before agent tools are enabled. Price-only changes do not rerun the checks. Availability is controlled by the Watta model catalog; switching models can change the available tools. Saved mode and model choices are retained.

<p align="center">
  <a href="https://watta.io/register?utm_source=extension_readme&amp;utm_medium=referral&amp;utm_campaign=ide_promo"><img src="https://watta.io/apps/vscode/screenshots/20261015-readme-buttons/start-free-compact.png" alt="Start for free" width="208"></a><br>
  <sub>No credit card required. Sign up in about a minute.</sub>
</p>

## Modes and context

| Mode      | Best for                                                             |
| --------- | -------------------------------------------------------------------- |
| **Agent** | Multi-step tasks: inspect, edit, and verify code in the workspace.   |
| **Ask**   | Explain a file, an error, or a piece of code without making changes. |
| **Plan**  | Get a concise implementation plan before asking the agent to edit.   |

The active file and cursor line are included as context when relevant. Pin a specific file or folder when it should take priority over the rest of the workspace.

## Model choice and Energy

The catalog is loaded from Watta.io, so new models, provider names, prices, and availability can appear without updating the extension.

- **Watta Free** is available for getting started.
- **Watta Lite, Pro, and Max** require a Starter plan or higher.
- Other paid models show whether they require a Starter plan and/or account credits.
- Reasoning effort is available as a separate control when the selected model supports it.

## Commands

| Command                                     | Description                                                              |
| ------------------------------------------- | ------------------------------------------------------------------------ |
| **Watta.io: Open Chat**                     | Focus the Watta.io chat view.                                            |
| **Watta.io: Add File to Chat**              | Pin the active file as priority context.                                 |
| **Watta.io: Sign In**                       | Connect your Watta.io account.                                           |
| **Watta.io: Sign Out**                      | Remove the local Watta.io session.                                       |
| **Watta.io: Restore Last Watta Checkpoint** | Restore the latest accepted edit checkpoint.                             |
| **Watta.io: Reset Workspace Approvals**     | Forget remembered file-edit and terminal permissions for this workspace. |

## Settings

- `wattaAi.agent.maxSteps` — default: `24`. Maximum agent steps for one request.

- `wattaAi.agent.enableTerminal` — default: `true`. Allow the agent to request terminal commands. Every command still needs approval unless you explicitly remember it for the workspace.

- `wattaAi.inlineSuggestions.enabled` — default: `false`. Enable Watta Fim inline completions. The Watta status-bar toggle updates this setting. VS Code’s `editor.inlineSuggest.enabled` must also be enabled. Requires sign-in and an eligible chat model.

- `wattaAi.apiBaseUrl` — default: Watta.io API. Advanced: override the Watta API endpoint.

- `wattaAi.authorizationUrl` — default: Watta.io authorization. Advanced: override the sign-in endpoint.

## Privacy and security

- Watta uses OAuth Authorization Code with PKCE.
- Access and refresh tokens are stored only in VS Code `SecretStorage`; they are never exposed to the chat webview.
- Your prompt, selected model, workspace paths, active-editor context, attached resources, and file content needed for a request may be sent to Watta.io to generate a response.
- Optional onboarding and product measurements respect both VS Code telemetry settings and `wattaAi.telemetry.enabled`. Anonymous onboarding events include a random installation ID, editor category, extension version, sign-in steps and outcomes. They never include code, prompts, paths, account details, OAuth codes or error messages. Product events are sent after sign-in. See `docs/onboarding-analytics.md` for the server ingestion contract.

Read the full [Privacy Policy](https://watta.io/privacy) and [Terms](https://watta.io/terms). For private security reports, contact [Watta.io support](https://watta.io/contact).

## Requirements

- Visual Studio Code `1.90` or newer.
- A Watta.io account and an internet connection.
- A local or remote workspace for workspace tools. Terminal and Git operations require an environment that supports the VS Code Node.js Extension Host.

## Support

Need help, have product feedback, or want to report a security issue privately? Contact us through [Watta.io support](https://watta.io/contact).

Agent compatibility is checked automatically for new or changed tool-capable models and for eligible older models whose Agent capability has not been enabled. Pending checks are shown separately from unsupported tools; the extension refreshes server capabilities before every request.

## GitHub downloads

Download tested VSIX builds from [GitHub Releases](https://github.com/srknlabs/watta_ai_ide_extension/releases). This repository is the public product page and release channel. The extension source code is proprietary and is not published here. All rights reserved © 2026 Watta.io.
