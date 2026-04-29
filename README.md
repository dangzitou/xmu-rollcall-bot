# XMU Rollcall Bot

> 厦门大学数字化教学平台 / Tronclass 签到监控命令行工具。
>
> A command-line tool for monitoring and handling XMU Tronclass rollcalls.

## 简介

XMU Rollcall Bot 是一个 Python CLI 工具，用于登录厦门大学数字化教学平台并持续监控课堂签到。

支持的能力：

- 多账号本地配置与切换
- 登录状态缓存与刷新
- 持续轮询签到状态
- 自动处理数字签到
- 尝试处理雷达签到
- 默认绕过系统代理，避免校园平台登录被本机代理配置影响

> 本项目仅用于个人学习和自动化便利。使用前请确认符合学校、课程与平台规则，风险自负。

## 环境要求

- Python 3.7+
- pip
- 可访问厦门大学相关平台的网络环境

## 安装

推荐从源码安装当前维护版本：

```bash
git clone https://github.com/dangzitou/xmu-rollcall-bot.git
cd xmu-rollcall-bot
python -m pip install -e ./xmu-rollcall-cli
```

安装完成后可用命令：

```bash
xmu --help
```

如果 `xmu` 没有进入 PATH，也可以使用：

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

自定义配置目录示例：

```bash
export XMU_ROLLCALL_CONFIG_DIR="$HOME/.xmu_rollcall"
```

Windows PowerShell：

```powershell
$env:XMU_ROLLCALL_CONFIG_DIR="$HOME\.xmu_rollcall"
```

## 限制

- 暂不支持二维码签到
- 平台接口变化可能导致功能失效
- 雷达签到依赖平台返回数据，不能保证所有场景可用

## English

XMU Rollcall Bot is a Python command-line tool for logging into Xiamen University's Tronclass platform and monitoring rollcalls.

### Requirements

- Python 3.7+
- pip
- Network access to XMU campus services

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
