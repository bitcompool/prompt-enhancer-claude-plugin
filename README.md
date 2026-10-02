# Prompt Enhancer for Claude

Turn a rough prompt or coding task into a clear, ready-to-send prompt.
Paste your draft and get one improved version back. It never runs the task,
and it sends nothing to Prompt Enhancer or any third party.

## Install

**Claude (web, desktop, mobile) and Cowork:** open Customize → Plugins,
search "Prompt Enhancer", and select Add.

**Claude Code:**

```
/plugin marketplace add bitcompool/prompt-enhancer-claude-plugin
/plugin install prompt-enhancer@promptgenerator
```

or from a terminal:

```bash
claude plugin marketplace add bitcompool/prompt-enhancer-claude-plugin
claude plugin install prompt-enhancer@promptgenerator
```

## Use it

Just ask. Claude loads the skill when you want a task or prompt enhanced:

```
Enhance this task before I give it to Codex: fix the crash when I click Save.
```

Or call it directly. This is the reliable route if you have many plugins and
Claude doesn't pick the skill up on its own:

```
/prompt-enhancer:enhance fix the crash when I click Save
```

You get one rewritten prompt, ready to copy. For coding tasks it returns an
agent-ready brief: the goal, where to look, constraints, how to verify, and
what to report back.

### Example

Draft: `Improve this prompt: translate "Good morning, is the shop open on
Sundays?" to French.`

Result: a short prompt that keeps your sentence exactly, asks for the natural
shop-door phrasing, and shows both the polite and the informal forms.

## The note after the first rewrite

After the first rewrite in a conversation, the plugin adds one short note with a
link to the Prompt Enhancer Chrome extension, made by the same developer as this
plugin. The extension goes through a prompt step by step with ready answers to
pick from. The note appears once per conversation, in the language of your
draft. The link (`https://promptgenerator.tools/go/store`) opens that page and
forwards to the Chrome Web Store; it is only text in the reply, and the plugin
sends nothing anywhere.

## What it does not do

- It does not answer or run the task in your draft.
- It does not ask you questions first. Gaps are handled inside the rewrite.
- It never invents names, dates or facts you didn't give.

## Privacy

This is a skills-only plugin: no server, no network calls, no account and no
credentials. Everything runs inside your Claude conversation.

## License

Apache-2.0
