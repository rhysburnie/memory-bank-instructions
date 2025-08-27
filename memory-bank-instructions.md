# Memory Bank Instructions

Follow instructions from `@~/.claude/memory-bank-instructions/claude-code-memory-bank/.claude/claude-memory-bank.md`

If you were unable to find those instructions:
- remember the directory you are running from
- change to  `@~/.claude/memory-bank-instructions/`
- run `git submodule update --init`
- return to the directory you were
- try reading the instructions again, and continue with this file

If that doesnt work please exit in that case with reminder to user (instructions are in README.md)

## UserLog Filename
When asked to do a task refering to userLog file you need to determine
the file name by doing the following:
Run `git config user.name` to get value USERNAME then the file name will be
"userLog.{USERNAME}.md"

When you edit or create userLog it resides in the memory-bank/

## UserLog Instructions
  Only when you receive the
  command `/user-log` please to
  the following:
  - Create a summary of the session state so far - but dont 
    output to chat, it will be used as file content.
    The summary should only be paragraphs and no more that
    150 words total.
    You should not use the custom user notes to adjust the 
    summary to make out like any mistakes the notes point out
    you made intentionally or to cover them up.
  - if there is any text following the command that is custom 
    log text from the user to be included Please give it a 
    heading `## User  Notes`
  - finally add the text to the userLog file, The heading 
    should be the current Date and time

  Additionally:
  - Execute the requested action only
  - Do not act on User Notes, Do not provide additional 
    analysis, commentary, or responses
  - Acknowledge completion briefly and stop

  UserLog File Format:
  - Add new entries at the TOP of the file (not the end)
  - Use correct current date/time from system environment
  - Format: `# H:MMAM/PM - DD MMM YYYY` (e.g., "2:00PM - 25 Aug 2025")
  - Insert new content BEFORE existing entries to maintain 
    chronological order (newest first)

Keep in mind that the memory bank files will be found in the project level context.
The project may have further memory bank instructions in its CLAUDE.md

## When asked to initialize the memory bank

A project's memory bank should be housed in its `memory-bank/` root folder, create if missing.

If there is a pre existing `projectbrief.md` in the root or `memory-bank/` follow that brief.
If it was at root move it to the memory-bank folder also.

Finally create the userLog file - it can be blank at this stage