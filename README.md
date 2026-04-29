<div align="center">

# XMU Rollcall Bot

<p>
  <img src="https://img.shields.io/badge/Python-3.7%2B-blue" />
  <img src="https://img.shields.io/badge/Platform-macOS%20%7C%20Linux%20%7C%20Windows-0f766e" />
  <img src="https://img.shields.io/badge/CLI-Tool-7c3aed" />
  <img src="https://img.shields.io/badge/XMU-TronClass-ef4444" />
  <img src="https://img.shields.io/badge/Direct%20connection-On-111827" />
  <img src="https://img.shields.io/badge/License-MIT-6b7280" />
</p>

<p><strong>A command-line tool for monitoring and handling XMU Tronclass rollcalls</strong></p>

</div>

---

## Disclaimer

This project is provided for learning, research, and personal automation convenience only. Users are responsible for complying with their school's rules, course policies, platform terms, and applicable laws.

The author and maintainers assume no liability for account risks, data issues, platform restrictions, or any other consequences arising from use of this project.

## Overview

XMU Rollcall Bot is a Python CLI tool for logging into Xiamen University's Tronclass platform and monitoring rollcalls.

## Installation

```bash
git clone https://github.com/dangzitou/xmu-rollcall-bot.git
cd xmu-rollcall-bot
python -m pip install -e ./xmu-rollcall-cli
```

Verify the CLI:

```bash
xmu --help
```

If `xmu` is not on your PATH:

```bash
python -m xmu_rollcall.cli --help
```

## Run

### macOS / Linux

```bash
cd xmu-rollcall-bot
python3 -m pip install -e ./xmu-rollcall-cli

xmu config
xmu start
```

Fallback:

```bash
python3 -m xmu_rollcall.cli config
python3 -m xmu_rollcall.cli start
```

### Windows PowerShell

```powershell
cd C:\path\to\xmu-rollcall-bot
python -m pip install -e .\xmu-rollcall-cli

xmu config
xmu start
```

Fallback:

```powershell
python -m xmu_rollcall.cli config
python -m xmu_rollcall.cli start
```

## Commands

```bash
xmu config   # Add/delete accounts and configure rollcall safety settings
xmu switch   # Switch account
xmu start    # Start rollcall monitoring
xmu refresh  # Remove cached login cookies
xmu --help   # Show help
```

## Notes

- QR code rollcalls are not supported.
- Number and radar rollcall answers can be delayed, and manual confirmation can be enabled from `xmu config`.
- The tool depends on XMU/Tronclass API behavior and may break if upstream services change.
- Use it responsibly and follow your school's rules.

## License

MIT
