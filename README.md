# Hazelchat for Gemini CLI

Check and improve your [Hazelchat](https://hazelchat.co) website agent from Gemini CLI: see what visitors asked, find the questions it couldn't answer, test answers against your draft and add missing answers for your review.

Built for agencies and developers who look after a website and its Hazelchat agent. Needs a Hazelchat account on a paid plan.

## Install

```bash
gemini extensions install https://github.com/hazelchat-co/gemini-extension
```

Restart Gemini CLI, then sign in:

```text
/mcp auth hazelchat
```

Your browser opens Hazelchat's sign-in page. Choose the workspace and what Gemini CLI may do. Contact details of visitors stay off unless you allow them. Sign-in needs a browser on the same computer, so it doesn't work over SSH or in a container.

## What it can do

- **Agent overview:** whether your agent is live, and counts for the last 7 and 30 days.
- **Unanswered questions:** what visitors asked that the agent had no source for.
- **Search conversations:** visitor questions matching a word, and how the agent answered.
- **Recent enquiries:** contact requests from the last 30 days.
- **Ask a test question:** asks your saved draft, like Test agent in Hazelchat. Uses one of your daily test answers.
- **Add an answer to the draft:** adds a Q&A or text snippet to your draft. Visitors see it only after you publish in Hazelchat.

It can't publish, change settings, websites or billing, delete anything, or read another workspace. In an interactive session Gemini CLI asks you before it runs a tool. In headless mode (`gemini -p`) the tools stay hidden unless you allow the server, for example with `--allowed-mcp-server-names hazelchat`, which lets every tool run without asking.

## Disconnect

Remove the connection in Hazelchat under Settings → AI assistants, and the extension with `gemini extensions uninstall hazelchat`.

## Without the extension

```bash
gemini mcp add --scope user --transport http hazelchat https://app.hazelchat.co/mcp
```

More: [hazelchat.co/docs/ai-assistants](https://hazelchat.co/docs/ai-assistants/)

## Data

What the tools return reaches Google under your own agreement with Google. Hazelchat's side is described in the [privacy notice](https://hazelchat.co/privacy/).

## Issues

Open a [GitHub issue](https://github.com/hazelchat-co/gemini-extension/issues) or write to hello@hazelchat.co.

MIT licence.
