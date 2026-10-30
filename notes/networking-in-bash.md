# 🌐 Networking in Bash

> Open TCP connections from pure Bash and make HTTP requests.

**2** items · **2** parameters  ·  [⬅ Back to index](../README.md)

<a id="commands"></a>

| Item | What it does |
|:--|:--|
| [`/dev/tcp/$ip/$port`](#cmd-dev-tcp-ip-port) | Special Bash path that opens a TCP connection to an IP and port as if it were a file, no netcat needed |
| [`curl`](#cmd-curl) | Sends requests to a URL from the terminal (HTTP, HTTPS, etc.) and shows the response |

---

<a id="cmd-dev-tcp-ip-port"></a>

## `/dev/tcp/$ip/$port`

Special Bash path that opens a TCP connection to an IP and port as if it were a file, no netcat needed

```bash
echo '' > /dev/tcp/127.0.0.1/22 && echo "open"
```

<sub>[⬆ Back to top](#commands)</sub>

---

<a id="cmd-curl"></a>

## `curl`

Sends requests to a URL from the terminal (HTTP, HTTPS, etc.) and shows the response

```bash
curl -s -X GET https://example.com
```

| Parameter | What it does | Example |
|:--|:--|:--|
| `-s` | Silent mode: hides the progress bar and error messages | `curl -s https://example.com` |
| `-X GET` | Sets the request's HTTP method (GET, POST, PUT...) | `curl -s -X GET https://example.com` |

<sub>[⬆ Back to top](#commands)</sub>
