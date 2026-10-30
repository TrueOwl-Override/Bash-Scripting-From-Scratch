# 🔁 Loops & Sequences

> Repeat work with for and while, and generate sequences to loop over.

**4** items · **3** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`for`](#cmd-for) | Loops over a list of items one by one, running a block of code for each |
| [`while`](#cmd-while) | Repeats a block of code while a condition is true |
| [`seq`](#cmd-seq) | Generates a sequence of numbers within a range, handy for loops |
| [`{0000..9999}`](#cmd-0000-9999) | Brace expansion: generates a sequence of values (here 0000 to 9999), useful as a counter in loops |

---

<a id="cmd-for"></a>

## `for`

Loops over a list of items one by one, running a block of code for each

```bash
for i in $(seq 1 5); do echo $i; done
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `line in; do; done` | Goes through the items of a list one by one and runs the block for each | `for line in $(cat list.txt); do echo $line; done` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-while"></a>

## `while`

Repeats a block of code while a condition is true

```bash
while [ $i -lt 5 ]; do echo $i; i=$((i+1)); done
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `[ ]; do; done` | Repeats the block while the condition inside the brackets is true | `while [ -f file.gz ]; do gunzip file.gz; done` |
| `read line; do; done` | Reads input line by line and runs the block for each line | `cat list.txt \| while read line; do echo $line; done` |

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-seq"></a>

## `seq`

Generates a sequence of numbers within a range, handy for loops

```bash
seq 1 10
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-0000-9999"></a>

## `{0000..9999}`

Brace expansion: generates a sequence of values (here 0000 to 9999), useful as a counter in loops

```bash
for i in {0000..9999}; do echo $i; done
```

<sub>[⬆ Back to top](#commands)</sub>
