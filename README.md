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

<p><strong>鍘﹂棬澶у鏁板瓧鍖栨暀瀛﹀钩鍙?/ Tronclass 绛惧埌鐩戞帶鍛戒护琛屽伐鍏?/strong></p>
<p><strong>A command-line tool for monitoring and handling XMU Tronclass rollcalls</strong></p>

</div>

---

<p align="center">
  <a href="#chinese">中文</a> | <a href="#english">English</a>
</p>

---

## 鍏嶈矗澹版槑 / Disclaimer

鏈」鐩粎渚涘涔犮€佺爺绌跺拰涓汉鑷姩鍖栦究鍒╀娇鐢ㄣ€備娇鐢ㄨ€呭簲鑷纭骞堕伒瀹堟墍鍦ㄥ鏍°€佽绋嬨€佸钩鍙颁笌鐩稿叧娉曞緥娉曡鐨勮姹傘€?
浣滆€呭強缁存姢鑰呬笉瀵瑰洜浣跨敤鏈」鐩鑷寸殑浠讳綍璐﹀彿椋庨櫓銆佹暟鎹紓甯搞€佸钩鍙伴檺鍒舵垨鍏朵粬鍚庢灉鎵挎媴璐ｄ换銆?
This project is provided for learning, research, and personal automation convenience only. Users are responsible for complying with their school's rules, course policies, platform terms, and applicable laws.

The author and maintainers assume no liability for account risks, data issues, platform restrictions, or any other consequences arising from use of this project.

<a id="chinese"></a>
## 绠€浠?
XMU Rollcall Bot 鏄竴涓?Python CLI 宸ュ叿锛岀敤浜庣櫥褰曞帵闂ㄥぇ瀛︽暟瀛楀寲鏁欏骞冲彴骞舵寔缁洃鎺ц鍫傜鍒般€?
> 鏈」鐩粎鐢ㄤ簬涓汉瀛︿範鍜岃嚜鍔ㄥ寲渚垮埄銆備娇鐢ㄥ墠璇风‘璁ょ鍚堝鏍°€佽绋嬩笌骞冲彴瑙勫垯锛岄闄╄嚜璐熴€?
## 瀹夎

```bash
git clone https://github.com/dangzitou/xmu-rollcall-bot.git
cd xmu-rollcall-bot
python -m pip install -e ./xmu-rollcall-cli
```

瀹夎瀹屾垚鍚庯細

```bash
xmu --help
```

濡傛灉 `xmu` 娌℃湁杩涘叆 PATH锛?
```bash
python -m xmu_rollcall.cli --help
```

## 鍚姩鏂瑰紡

### macOS / Linux

```bash
cd xmu-rollcall-bot
python3 -m pip install -e ./xmu-rollcall-cli

xmu config
xmu start
```

濡傛灉绯荤粺鎵句笉鍒?`xmu`锛?
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

濡傛灉绯荤粺鎵句笉鍒?`xmu`锛?
```powershell
python -m xmu_rollcall.cli config
python -m xmu_rollcall.cli start
```

## 甯哥敤鍛戒护

```bash
xmu config   # 娣诲姞銆佸垹闄よ处鍙凤紝骞惰缃綋鍓嶈处鍙?xmu switch   # 鍒囨崲褰撳墠璐﹀彿
xmu start    # 鍚姩绛惧埌鐩戞帶
xmu refresh  # 娓呴櫎褰撳墠璐﹀彿鐧诲綍缂撳瓨
xmu --help   # 鏌ョ湅甯姪
```

## 閰嶇疆鏂囦欢

鏈湴閰嶇疆榛樿淇濆瓨鍦?`.xmu_rollcall` 鐩綍涓紝浼樺厛绾у涓嬶細

1. `XMU_ROLLCALL_CONFIG_DIR` 鎸囧畾鐨勭洰褰?2. 鐢ㄦ埛涓荤洰褰曚笅鐨?`~/.xmu_rollcall`
3. 褰撳墠宸ヤ綔鐩綍涓嬬殑 `./.xmu_rollcall`

涓昏鏂囦欢锛?
- `config.json`锛氳处鍙峰垪琛ㄤ笌褰撳墠璐﹀彿
- `<account_id>.json`锛氬搴旇处鍙风殑鐧诲綍 cookie 缂撳瓨

## 闄愬埗

- 鏆備笉鏀寔浜岀淮鐮佺鍒?- 骞冲彴鎺ュ彛鍙樺寲鍙兘瀵艰嚧鍔熻兘澶辨晥
- 闆疯揪绛惧埌渚濊禆骞冲彴杩斿洖鏁版嵁锛屼笉鑳戒繚璇佹墍鏈夊満鏅彲鐢?
<a id="english"></a>
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
