# /onboard script

Follow this file when the user types `/onboard`. Ask one question at a time. Wait for the answer. Do not skip ahead.

## If CLAUDE.md says `onboarded: true`

Do not rewrite memory.

Say, in their language:

- onboard already ran
- memory is in `memory.md`
- close a session with `/save`
- to start over they must type exactly: `reset onboard`

Then stop.

## If they typed `reset onboard`

Confirm once. If they confirm, set `onboarded: false` and run the first-time flow below. Keep old files in place until new answers replace them.

## First-time flow

1. Explain in 6 lines, their language if already known, otherwise English then switch:
   - this is a BOS, not a skills pack
   - it will remember them across chats
   - it will not publish without them
   - tonight: answers, then `/save`, then a new chat that still knows them

2. Ask: name or handle, what they do in one line, which language to use from now on.
   Write those three into `CLAUDE.md` and `memory.md`.

3. Ask: every project or business they are actually running, including the one they keep postponing.
   Write short lines under Active work in `memory.md`. No project files.

4. Ask: every relationship they need to track (clients, leads, collaborators).
   If they name people, create `network/<slug>.md` from `network/_template.md` for each, and list the names in memory.
   If they name no one, leave `network/` empty.

5. Ask: every decision they keep re-explaining or re-arguing with themselves.
   For each one they consider already decided, append to `decisions/log.md` as `active`.
   For each one still open, leave it under Decisions I keep re-explaining in memory.

6. Explain the four folders in four lines. Explain `/save`. Explain the second-chat test: close this tab, open a new one, ask "where were we?".

7. Set `onboarded: true` in `CLAUDE.md`.
   Write `system/current-state.md` as: onboard just finished, next action is `/save` then a new chat.

8. Stop. Do not add skills, departments, or extra folders.
