# 🧩 Functions & Signals

> Group commands into functions and react to signals like Ctrl+C.

**2** items · **2** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`function name(){ commands }`](#cmd-function-name-commands) | Defines a custom function that groups several commands under one name |
| [`trap`](#cmd-trap) | Catches a signal (like Ctrl+C) and runs a function instead of stopping the script right away |

---

<a id="cmd-function-name-commands"></a>

## `function name(){ commands }`

Defines a custom function that groups several commands under one name

```bash
function greet(){ echo "Hello $1"; }
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `ctrl_c(){}` | Defines the ctrl_c function that runs when trap catches Ctrl+C | `function ctrl_c(){ echo "Exiting..."; exit 1; }` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-trap"></a>

## `trap`

Catches a signal (like Ctrl+C) and runs a function instead of stopping the script right away

```bash
trap ctrl_c INT
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `ctrl_c INT` | Catches the Ctrl+C signal and runs the ctrl_c function instead of stopping the script | `trap ctrl_c INT` |

<sub>[⬆ Back to top](#commands)</sub>
