# Nova Download

Public download repository for Nova, a customizable on-screen keyboard for Windows by Remington Inc.

## Download

Latest Windows package:

https://github.com/lJazzpahlol/nova-download/releases/latest/download/Nova-win64.zip

## Install

1. Download the zip.
2. Extract it anywhere you like.
3. Open the extracted folder.
4. Double-click `Nova.exe`.
5. Accept the Windows UAC prompt.

Nova runs elevated so it can type into elevated windows too, the same kind of access the Windows On-Screen Keyboard needs.

No accounts. No telemetry. Prediction data and learned words stay local.

## Maintainer Notes

Build from the private/source workspace:

```powershell
cd C:\Users\remto\OneDrive\Desktop\projects\Nova
.\tools\build_release.bat
```

The release asset should stay named `Nova-win64.zip` so website links can use:

```text
https://github.com/lJazzpahlol/nova-download/releases/latest/download/Nova-win64.zip
```

## Updates

Nova checks for new versions on launch. When one is available, a Windows notification appears and you can update in place from the NOVA tray icon (right-click, then Update) - no manual re-download needed. Your settings and learned words are kept. Normal app fixes ship as a small `Nova-patch-win64.zip`; installed copies prefer that automatically and fall back to the full `Nova-win64.zip` if the patch is missing or fails.

The app-only patch is built with:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File tools\build_patch.ps1 -CopyToDownloadRepo
```

Publish both `Nova-win64.zip` and `Nova-patch-win64.zip` on the same release.
