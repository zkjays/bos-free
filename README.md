# BOS free

A personal assistant that remembers everything.
It does not run your life. It remembers it, so you can decide.

Not a skills pack. Not a second-brain template with empty numbered folders.
A small operating system: memory, decisions, one save command.

You still need an AI subscription (Claude in the browser, or Codex). That is the only cost.

## Before tonight

You need two things:

- A GitHub account. Free. Sign up at [github.com/signup](https://github.com/signup) and confirm your email. GitHub is just where your assistant's memory is stored, as plain files you own.
- A Claude subscription that includes [claude.ai/code](https://claude.ai/code).

## Tonight

1. On this page, click **Use this template** → **Create a new repository**. This public repo is only the template.
2. Name it, set it to **Private**, then click **Create repository**. Your vault must be private.
3. Open [claude.ai/code](https://claude.ai/code). The first time, it asks to connect GitHub: accept, and when GitHub asks which repositories Claude can access, choose **Only select repositories** and pick the private repo you just created. Claude only sees that one. Already connected before? Add the new repo in GitHub → **Settings** → **Applications** → **Claude** → **Configure**.
4. Type `/onboard`. Answer the questions. Do not design folders.
5. Type `/save`. When it asks if you want to save for good, say yes.
6. Open a **new** chat on the same repo and ask: `where were we?`

If it answers without a brief, it works. If it asks who you are, run `/save` again.

Obsidian is optional, later, as a reader. Not on the path tonight.

## What you get

```
CLAUDE.md                 operator rules, filled by /onboard
memory.md                 who you are, what you run, pointers only
ONBOARD.md                script /onboard follows
inbox/                    quick notes, filed on /save
decisions/log.md          active and parked decisions
decisions/archive/        obsolete decisions
network/                  one file per person, only if you named someone
system/current-state.md   in progress — overwritten, never appended
system/sessions/          one log per session
.claude/commands/
  onboard.md
  save.md
```

No departments. No CEO dispatcher. No `00-` prefixes.
Projects you name during onboard become short lines in `memory.md`, not a projects folder.

## Commands

- `/onboard` — first run writes memory. Later runs are read-only unless you say `reset onboard`.
- `/save` — update memory if something new is true, overwrite state, log the session, route stale decisions, then ask before saving to GitHub for good. After 5 session logs, it *asks* to compact. It does not compact alone the first week.

## What this is not

You can install a hundred skills tonight and still re-explain your business in the morning. That is the part BOS is for.

Playbooks come later, one at a time, in [Self System](https://zkjays.beehiiv.com). Each one runs without BOS, and runs better on it.

## License

MIT. Built by [@zkjays](https://x.com/zkjays).
