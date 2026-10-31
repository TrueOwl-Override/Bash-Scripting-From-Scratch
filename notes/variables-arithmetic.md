# 📦 Variables & Arithmetic

> Store values in variables, read them back and do math with them.

**5** items · **2** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`variable="Hello"`](#cmd-variable-hello) | Declares a variable and assigns it some text (no spaces around the =) |
| [`$variable or ${variable}`](#cmd-variable-or-variable) | Reads a variable's value; the braces mark where the name ends when it's stuck to other text |
| [`${color_variable}`](#cmd-color-variable) | Variables that hold ANSI color codes; put one before the text to color it and close with the end-color variable |
| [`declare`](#cmd-declare) | Declares variables with attributes, for example making them integers |
| [`let`](#cmd-let) | Does arithmetic on variables |

---

<a id="cmd-variable-hello"></a>

## `variable="Hello"`

Declares a variable and assigns it some text (no spaces around the =)

```bash
greeting="Hello"; echo $greeting
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-variable-or-variable"></a>

## `$variable or ${variable}`

Reads a variable's value; the braces mark where the name ends when it's stuck to other text

```bash
file="data"; echo "${file}_backup.txt"
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-color-variable"></a>

## `${color_variable}`

Variables that hold ANSI color codes; put one before the text to color it and close with the end-color variable

```bash
greenColour="\e[0;32m\033[1m"; endColour="\033[0m\e[0m"; echo -e "${greenColour}[+] Hello${endColour}"
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-declare"></a>

## `declare`

Declares variables with attributes, for example making them integers

```bash
declare -i counter=0
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `-i` | Makes the variable an integer, so its value is treated as a number | `declare -i counter=0` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-let"></a>

## `let`

Does arithmetic on variables

```bash
let counter+=1
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `+=` | Adds a value to what the variable already holds | `let counter+=1` |

<sub>[⬆ Back to top](#commands)</sub>
