# Prompt Enhancer plugin for Claude (skills-only)

Prompt Enhancer rewrites a draft prompt or coding task into a clearer,
agent-ready prompt and returns that one rewritten prompt as plain text. It
never executes the task, never answers the underlying question, and never
runs the rewritten prompt on the user's behalf.

## How to use it

There is no setup and no command to run. Claude loads this skill
automatically whenever the situations described in the skill's frontmatter
`description` apply — for example when the user asks to improve, rewrite,
sharpen or "enhance" a prompt, a spec, or a coding task before sending it to
an AI or a coding agent. The full rewrite contract is in
`skills/prompt-enhancer/references/rewrite-rules.md`, with worked examples in
`skills/prompt-enhancer/references/examples.md`.

## What data it sends

This is a skills-only plugin: no `.mcp.json`, no MCP server, no network call,
no account and no credential. Everything runs inside the Claude conversation
itself. Nothing about the user's draft, or anything else, is sent to Prompt
Enhancer's backend or to any other service.

## Relationship to the ChatGPT/Codex package

This package is the Claude counterpart to the existing skills-only
ChatGPT/Codex plugin at `plugins/prompt-enhancer/` in this repository. It
follows the same policy precedent recorded in
`docs/architecture/ADR-007-chatgpt-skills-plugin.md`: skills-only, no MCP
server, and one neutral note per conversation pointing at the Prompt Enhancer
Chrome extension, with no pricing or offer language.

## Status

This folder is prep only. Submission itself — creating the public GitHub
repository this plugin will live in, connecting that repository in the
Claude developer portal, and clicking Submit for review — is a pending
Product Owner action and has not been done.
