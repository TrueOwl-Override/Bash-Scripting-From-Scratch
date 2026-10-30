<div align="center">

# 🐚 Bash Scripting From Scratch

**A personal reference for writing Bash scripts: variables, arguments, conditionals, loops, functions and more, with copy-ready examples.**

![Concepts](https://img.shields.io/badge/concepts-30-2ea44f?style=for-the-badge) ![Parameters](https://img.shields.io/badge/parameters-17-0969da?style=for-the-badge) ![Categories](https://img.shields.io/badge/categories-9-8250df?style=for-the-badge)

🌐 **Searchable web version:** [`docs/index.html`](docs/index.html)  ·  🐧 **Companion repo:** [Linux-Commands](https://github.com/TrueOwl-Override/Linux-Commands)

</div>

---

## 📚 Categories

| | Category | What's inside | Items |
|:-:|:--|:--|:--|
| 📜 | **[Script Basics](notes/script-basics.md)** | The building blocks of every script: the shebang, exit codes, command substitution and subshells. | `#!/bin/bash` `exit` `$()` `(command)` |
| 📦 | **[Variables & Arithmetic](notes/variables-arithmetic.md)** | Store values in variables, read them back and do math with them. | `variable="Hello"` `$variable or ${variable}` `declare` `let` |
| 🎯 | **[Arguments & Options](notes/arguments-options.md)** | Read what's passed to your script: positional arguments and flags parsed with getopts. | `$0` `$1, $2...` `$#` `$*` `getopts` `$OPTARG` |
| 🔀 | **[Conditionals](notes/conditionals.md)** | Make decisions with if and case. | `if` `case` |
| 🔁 | **[Loops & Sequences](notes/loops-sequences.md)** | Repeat work with for and while, and generate sequences to loop over. | `for` `while` `seq` `{0000..9999}` |
| 🧩 | **[Functions & Signals](notes/functions-signals.md)** | Group commands into functions and react to signals like Ctrl+C. | `function name(){ commands }` `trap` |
| ⚙️ | **[Jobs, Temp Files & Terminal](notes/jobs-temp-files-terminal.md)** | Wait for background jobs, set time limits, create temp files and control the cursor. | `wait` `timeout` `mktemp` `tput` |
| 🌐 | **[Networking in Bash](notes/networking-in-bash.md)** | Open TCP connections from pure Bash and make HTTP requests. | `/dev/tcp/$ip/$port` `curl` |
| 🛠️ | **[Helper Tools](notes/helper-tools.md)** | Handy tools for reading and prettifying code while you script. | `batcat` `js-beautify` |

## 🔤 A–Z index

| Item | What it does | Category |
|:--|:--|:--|
| [`batcat`](notes/helper-tools.md#cmd-batcat) | Shows a file like cat, but with syntax highlighting and line numbers | 🛠️ Helper Tools |
| [`case`](notes/conditionals.md#cmd-case) | Compares a variable against several patterns and runs the block that matches; closed with esac | 🔀 Conditionals |
| [`curl`](notes/networking-in-bash.md#cmd-curl) | Sends requests to a URL from the terminal (HTTP, HTTPS, etc.) and shows the response | 🌐 Networking in Bash |
| [`declare`](notes/variables-arithmetic.md#cmd-declare) | Declares variables with attributes, for example making them integers | 📦 Variables & Arithmetic |
| [`exit`](notes/script-basics.md#cmd-exit) | Ends the script; its exit code tells whether it worked (0) or failed (anything else) | 📜 Script Basics |
| [`for`](notes/loops-sequences.md#cmd-for) | Loops over a list of items one by one, running a block of code for each | 🔁 Loops & Sequences |
| [`function name(){ commands }`](notes/functions-signals.md#cmd-function-name-commands) | Defines a custom function that groups several commands under one name | 🧩 Functions & Signals |
| [`getopts`](notes/arguments-options.md#cmd-getopts) | Processes the options a script receives (-m, -h...) one at a time; usually used inside a while loop | 🎯 Arguments & Options |
| [`if`](notes/conditionals.md#cmd-if) | Runs a block if the condition is true and another one (else) if it isn't; closed with fi | 🔀 Conditionals |
| [`js-beautify`](notes/helper-tools.md#cmd-js-beautify) | Formats minified JavaScript or JSON so it's readable (line breaks and indentation) | 🛠️ Helper Tools |
| [`let`](notes/variables-arithmetic.md#cmd-let) | Does arithmetic on variables | 📦 Variables & Arithmetic |
| [`mktemp`](notes/jobs-temp-files-terminal.md#cmd-mktemp) | Creates a temporary file with a unique name, avoiding clashes with other files | ⚙️ Jobs, Temp Files & Terminal |
| [`seq`](notes/loops-sequences.md#cmd-seq) | Generates a sequence of numbers within a range, handy for loops | 🔁 Loops & Sequences |
| [`timeout`](notes/jobs-temp-files-terminal.md#cmd-timeout) | Runs a command and kills it if it takes longer than the given time | ⚙️ Jobs, Temp Files & Terminal |
| [`tput`](notes/jobs-temp-files-terminal.md#cmd-tput) | Controls the terminal, for example hiding or showing the cursor | ⚙️ Jobs, Temp Files & Terminal |
| [`trap`](notes/functions-signals.md#cmd-trap) | Catches a signal (like Ctrl+C) and runs a function instead of stopping the script right away | 🧩 Functions & Signals |
| [`variable="Hello"`](notes/variables-arithmetic.md#cmd-variable-hello) | Declares a variable and assigns it some text (no spaces around the =) | 📦 Variables & Arithmetic |
| [`wait`](notes/jobs-temp-files-terminal.md#cmd-wait) | Waits for one or more background processes to finish before continuing | ⚙️ Jobs, Temp Files & Terminal |
| [`while`](notes/loops-sequences.md#cmd-while) | Repeats a block of code while a condition is true | 🔁 Loops & Sequences |
| [`#!/bin/bash`](notes/script-basics.md#cmd-bin-bash) | Shebang: the first line of a script, telling the system to run it with Bash | 📜 Script Basics |
| [`$#`](notes/arguments-options.md#cmd-sym-36-35) | Holds the number of arguments passed on the command line | 🎯 Arguments & Options |
| [`$()`](notes/script-basics.md#cmd-sym-36-40-41) | Runs the command inside the parentheses and uses its output (command substitution) | 📜 Script Basics |
| [`$*`](notes/arguments-options.md#cmd-sym-36-42) | Holds all the arguments passed on the command line in a single variable | 🎯 Arguments & Options |
| [`$0`](notes/arguments-options.md#cmd-0) | Holds the name of the script as it was called from the terminal | 🎯 Arguments & Options |
| [`$1, $2...`](notes/arguments-options.md#cmd-1-2) | The first, second (and so on) argument passed on the command line | 🎯 Arguments & Options |
| [`$OPTARG`](notes/arguments-options.md#cmd-optarg) | Holds the value that comes with the option getopts is currently processing | 🎯 Arguments & Options |
| [`$variable or ${variable}`](notes/variables-arithmetic.md#cmd-variable-or-variable) | Reads a variable's value; the braces mark where the name ends when it's stuck to other text | 📦 Variables & Arithmetic |
| [`(command)`](notes/script-basics.md#cmd-command) | Runs the command in a subshell, a child process separate from the main script | 📜 Script Basics |
| [`/dev/tcp/$ip/$port`](notes/networking-in-bash.md#cmd-dev-tcp-ip-port) | Special Bash path that opens a TCP connection to an IP and port as if it were a file, no netcat needed | 🌐 Networking in Bash |
| [`{0000..9999}`](notes/loops-sequences.md#cmd-0000-9999) | Brace expansion: generates a sequence of values (here 0000 to 9999), useful as a counter in loops | 🔁 Loops & Sequences |

## 🛠️ How to update

The data lives in [`data/`](data): [`categories.csv`](data/categories.csv), [`commands.csv`](data/commands.csv) and [`parameters.csv`](data/parameters.csv). After editing them, run:

```bash
python3 scripts/build.py
```

This rebuilds this README, the notes in [`notes/`](notes) and the web page in [`docs/`](docs).

> 💡 To publish the web page: **Settings → Pages → Branch `main` / folder `/docs`**.
