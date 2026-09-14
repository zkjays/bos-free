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

1. Ask: name or handle, what they do in one line, which language to use from now on.
   Write those three into `CLAUDE.md` and `memory.md`. Switch to that language now.

2. In their language, explain in a few plain lines:
   - this remembers you across chats, so you don't re-explain yourself
   - it never publishes or sends anything without you
   - tonight: a quick walkthrough, then closing the session, then opening a new one to prove it remembers

3. Walk through the pieces one at a time, plain language, no jargon, no command names in the explanation itself.

   - Memory: "I keep track of what you're working on, automatically, every time we close a session."
     No question needed here — nothing to fill in now.

   - People: "Want to keep track of anyone you deal with regularly, like clients or collaborators?
     I'll keep a note per person so you never have to re-explain who they are."
     If yes, take down a note for each name they give.

   - Decisions: "When you make a real decision on something, I'll log it so you never
     have to re-argue it with yourself later." No question needed — nothing to do now.

   - Inbox: "Any notes you want to remember and use later, want to add one now?"
     If yes, take it down. If no, move on.

4. Explain closing a session (`/save`): it writes down what happened and remembers it for next time.
   Explain the test: close this tab, open a new one, ask "where were we?".

5. Set `onboarded: true` in `CLAUDE.md`.
   Write `system/current-state.md` as: onboard just finished, next action is `/save` then a new chat.

6. Stop. Do not add skills, departments, or extra folders.
