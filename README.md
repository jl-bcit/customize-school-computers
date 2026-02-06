# Windows Taskbar Configuration & Optional Software Installer

This PowerShell script customizes several Windows taskbar settings for a more clean layout and can optionally install common desktop applications.

## What This Script Does

### Taskbar & UI Customization
The script modifies Windows registry settings under the current user to apply the following changes:

- **Combine taskbar buttons** only when the taskbar is full
- **Combine buttons on secondary taskbars** only when full
- **Show taskbar apps** on the taskbar where the window is open (multi-monitor setups)
- **Align the taskbar to the left** (Windows 11 style adjustment)
- **Hide the Search box** from the taskbar
- **Hide the Task View button**

After applying these settings, the script **restarts Windows Explorer** to immediately apply the changes.

### Optional Software Installation
When run with the `-software` switch or when the script is entered and executed within PS ISE, the script will also install the following applications:

- **Notion** (downloaded directly from Notion)
- **Discord** (downloaded directly from Discord)
- **Visual Studio Code** (installed via `winget`)

Installers for Notion and Discord are downloaded to the user’s `Downloads` folder and launched automatically.

## Parameters

### `-software`
Optional switch that enables software installation.

```powershell
.\script.ps1 -software
