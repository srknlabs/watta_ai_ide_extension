# 0.18.125

- Refresh the sign-in screen with the color logo, free access to three premium models, and Chat & Work, Remote Telegram App and model catalog benefits.
- Use contrasting sign-in buttons in light and dark themes and turquoise benefit icons.
- Measure onboarding steps before sign-in while respecting editor telemetry preferences. Preserve anonymous attempt IDs for website attribution; never send code, prompts, account details or OAuth secrets in onboarding events.
- Avoid showing the sign-in screen while a saved session is loading.

# 0.18.124

- Refresh the marketplace title and description for 300+ AI models and rotating free promo access to three paid models.
- Lead the README with the registration offer and provide separate VS Code Marketplace and Open VSX installation links.

# 0.18.123

- Use the standalone Watta mark in the chat header and welcome screen.

# 0.18.122

- Use the standalone Watta mark in the model filter instead of the square application icon.

# 0.18.121

- Choose one of four localized thinking labels for each response, keeping it stable throughout the request.

# 0.18.120

- Speed up the working-logo animation to a two-second cycle and use dark lettering for clearer contrast on the turquoise tile.

# 0.18.119

- Move the animated Watta logo to the first activity block in the response, with friendly active and history labels.
- Keep the completed logo static and remove the duplicate activity header above the composer.

# 0.18.118

- Refresh the extension branding from the updated resource icons.
- Draw the dash and official W silhouette in sequence during active requests, with a brief cursor blink and a quiet repeat. Respect reduced-motion preferences.

# 0.18.117

- Animate the official Watta logo beside the active request status with a gentle pulse and tilt. Respect reduced-motion preferences and remove the animation when the request ends.

# 0.18.116

- Allow selecting the model, mode, and reasoning effort while an agent request runs. The active request keeps its original settings; new queued requests use the selected settings.

# 0.18.115

- Show the agent’s brief progress explanations before tool calls, separately from the final answer.
- Move technical steps into a collapsed work log in each response; keep only the current status above the composer while a request runs.
- Preserve progress explanations in chat history and stop animating activity after completion or interruption.

# 0.18.114

- Add optional authenticated product measurements for the marketing dashboard, respecting editor telemetry settings. No prompts, code, file paths, or raw errors are collected.

# Changelog

## 0.18.113

- Start the composer at one line, grow to three lines, then scroll.
- Explain interrupted connections and stop displaying failed tasks as running.

## 0.18.112

- Display subscription names from the admin catalog, including Max for the studio plan.

## 0.18.111

- Allow agent proposals to populate existing empty files while protecting nonempty files.
- Request a concrete edit tool call after a premature final answer and at the final edit step.
- Clarify the tool format for creating and filling files.
- Display completed file reads as “Read” instead of implying the whole task is done.

## 0.18.110

- Use Watta Fim branding consistently in suggestion status text and documentation.

## 0.18.109

- Use a code icon when inline suggestions are off and clarify the status-bar tooltip.
- Explain Codestral suggestion billing and link to Logs and Usage in the README.

## 0.18.108

- Codestral-only inline suggestions through Watta FIM with richer prefix, suffix, file header and related open-file context.
- Remove the 24-token, 160-character and 2-second completion cutoffs; preserve multiline code and cursor cancellation.
- Avoid duplicate closing punctuation when completing partial HTML tags.

## 0.18.107

- After accepting an inline suggestion with Tab, request one short continuation at the new cursor. Cancel deferred continuation when editing, moving the cursor, switching documents/models, disabling suggestions, or disposing the service; preserve API backoff and latest-request cancellation.

## 0.18.106

- Log the upstream FIM model, prefix-cache hit, and token count for each inline suggestion, and explain in the log when no FIM model is configured in the Watta admin.
- Security: restrict `wattaAi.apiBaseUrl` and `wattaAi.authorizationUrl` to application scope so a workspace cannot override them, and validate both at activation — only HTTPS `watta.io` hosts are accepted, otherwise the built-in default is used and a warning is shown.
- Keep the signed-in session alive: a transient network error during token refresh no longer clears stored tokens or signs the user out. Only a rejected grant (400/401/403) ends the session.
- Reuse the stored refresh token when the server omits a new one, and cache tokens in memory with a single-flight refresh so parallel requests share one token call.
- Route inline suggestions through the dedicated streaming FIM endpoint (`POST /v1/completions`) with the fixed `watta/watta-fim` alias. The upstream model is chosen in the Watta admin and can change without an extension update.
- Stream completion deltas and stop the request after two seconds; reduce the typing pause to 100 ms and remove the post-success request interval.
- Update the status bar tooltip, README, and localized setting descriptions to describe the FIM model instead of a fixed chat model.

## 0.18.105

- Disable inline suggestions by default. They can still be enabled from the Watta status bar or extension setting.

## 0.18.104

- Disable Qwen3 thinking mode for inline completion so the small output budget is used for code.
- Keep the 24-token output limit and wait for Qwen's response without a two-second timeout.

## 0.18.103

- Use only `watta/qwen3-32b` for inline suggestions, regardless of the chat model.
- Disable Qwen3 thinking mode, limit generated output to 24 tokens, and remove the two-second response timeout.
- Keep one request active and discard stale results after edits before requesting the latest line.

## 0.18.102

- Use MiMo V2.6 Flash for all inline suggestions based on live server timings (about 0.5–1.35 seconds versus 1.7–7.5 seconds for DeepSeek in the reported session).
- Do not abort the upstream request when the document changes. Wait for the single active server request to finish, then automatically request the newest line; this prevents repeated edits from stacking slow provider requests.
- Stop waiting in the editor after two seconds while keeping the background request tracked until the server finishes.

## 0.18.101

- Route inline completions through MiMo V2.6 Flash, which had lower live latency than DeepSeek in recent IDE usage.
- Keep the newest line queued while an earlier server request finishes, then trigger the latest completion without stacking requests.
- Preserve Temp access eligibility, keep free selections disabled, and cap how long the editor waits at two seconds.

## 0.18.100

- Route inline suggestions through two measured low-latency paid models. Slow chat models use DeepSeek V4.1 Flash for suggestions; the chat model itself stays unchanged.
- Reduce the typing pause to 250 ms, request up to 32 tokens with low reasoning, and stop requests after 3.5 seconds so late suggestions do not interrupt typing.
- Keep one request in flight and reuse its result when VS Code refreshes the inline provider.

## 0.18.99

- Disable inline suggestion requests when a free model is selected; the status bar opens chat to choose a paid model.
- Keep suggestions to one short fragment in the current line or block, reject duplicate HTML closing tags, and remove code already present after the cursor.
- Log the response time for each completed suggestion.

## 0.18.98

- Use the model currently selected in chat for inline suggestions, and remember that selection across webview reloads.
- Request one short line with a 64-token output limit and a smaller code context; reject explanatory text instead of showing it as code.
- Start suggestions after 600 ms of idle typing for selected models. Watta Free retains a longer pause to limit slow automatic requests.

## 0.18.97

- Offer inline suggestions on blank lines when surrounding code provides context, including after an HTML doctype.
- Avoid repetitive automatic logs for files with no useful context yet.

## 0.18.96

- Wait until typing has been idle for 1.2 seconds before starting an automatic inline suggestion, avoiding repeated requests for each keystroke.

## 0.18.95

- Cancel a pending inline suggestion when its document changes, allowing the next typed request to start without waiting for a stale response.
- Keep automatic request throttling messages out of the diagnostic log; manual requests still show why they cannot run.

## 0.18.94

- Keep an inline suggestion request running when VS Code cancels a provider invocation. Reuse and show its result if the file and cursor are unchanged.
- Report a clear timeout when a suggestion takes longer than 20 seconds.

## 0.18.93

- Label inline suggestions and next-edit requests separately so their Watta Energy usage appears as IDE suggestions in Spend by environment.

## 0.18.92

- Route short inline and next-edit requests through the buffered Watta API completion endpoint with small output limits. They no longer occupy long-running stream slots used by chat.

## 0.18.91

- Reduced the normal inline completion interval from eight to 2.5 seconds and the debounce to 350 ms.
- Added increasing pauses when the Watta API reports too many active long-running requests, and prevented overlapping suggestion requests.

## 0.18.90

- Inline suggestions now work inside a line, including between HTML attribute quotes.
- Automatic request cooldown begins after a completed response; canceled requests no longer consume it.

## 0.18.89

- Added a command to request an inline suggestion and show a diagnostic log with the reason no suggestion appeared.
- Increased the completion request timeout to 20 seconds.

## 0.18.88

- Fixed the inline suggestion toggle when VS Code has not refreshed the extension's settings registry after installation.

## 0.18.87

- Added a status bar toggle and command to make Watta inline suggestions easy to enable.
- Added site preview inside VS Code for the active HTML file or a running localhost site.
- Added next edit suggestions with review before applying. Automatic suggestions after saving are opt-in.

## 0.18.86

- Removed the Verify result button from staged edits.
- Replaced the model power select with a compact All button and a wider custom menu.

## 0.18.85

- Added short inline code suggestions from Watta Free, with cancellation, a request limit, and a setting to turn them off.
- Added **Verify result** to staged edits: inspect changed-file diagnostics and optionally run a project check script in a VS Code task.

## 0.18.84

- Kept the pricing activation icon beside the access label at the right edge of model rows, and sized and colored it to match Energy text.

## 0.18.83

- Refined the model picker controls: Watta logo filter, transparent search field, subtler filter backgrounds, Energy tint for Temp access, and an inline power icon linking to pricing for unavailable models.

## 0.18.82

- Fixed the model picker layout: filter buttons stay compact, the count and available filter share the header, model rows no longer overflow horizontally, and the activation link stays inline with model cost.

## 0.18.81

- Added model power, Watta, Temp access, and available model filters to the picker.
- Free users can identify and select eligible Temp access models, with the Free Energy estimate shown in the picker.
- Added a link to Watta pricing for models unavailable on the current account.

## 0.18.79

- The energy spent on an answer is now shown with the same bolt symbol used in the model picker, instead of a trailing "E" (for example `1⚡` rather than `1E`).

## 0.18.78

- Agent task names are now translated. Previously the task list always showed English titles such as "Analyzing request" because the strings were built in the extension host, which has no access to the webview dictionaries. The host now sends a task descriptor and the webview renders the label in the selected language.
- Fixed the Git changes tool being reported under an unlocalized name: the check compared the wrong tool name (`get_git_diff` instead of the registered `git_diff`), so its task and activity label were never matched.

## 0.18.77

- The model button in the composer now shows the provider logo instead of a generic spark, so the active provider is recognisable at a glance. Providers without a logo fall back to their initial letter.

## 0.18.76

- Opening a chat now restores the model that produced its latest answer instead of resetting to Watta Lite. The selection is resolved from local state, so opening a thread does not wait for a model refresh.
- New chats and the initial default now start from the first model in the picker (Watta Free) rather than Watta Lite, including remote prompts that arrive without an explicit model.

## 0.18.75

- Pinned chats in the Pinned tab now show an unpin icon instead of a pin icon, so the action matches what it does.
- Fixed the tab bar shifting to the centre and the list losing its left padding when the selected tab had no chats; every tab now keeps the same alignment.

## 0.18.74

- The session list now aligns with the toolbar, so its left edge lines up with the logo and the title instead of being indented.
- Added a Pinned tab to the session list. Pinned chats moved out of Recent into their own tab, and the list opens on Pinned automatically when pinned chats exist.

## 0.18.73

- Removed the duplicate loading spinner: the run now shows a single activity indicator instead of a reading spinner and a tool spinner at the same time.
- The active editor file chip no longer shows a pin icon, since the active file is not a pinned resource.
- Typing `@` in the composer opens a context menu that can insert the editor selection, current Problems, or the Git diff directly into the prompt.

## 0.18.72

- Completed chats are no longer lost: the session list now has "Recent" and "Completed" tabs, and a chat can be moved back from completed to recent.
- Replaced the ambiguous pin and check icons in the session list with a clear pin and an archive box.
- Watta Free no longer shows per-million token prices; only its Energy estimate is displayed, matching the other Watta models.

## 0.18.71

- Added syntax highlighting and a hover copy button to code blocks in chat answers; links in answers now open in the browser instead of inside the chat panel.
- The history button now opens the session list without discarding the open conversation, and the new-chat button is only shown when a chat is open.
- Fixed a duplicated expand control in the changed-files bar.
- Chat metadata now shows the model name instead of its raw identifier.
- Made long conversations noticeably lighter: finished messages are no longer re-parsed on every streamed chunk, model grouping is computed once per catalog change, and session state is written on a debounce instead of on every token.
- The composer input now grows with its content up to the theme limit.
- Completed the missing translations for German, French, Japanese, Chinese, Indonesian and Ukrainian, and added a CI check that fails when a locale is missing a key.
- Watta now declares that it requires a trusted, filesystem-backed workspace.

## 0.18.70

- Updated the Watta branding assets and extension icons.

## 0.18.69

- Added a per-run agent guard that stops repeated identical tool calls before they can loop and consume more requests.
- Added a total tool-call ceiling to stop alternating or continuously changing loops, with a clear recovery message in chat.

## 0.18.68

- Limited the IDE model catalog to models that can return text, while preserving multimodal text-output models and Watta routing engines.
- Added a defensive output-modality check so image, video, audio, embedding, reranking, and transcription-only models cannot appear in the coding model picker.

## 0.18.67

- Prevented edit requests from reporting success before a valid file-change proposal reaches review.
- Added recovery steps when an agent spends its normal budget on file discovery and kept edit tools available until a proposal is prepared.
- Marked incomplete edit runs as failed with an explicit message that no files were changed.

## 0.18.66

- Improved Remote Workspace session handling and delivery of remote prompts in the active IDE chat.

## 0.18.65

- Remote prompts from Watta Web and Telegram now open in the visible IDE chat with the selected model.
- Added current Watta Lite, Pro, and Max engine routing for remote work.
- Prevented duplicate remote messages when the IDE session is persisted.

## 0.18.64

- Added the secure Remote Workspace adapter for Watta Web and Telegram Mini App.
- IDE sessions now publish task state, approvals, questions, changed files, command progress, and final results.
- Remote prompts, stop/continue actions, and approval responses execute locally in the connected VS Code workspace.

## 0.18.63

- Added a chat timeline divider whenever a new request uses a different model, including the new model name and restored-session support.

## 0.18.62

- Center the active model vertically in the visible model list when opening the picker.

## 0.18.61

- Open the model picker at the active model with comfortable space above it.
- Simplified the model picker header by removing the logo and placing the title and model count at opposite edges.

## 0.18.60

- Sized model selectors without reasoning to their content instead of a fixed width, while retaining responsive ellipsis for long model names.

## 0.18.59

- Kept the model selector compact when the selected model has no reasoning control, while preserving responsive truncation for models with reasoning.

## 0.18.58

- Capitalized the account plan label and corrected spacing around the account separator.
- Added a subtle support shortcut beside Usage that opens the Watta.io contact page.

## 0.18.57

- Prevented long model and reasoning labels from overlapping in the composer by truncating each control with an ellipsis.

## 0.18.56

- Simplified selected-model styling to the left accent only and removed row rounding for a uniform provider model list.

## 0.18.55

- Reduced provider logo size, increased spacing before provider names, and render either a provider logo or fallback letter to prevent overlapping marks.

## 0.18.54

- Refined model picker pricing hierarchy and simplified provider logos by removing their framed containers.

## 0.18.53

- Replaced the Energy indicator below the composer with a localized link to Watta.io usage.

## 0.18.52

- Updated Watta branding assets and Marketplace icon.

## 0.18.51

- Allow Free-plan users to select paid third-party models when their Watta wallet has a positive credit balance; Watta subscription models remain Starter+ only.

## 0.18.50

- Keep model pricing and Energy together on one visible line, while placing plan and credit availability at the right edge.

## 0.18.49

- Rewrote the Marketplace README with a product overview, getting-started flow, safe editing model, model and Energy guidance, commands, settings, and privacy details.

## 0.18.36

- Replaced the large file changes card with a compact changes bar integrated above the chat composer, showing file count, +/− line stats, and Accept/Revert actions in a single toolbar row.
- Clicking the chevron or file count expands a scrollable list of changed files with per-file stats; clicking a file opens its diff.
- The changes bar appears only when there are pending proposals and disappears after accepting or reverting.
- Animated glow border on the composer activates when the agent is working (thinking, streaming, running tools, waiting for approval, or asking questions).
- The glow uses a small bright segment traveling along the border perimeter with mask-based rendering for proper visibility over the opaque background.
- Stop button uses theme-aware foreground color with no separator.
- Mode selector shows only the icon with a tooltip.
- All animations respect `prefers-reduced-motion`.

## 0.18.31

- Added a "Cancel authorization" link below the waiting message during sign-in, allowing users to reset a stuck auth flow.

## 0.18.19

- Aligned the “Sessions” title with the “Recent” section left edge.

## 0.18.18

- Removed the back arrow from the all-sessions screen.

## 0.18.17

- Reliably merge restored and persisted chat sessions so existing conversations do not disappear from “All chats”.
- Added hover-only Pin and Complete actions to each chat session; completed chats are archived from the active list without being deleted.

## 0.18.16

- Fixed opening the native diff from a staged change card by resolving the review ID correctly.

## 0.18.15

- Apply and save every agent file change immediately, while keeping it reversible until accepted or cancelled.
- Replace oversized inline code previews in the chat review card with compact, clickable changed-file rows.
- Open a native VS Code before/after diff from each changed-file row, with red/green changes and editor accept/undo controls.
- Made the queued-send menu button visible and keep its menu inside the chat panel.
- Render active editor context as a compact pinned file chip with its line number.

## 0.18.14

- Keep attached files and folders pinned across consecutive requests until they are removed explicitly.
- Added “Add File to Chat” to the editor-tab context menu and expanded editor-resource drag-and-drop support.
- Detect ambiguous same-named files before an agent request and ask the user to choose a path or enter a custom answer inline.
- Restore the active conversation, draft, history view, and exact scroll position when returning to Watta.io.
- Require workspace file discovery before the agent reports that a named file is missing.

## 0.18.13

- Fixed agent failures when a model provider returns tool arguments as an object instead of a JSON string.
- Normalize tool calls before adding them back to conversation history so subsequent provider requests remain valid.
- Recover from incomplete edit and terminal tool calls and let the model retry the step.
- Replace raw provider error payloads with concise user-facing messages.

## 0.18.12

- Apply and save trusted edits immediately while keeping a reversible review in the editor and chat.
- Let the agent finish its response without waiting for trusted edit confirmation.
- Added clear “Accept all” and “Undo all” actions and removed the extra diff button from the change log.
- Reworded agent activity into friendlier progress messages while retaining key file, search, and command details.
- Restored the composer placeholder to “Опишите, что нужно сделать”.

## 0.18.11

- Made concise, decision-focused answers the default to reduce output tokens and avoid filler.
- Limit standard final responses to a short result and up to six essential points; expand only on request.

## 0.18.10

- Show the active file and cursor line above each submitted chat message.
- Keep the active editor reference alongside manually attached files and refresh it as the cursor moves.

## 0.18.9

- Improved AI answer readability with a concise structured Markdown response format.
- Refined chat typography for paragraphs, headings, lists, code, quotes, and comparison tables.

## 0.18.8

- Keep trusted file edits staged in the editor until they are explicitly accepted or cancelled.
- Show staged edit highlights and `Apply Watta change` / `Cancel Watta change` controls directly in changed files.
- Keep the changed-file list and save/cancel review card in chat even when file-edit approval is permanent.
- Turn the first “Always allow edits” choice into the same staged review instead of saving it immediately.

## 0.18.6

- Render user-provided multi-line and fenced code as compact expandable code blocks.
- Replace repeated agent tool logs with one live activity status.

## 0.18.5

- Fixed review-card layout for long file paths: paths truncate cleanly and the diff action stays visible.

## 0.18.4

- Updated Marketplace artwork and extension icon.

## 0.18.3

- Added a request queue while the assistant is working, with queue-first sending and an “Apply immediately” option that stops the active request.
- Added a compact, removable queue preview above the composer.
- Reject stale edit proposals before review and ask the agent to re-read the current document.
- Save agent-edited documents that were clean before the approved change while preserving unrelated unsaved user work.

## 0.18.2

- Added workspace-scoped “Always allow” choices for file edits and terminal commands, with separate trust scopes and a reset command.
- Added native VS Code diff previews for proposed edits plus compact changed-file and line summaries in chat.

## 0.18.1

- Added a metadata-only workspace tree to agent requests and strengthened anti-hallucination instructions for project facts.
- Persisted IDE chat sessions in VS Code workspace storage.
- Added configurable agent step and terminal limits plus symlink boundary checks.
- Completed Marketplace metadata, security/privacy documentation, tests, CI, and dependency audit.

## 0.18.0

- Added a multi-step coding agent with workspace search, file reading, diagnostics, and Git diff tools.
- Added inline approvals for file edits and terminal commands.
- Added automatic checkpoints and a restore command for approved edits.
- Added compact tool activity in chat and native streamed tool-call support in the Watta.io API.
- Reduced initial workspace data transfer by reading files on demand in Agent mode.

## 0.17.0

- Added workspace-aware context, pinned files and folders, drag and drop, inline external-file permissions, improved chat rendering, model catalog, reasoning controls, voice input, localization, and Watta Energy display.
