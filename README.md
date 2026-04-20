# pingforge TUI

A simple and fast real-time multi-host ping monitor with a clean terminal user interface (TUI).

<img width="1067" height="736" alt="image" src="https://github.com/user-attachments/assets/3052a8ce-deb0-4812-a97c-6a8fc7bd5add" />

Built with [Textual](https://github.com/Textualize/textual).

## Features

- Live ping monitoring (updates every second)
- Hierarchical host groups using a config file
- Color-coded latency (green = fast, red = slow)
- Visual heat bars for quick status overview
- Details panel for selected hosts
- Lightweight and cross-platform (Linux, MacOS)

## Quick Start

### 1. Installation

```bash
git clone https://github.com/betz-anthony/pingforge.git
cd pingforge

pip install textual
```
### 2. Run the app
```bash
python3 pingforge.py
```
or
```bash
chmod +x pingforge.py
./pingforge.py
```
### 3. Configuration
Create a file named pingforge.conf in the same folder to organize your hosts:

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
If no config file exists, it defaults to pinging Google and Cloudflare DNS.  Alternate config files can be used. 
```bash
./pingforge.py -c alt_config.conf
```
OR
```bash
./pingforge.py --config alt_config.conf
```

Keyboard Controls

* Arrow keys — Navigate tree
* Enter — Expand/collapse folders
* q — Quit
* r — force refresh
* ctrl + p — palette

### 4. Requirements

Python 3.8 or higher
textual library

## License
GPLv3 license
