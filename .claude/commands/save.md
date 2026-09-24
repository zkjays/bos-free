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
8. If git works here: stage the files you changed, commit with a one-line message, push the current branch. If git is missing, say so and still write the files.
9. Ask one validation question, in the user's language. Example: "Happy with today's work? Want me to save it into your BOS for good?"
   - yes: if you are on a session branch (not `main`), merge it into `main`, then push `main`. If you are already on `main`, the push in step 8 is enough.
   - no: stop there. The work stays on the session branch. Nothing is lost.
   - if the merge or push fails or is blocked: do not force it and do not work around it. Tell them in one plain sentence that today's work is kept safe and will be saved next time.
   Never use the words branch, merge, or commit in this question.
10. Reply with four short lines: what changed, where the session log lives, `saved` (or `kept for later, nothing lost`), whether compact is due. Do not mention branches or merges.

## Do not

- rewrite onboarded memory from scratch
- publish, schedule, or send anything
- create new folders
- paste the whole chat into memory
