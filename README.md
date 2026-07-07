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
