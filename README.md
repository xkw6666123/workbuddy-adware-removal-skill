# WorkBuddy Adware Removal Skill

A WorkBuddy skill that scans and removes unwanted adware, bundled software, and popup ad software from Windows systems.

## What It Does

Scans **6 key locations** on your Windows system to find and remove adware:

| Scan Target | What It Finds |
|-------------|---------------|
| Registry (installed programs) | All installed software names, publishers, paths |
| Running processes | Active adware processes |
| Windows services | Adware registered as system services |
| File directories | Adware folders in Program Files, AppData, ProgramData, drivers |
| Startup items | Programs set to launch on boot |
| Scheduled tasks | Timed popup ad triggers |

**Built-in detection** for common Chinese adware: 360安全卫士, C盘清理大师, Dll修复工具箱, 花生清理, 芒果快压, 2345系列, 鲁大师, 驯动精灵, and more.

## How It Works

1. **Scan** - Parallel scans of registry, processes, services, directories, startup items, and scheduled tasks
2. **Stop** - Kill adware processes and disable adware services
3. **Delete** - Remove accessible files from AppData, LocalLow, Temp directories
4. **Report** - Generate a detailed cleanup report with manual instructions for items that need admin rights

## Limitations

- Without **administrator privileges**, system-level files (Program Files, drivers, system services) cannot be deleted. The skill will generate a manual cleanup report for these items.
- Detection relies on **keyword matching** - known adware names are detected reliably, but disguised or unfamiliar adware may be missed.

## Installation

### Method 1: Copy to WorkBuddy skills directory

1. Download or clone this repo
2. Copy the `workbuddy-adware-removal-skill` folder to your WorkBuddy skills directory:
   - Windows: `C:\Users\<YourName>\.workbuddy\skills\windows-adware-removal\`
   - macOS: `~/.workbuddy/skills/windows-adware-removal/`
3. Restart WorkBuddy - the skill will be automatically detected

### Method 2: Use in WorkBuddy directly

Tell WorkBuddy: "帮我清理弹窗广告" or "remove adware from my computer" - it will activate this skill automatically.

## Usage Examples

- "帮我清理360安全卫士"
- "我的电脑有弹窗广告，帮我清理"
- "remove 2345 from my computer"
- "扫描流氓软件"

## Common Adware Targets

| Software | Publisher | Typical Location |
|----------|-----------|-----------------|
| 360安全卫士 | 360/奇虎 | C:\Program Files (x86)\360\ |
| C盘清理大师 | 成都赤侠 | C:\Program Files (x86)\SysCleaner\ |
| Dll修复工具箱 | 成都汇电时代 | C:\Program Files (x86)\DllRepairTools\ |
| 花生清理 | 天津拂云 | C:\Program Files (x86)\PeanutClean\ |
| 芒果快压 | 天津简诚 | C:\Program Files (x86)\MangoZip\ |
| 2345系列 | 2345 | C:\Program Files (x86)\2345\ |
| 鲁大师 | 鲁大师 | C:\Program Files (x86)\Ludashi\ |
| 驯动精灵 | 驯动精灵 | C:\Program Files (x86)\DriverGenius\ |

## Requirements

- WorkBuddy desktop app (latest version)
- Windows 10/11
- Administrator privileges recommended for full cleanup (without admin, user-level cleanup + manual report)

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Contributing

Feel free to submit issues or pull requests to add more adware patterns or improve detection accuracy.
