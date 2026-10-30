# 📜 Script Basics

> The building blocks of every script: the shebang, exit codes, command substitution and subshells.

**4** items · **1** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`#!/bin/bash`](#cmd-bin-bash) | Shebang: the first line of a script, telling the system to run it with Bash |
| [`exit`](#cmd-exit) | Ends the script; its exit code tells whether it worked (0) or failed (anything else) |
| [`$()`](#cmd-sym-36-40-41) | Runs the command inside the parentheses and uses its output (command substitution) |
| [`(command)`](#cmd-command) | Runs the command in a subshell, a child process separate from the main script |

---

<a id="cmd-bin-bash"></a>

## `#!/bin/bash`

Shebang: the first line of a script, telling the system to run it with Bash

```bash
#!/bin/bash   (first line of script.sh)
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-exit"></a>

## `exit`

Ends the script; its exit code tells whether it worked (0) or failed (anything else)

```bash
exit 0
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `1` | Ends the script with exit code 1, signalling an error | `exit 1` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-sym-36-40-41"></a>

## `$()`

Runs the command inside the parentheses and uses its output (command substitution)

```bash
echo "I'm in $(pwd)"
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-command"></a>

## `(command)`

Runs the command in a subshell, a child process separate from the main script

```bash
(ping -c 1 192.168.1.1) &
```

<sub>[⬆ Back to top](#commands)</sub>
