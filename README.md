# pingping TUI

A simple and fast real-time multi-host ping monitor with a clean terminal user interface (TUI).

Built with [Textual](https://github.com/Textualize/textual).

## Features

- Live ping monitoring (updates every second)
- Hierarchical host groups using a config file
- Color-coded latency (green = fast, red = slow)
- Visual heat bars for quick status overview
- Details panel for selected hosts
- Lightweight and cross-platform

## Quick Start

### 1. Installation

```bash
git clone https://github.com/betz-anthony/pingping.git
cd multi-ping-tui

pip install textual
```
### 2. Run the app
```bash
python3 multi-ping.py
```
or
```bash
chmod +x multi-ping.py
./multi-ping.py
```
### 3. Configuration
Create a file named pingping.conf in the same folder to organize your hosts:

```ini:
[Google]
hosts = 8.8.8.8
        8.8.4.4

[Cloudflare]
hosts = 1.1.1.1
        1.0.0.1

[Home.Network]
hosts = 192.168.1.1
        192.168.1.254

[Work.Servers]
hosts = 10.0.0.10
        10.0.0.20
```
Use dotted notation for deeper nesting (e.g. Company.Site1.Servers)
If no config file exists, it defaults to pinging Google and Cloudflare DNS

Keyboard Controls

* Arrow keys — Navigate tree
* Enter — Expand/collapse folders
* q — Quit

### 4. Requirements

Python 3.8 or higher
textual library
