# Quick manual and commands

[Português (Brasil)](USAGE.md)

## Interface

After installation, b-print remains available in the Windows system tray.

- Left-click the tray icon: capture a region.
- Right-click: region, timer, all monitors, window under cursor, recent
  captures, canvas, pin, Settings, Help, and Exit.
- Print Screen: capture a region.
- Ctrl+Shift+D: configurable secondary shortcut.

The complete Help manual is included in the application.

## Silent installation

```powershell
.\b-print-1.1.0-windows-x64.exe /S /LANG=en
```

With options:

```powershell
.\b-print-1.1.0-windows-x64.exe /S `
  /LANG=en `
  /DIR="$env:LOCALAPPDATA\Programs\b-print" `
  /AUTOSTART=0 `
  /DESKTOP=1 `
  /LAUNCH=0
```

Options:

- `/S`: silent mode.
- `/LANG=pt-BR|en`: installer and initial app language.
- `/DIR=`: installation folder.
- `/AUTOSTART=0|1`: start with Windows.
- `/DESKTOP=0|1`: create a Desktop shortcut.
- `/LAUNCH=0|1`: launch after installation.

## Silent uninstall

Using the installer:

```powershell
.\b-print-1.1.0-windows-x64.exe /uninstall /S
```

Using the installed uninstaller:

```powershell
& "$env:LOCALAPPDATA\Programs\b-print\b-print-desinstalador.exe" --uninstall /S
```

## Installed application commands

```powershell
$app = "$env:LOCALAPPDATA\Programs\b-print\b-print.exe"

& $app --region
& $app --active-screen
& $app --all-screens
& $app --window-under-cursor
& $app --tray
```

Configuration:

```powershell
& $app --configure --desktop-shortcut --autostart
& $app --configure --no-desktop-shortcut --no-autostart
& $app --set-save-dir "D:\Screenshots"
& $app --factory-reset
```

## Verify SHA-256

```powershell
Get-FileHash .\b-print-1.1.0-windows-x64.exe -Algorithm SHA256
```

Compare the result against `SHA256SUMS.txt` from the same Release.
