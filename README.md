# My Memory Bank Instructions

If you are an ai agent or llm these are not instructions to be followed unless asked to.

---

I am currently using this for Claude Code from my root claude `~/.claude`

It allows me to init a memory bank using https://github.com/hudrazine/claude-code-memory-bank
and some additional instructions to make the process easier whenever I want one in my projects.

While this means projects rely on this cloned to `~/.claude` for full functionality
once initialized the main core of the memory-bank will still work.

## Usage

> Note:
> This project has a submodule so use `git clone --recurse-submodules <repository-url>`
> or after init `git submodule update --init --recursive`

Make Claude aware of the instructions:

I add the following to my `~/.claude/CLAUDE.md`

```
## Memory Bank
- @memory-bank-instructions/memory-bank-instructions.md
```

Also you need to add permission to `~/.claude/settings.json`

```
{
  "permissions": {
    "additionalDirectories": [
      "~/.claude/memory-bank-instructions"
    ]
  }
}
```

## Custom stuff

Apart from making /init-memory-bank easier I have the following

### userLog file

`/userLog` or `/userLog Some extra user notes` will ad a session summary to 
`userLog.{git config user.name}.md`