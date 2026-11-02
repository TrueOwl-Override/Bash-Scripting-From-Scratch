# 🎯 Arguments & Options

> Read what's passed to your script: positional arguments and flags parsed with getopts.

**5** items · **2** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`$0`](#cmd-0) | Holds the name of the script as it was called from the terminal |
| [`$1, $2...`](#cmd-1-2) | The first, second (and so on) argument passed on the command line |
| [`$#`](#cmd-sym-36-35) | Holds the number of arguments passed on the command line |
| [`$*`](#cmd-sym-36-42) | Holds all the arguments passed on the command line in a single variable |
| [`getopts`](#cmd-getopts) | Processes the options a script receives (-m, -h...) one at a time; usually used inside a while loop |

---

<a id="cmd-0"></a>

## `$0`

Holds the name of the script as it was called from the terminal

```bash
echo $0
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-1-2"></a>

## `$1, $2...`

The first, second (and so on) argument passed on the command line

```bash
./script.sh hello world → echo $1
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-sym-36-35"></a>

## `$#`

Holds the number of arguments passed on the command line

```bash
echo "Got $# arguments"
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-sym-36-42"></a>

## `$*`

Holds all the arguments passed on the command line in a single variable

```bash
echo "Arguments: $*"
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-getopts"></a>

## `getopts`

Processes the options a script receives (-m, -h...) one at a time; usually used inside a while loop

```bash
while getopts "m:h" arg; do ... done
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `"m:h" arg` | List of valid options, stored in arg; a ":" after a letter means that option takes a value, which ends up in $OPTARG | `while getopts "m:h" arg; do case $arg in m) name=$OPTARG;; h) help;; esac; done` |
| `$OPTARG` | Holds the value that comes with the option getopts is currently processing | `while getopts "m:h" arg; do case $arg in m) name=$OPTARG;; esac; done` |

<sub>[⬆ Back to top](#commands)</sub>
