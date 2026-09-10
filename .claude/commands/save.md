# /save

Close this session. Persist. Push if git is available.

## Do, in order

1. Read `memory.md`, `system/current-state.md`, `decisions/log.md`.
2. Update `memory.md` only if a new stable fact appeared (identity, a named project, a named person). Pointers, not a recap of the chat.
3. Overwrite `system/current-state.md`. Never append. Keep: in progress, blocked, next. Drop anything done.
4. Write `system/sessions/session-YYYY-MM-DD.md` (add `-2` if one already exists today). Short: what we did, what we decided, what is next.
5. Decisions:
   - if a new decision was taken, append it to `decisions/log.md` as `active`
   - if an `active` decision was explicitly killed, move it to `decisions/archive/` and remove it from the log
   - if an `active` decision has not moved and the user agrees it is stale, set `parked` or ask: park or archive?
   Do not invent staleness dates. Ask when unsure.
6. Inbox: if they dropped notes in `inbox/` that now belong in memory, decisions, or network, file them and delete or empty the inbox file.
7. Count files in `system/sessions/` that are not under `archives/`. If the count is 5 or more, tell them it is time to compact, and wait. Do not compact unless they say yes.
8. If git works here: stage the files you changed, commit with a one-line message, push to the connected remote. If git is missing, say so and still write the files.
9. Reply with four lines: what changed, where the session log lives, whether you pushed, whether compact is due.

## Do not

- rewrite onboarded memory from scratch
- publish, schedule, or send anything
- create new folders
- paste the whole chat into memory
