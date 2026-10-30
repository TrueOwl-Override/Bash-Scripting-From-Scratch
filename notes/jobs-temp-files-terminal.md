# ⚙️ Jobs, Temp Files & Terminal

> Wait for background jobs, set time limits, create temp files and control the cursor.

**4** items · **4** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`wait`](#cmd-wait) | Waits for one or more background processes to finish before continuing |
| [`timeout`](#cmd-timeout) | Runs a command and kills it if it takes longer than the given time |
| [`mktemp`](#cmd-mktemp) | Creates a temporary file with a unique name, avoiding clashes with other files |
| [`tput`](#cmd-tput) | Controls the terminal, for example hiding or showing the cursor |

---

<a id="cmd-wait"></a>

## `wait`

Waits for one or more background processes to finish before continuing

```bash
sleep 5 & wait
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-timeout"></a>

## `timeout`

Runs a command and kills it if it takes longer than the given time

```bash
timeout 5 ping 8.8.8.8
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `1 bash -c ""` | Runs a command with a 1-second limit; if it doesn't finish, it's cancelled | `timeout 1 bash -c "echo > /dev/tcp/127.0.0.1/22" && echo "open"` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-mktemp"></a>

## `mktemp`

Creates a temporary file with a unique name, avoiding clashes with other files

```bash
mktemp
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `-d` | Creates a temporary folder instead of a file, with a unique name | `mktemp -d` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-tput"></a>

## `tput`

Controls the terminal, for example hiding or showing the cursor

```bash
tput civis
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `civis` | Hides the terminal cursor | `tput civis` |
| `cnorm` | Shows the terminal cursor again | `tput cnorm` |

<sub>[⬆ Back to top](#commands)</sub>
