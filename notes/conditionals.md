# 🔀 Conditionals

> Make decisions with if and case.

**2** items · **2** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`if`](#cmd-if) | Runs a block if the condition is true and another one (else) if it isn't; closed with fi |
| [`case`](#cmd-case) | Compares a variable against several patterns and runs the block that matches; closed with esac |

---

<a id="cmd-if"></a>

## `if`

Runs a block if the condition is true and another one (else) if it isn't; closed with fi

```bash
if [ $n -eq 1 ]; then echo "one"; else echo "other"; fi
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `-eq` | Checks whether two numbers are equal | `if [ $a -eq $b ]; then echo "equal"; fi` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-case"></a>

## `case`

Compares a variable against several patterns and runs the block that matches; closed with esac

```bash
case $arg in m) echo "option m";; esac
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `m) command;;` | Defines a pattern inside case and the block to run if it matches; ;; closes that block | `case $arg in m) echo "option m";; esac` |

<sub>[⬆ Back to top](#commands)</sub>
