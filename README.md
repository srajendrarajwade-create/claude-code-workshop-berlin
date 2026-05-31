# Claude Code Workshop — Berlin

Welcome! In the next 2 hours you'll build and deploy your own website using Claude Code.

## What you'll build

Pick one of these starter templates:

- **`templates/portfolio/`** — personal portfolio (about, projects, contact)
- **`templates/landing/`** — small-business landing page (hero, services, contact)

By the end of the workshop, your site will be live on the internet at a Vercel URL you can share.

## Before the workshop

You should have received a setup email with the account checklist (GitHub, Claude, Vercel). If you missed it, ping the organizer.

## Getting started (during the workshop)

1. **Fork this repo** to your own GitHub account (top-right "Fork" button).
2. **Open in Codespaces**: on your fork, click the green "Code" button → "Codespaces" tab → "Create codespace on main". Wait ~60 seconds for the environment to boot.
3. **Pick your template** in the Codespace terminal:
   ```bash
   cd templates/portfolio   # or: cd templates/landing
   npm install
   npm run dev
   ```
4. Click the "Open in Browser" popup that appears (port 3000) — that's your live preview.
5. **Open Claude Code** in a second terminal:
   ```bash
   claude
   ```
6. Start chatting. Try: *"Change the headline to say 'Hi, I'm [your name]'"*

## Deploying to Vercel

This repo includes a `vercel.json` at the root that pre-configures the deploy:

- **Framework** — auto-selected as Next.js (no dropdown to pick)
- **Default template** — `templates/portfolio`

### To deploy

1. Go to [vercel.com/new](https://vercel.com/new) and import your fork
2. Click **Deploy** — no settings to change
3. ~60 seconds later, your portfolio site is live

### Deploying the landing template instead

Open `vercel.json` in your project (or ask Claude *"open vercel.json"*) and replace both occurrences of `templates/portfolio` with `templates/landing`:

```json
{
  "framework": "nextjs",
  "buildCommand": "cd templates/landing && npm install && npm run build",
  "outputDirectory": "templates/landing/.next",
  "installCommand": "echo 'Install runs inside the template directory during build.'"
}
```

Commit and push. Vercel auto-redeploys with the new template.

Easier route: just ask Claude:

> *"Update vercel.json so it deploys the landing template instead of portfolio."*

## Reference docs

Whether during or after the workshop, these are the references to keep on hand:

- [docs/01-terminal-basics.md](./docs/01-terminal-basics.md) — the dozen commands you actually need (`pwd`, `cd`, `mkdir`, etc.)
- [docs/02-claude-commands.md](./docs/02-claude-commands.md) — every Claude Code slash command, keyboard shortcut, and launch mode
- [docs/03-prompts.md](./docs/03-prompts.md) — a library of useful prompts, organized by what you're trying to do
- [docs/04-next-steps.md](./docs/04-next-steps.md) — going further: custom slash commands, MCP servers, skills, extending your site
