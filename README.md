<div align="center">

# XMU Rollcall Bot

<p>
  <img src="https://socialify.git.ci/dangzitou/xmu-rollcall-bot/image?font=JetBrains+Mono&forks=1&language=1&name=1&owner=1&pattern=Plus&stargazers=1&theme=Light" alt="XMU Rollcall Bot" />
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.7%2B-blue" />
  <img src="https://img.shields.io/badge/Platform-macOS%20%7C%20Linux%20%7C%20Windows-0f766e" />
  <img src="https://img.shields.io/badge/CLI-Tool-7c3aed" />
</p>

<p>
  <img src="https://img.shields.io/badge/XMU-TronClass-ef4444" />
  <img src="https://img.shields.io/badge/Proxy-Bypass-111827" />
  <img src="https://img.shields.io/badge/License-MIT-6b7280" />
</p>

<p><strong>厦门大学数字化教学平台 / Tronclass 签到监控命令行工具</strong></p>
<p><strong>A command-line tool for monitoring and handling XMU Tronclass rollcalls</strong></p>

</div>

---

## 免责声明 / Disclaimer

本项目仅供学习、研究和个人自动化便利使用。使用者应自行确认并遵守所在学校、课程、平台与相关法律法规的要求。

作者及维护者不对因使用本项目导致的任何账号风险、数据异常、平台限制或其他后果承担责任。

This project is provided for learning, research, and personal automation convenience only. Users are responsible for complying with their school's rules, course policies, platform terms, and applicable laws.

The author and maintainers assume no liability for account risks, data issues, platform restrictions, or any other consequences arising from use of this project.

## 简介

XMU Rollcall Bot 是一个 Python CLI 工具，用于登录厦门大学数字化教学平台并持续监控课堂签到。

> 本项目仅用于个人学习和自动化便利。使用前请确认符合学校、课程与平台规则，风险自负。

## 安装

```bash
git clone https://github.com/dangzitou/xmu-rollcall-bot.git
cd xmu-rollcall-bot
python -m pip install -e ./xmu-rollcall-cli
```

安装完成后：

```bash
xmu --help
```

如果 `xmu` 没有进入 PATH：

```bash
python -m xmu_rollcall.cli --help
```

## 启动方式

### macOS / Linux

```bash
cd xmu-rollcall-bot
python3 -m pip install -e ./xmu-rollcall-cli

xmu config
xmu start
```

如果系统找不到 `xmu`：

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

如果系统找不到 `xmu`：

```powershell
python -m xmu_rollcall.cli config
python -m xmu_rollcall.cli start
```

## 常用命令

```bash
xmu config   # 添加、删除账号，并设置当前账号
xmu switch   # 切换当前账号
xmu start    # 启动签到监控
xmu refresh  # 清除当前账号登录缓存
xmu --help   # 查看帮助
```

## 配置文件

本地配置默认保存在 `.xmu_rollcall` 目录中，优先级如下：

1. `XMU_ROLLCALL_CONFIG_DIR` 指定的目录
2. 用户主目录下的 `~/.xmu_rollcall`
3. 当前工作目录下的 `./.xmu_rollcall`

主要文件：

- `config.json`：账号列表与当前账号
- `<account_id>.json`：对应账号的登录 cookie 缓存

## 限制

- 暂不支持二维码签到
- 平台接口变化可能导致功能失效
- 雷达签到依赖平台返回数据，不能保证所有场景可用

## English

XMU Rollcall Bot is a Python command-line tool for logging into Xiamen University's Tronclass platform and monitoring rollcalls.

### Tags

<p align="center">
  <img src="https://img.shields.io/badge/Multi--account-Supported-2563eb" />
  <img src="https://img.shields.io/badge/Cookie%20cache-Supported-0f766e" />
  <img src="https://img.shields.io/badge/Polling-1s-7c3aed" />
  <img src="https://img.shields.io/badge/Number%20rollcall-Auto-ef4444" />
  <img src="https://img.shields.io/badge/Radar%20rollcall-Supported-f59e0b" />
  <img src="https://img.shields.io/badge/Direct%20connection-On-111827" />
</p>

### Installation

```bash
git clone https://github.com/dangzitou/xmu-rollcall-bot.git
cd xmu-rollcall-bot
python -m pip install -e ./xmu-rollcall-cli
```

Verify the CLI:

```bash
xmu --help
```

### Run on macOS / Linux

```bash
cd xmu-rollcall-bot
python3 -m pip install -e ./xmu-rollcall-cli

xmu config
xmu start
```

Fallback command:

```bash
python3 -m xmu_rollcall.cli config
python3 -m xmu_rollcall.cli start
```

### Run on Windows PowerShell

```powershell
cd C:\path\to\xmu-rollcall-bot
python -m pip install -e .\xmu-rollcall-cli

xmu config
xmu start
```

Fallback command:

```powershell
python -m xmu_rollcall.cli config
python -m xmu_rollcall.cli start
```

### Commands

```bash
xmu config   # Add/delete accounts and set the current account
xmu switch   # Switch account
xmu start    # Start rollcall monitoring
xmu refresh  # Remove cached login cookies
xmu --help   # Show help
```

### Notes

- QR code rollcalls are not supported.
- This tool depends on XMU/Tronclass API behavior and may break if upstream services change.
- Use it responsibly and follow your school's rules.

## License

MIT
