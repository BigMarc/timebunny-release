# TimeBunny — downloads

Installers for the TimeBunny desktop agent.

**➡️ [Download page](https://bigmarc.github.io/timebunny-release/)** · [All releases](https://github.com/BigMarc/timebunny-release/releases)

This repository holds released binaries only. The source lives in a private repository.

| Platform | File | Signing |
| --- | --- | --- |
| macOS 10.15+ (Universal) | `TimeBunny_<version>_universal.dmg` | Developer ID, notarised and stapled by Apple |
| Windows 10/11 (x64) | `TimeBunny_<version>_x64-setup.exe` | **Unsigned** — SmartScreen will warn |

## Verifying a download

Each release lists a SHA-256 for every installer on the [download page](https://bigmarc.github.io/timebunny-release/).

```bash
# macOS
shasum -a 256 ~/Downloads/TimeBunny_*.dmg
spctl -a -vvv /Applications/TimeBunny.app   # expect: accepted / source=Notarized Developer ID
```

```powershell
# Windows
Get-FileHash -Algorithm SHA256 $HOME\Downloads\TimeBunny_*-setup.exe
```

## Privacy

TimeBunny records **only while you have a shift running**. Stopping is instant, always available
from the tray icon, and never needs anyone's approval.

**Collected during a shift:** shift start/stop times; three integers per minute (keystroke, mouse
move and mouse click *counts*); screenshots of each monitor at a randomised moment in each capture
interval; the foreground application name per minute; and a once-a-minute diagnostic heartbeat
(agent version, monitor count, permission state, clock skew). Window titles and browser
origin/path are collected only if your company's policy enables them — never the query string.

**Never collected:** the content of anything you type (no keylogging), audio, camera, clipboard,
your files, network traffic, your location, or *anything at all outside an active shift*.

Tracked data is immutable: you cannot edit, blur or delete your own records, and no one else can
without leaving an audit-log entry. The full notice is at `/privacy` in the dashboard.

## Support

Message the team in Slack.
