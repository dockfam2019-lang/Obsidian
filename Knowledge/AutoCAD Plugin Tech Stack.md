# AutoCAD Plugin Tech Stack

Related: [[Projects/AutoCAD Tracking Plugin]]

## Language
C# — .NET Framework 4.8 (net48). Required by AutoCAD 2020-2024.

## Platform
Windows only. AutoCAD is 64-bit Windows. No Mac support in V1.

## Key Libraries
- AutoCAD .NET API — `accoremgd.dll`, `acmgd.dll`, `acdbmgd.dll`
- `System.Text.Json` — local JSON buffer serialization
- Google Sheets API v4 — for uploading session data (Phase 6)

## Architecture
- No backend server — plugin POSTs directly to Google Sheets API
- Data buffered locally in `pending.json` if upload fails
- Retries on next AutoCAD startup
- One row per drawing session in Google Sheets

## Install
Copy `.bundle` folder to `%APPDATA%\Autodesk\ApplicationPlugins\`
AutoCAD auto-loads it on next startup. No admin rights needed.

## Targets
AutoCAD 2020–2024 (R23.1–R24.3)

## Key Files
- `PluginEntryPoint.cs` — entry point, loads silently
- `SessionRecord.cs` — data shape for one drawing session
- `ConfigLoader.cs` — reads config.json (Spreadsheet ID, service account key)
- `PackageContents.xml` — tells AutoCAD where to find the DLL
