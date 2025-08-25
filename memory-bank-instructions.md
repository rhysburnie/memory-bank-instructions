# Memory Bank Instructions

Follow instructions from `@~/.claude/memory-bank-instructions/claude-code-memory-bank/.claude/claude-memory-bank.md`

## UserLog Filename
When asked to do a task refering to userLog file you need to determine
the file name by doing the following:
Run `git config user.name` to get value USERNAME then the file name will be
"userLog.{username}.md"

When you edit or create userLog it resides in the memory-bank/

## UserLog Instructions

When you encounter the command /user-log please to the following:
- Create a summary of the session state so far - but dont output to chat, it will be used as file content. The summary should only be paragraphs and no more that 150 words total.
- if there is any text following the command that is custom log text from the user to be included Please give it a heading `## User Notes`
- finally add the text to the userLog file, The heading should be `# Session Summary` plus the current Date and time

Keep in mind that the memory bank files will be found in the project level context.
The project may have further memory bank instructions in its CLAUDE.md

## When asked to initialize the memory bank

A project's memory bank should be housed in its `memory-bank/` root folder, create if missing.

If there is a pre existing `projectbrief.md` in the root or `memory-bank/` follow that brief.
If it was at root move it to the memory-bank folder also.

Finally create the userLog file - it can be blank at this stage