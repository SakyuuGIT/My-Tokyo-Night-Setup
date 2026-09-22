# Komorebi - Tokyo Night

This folder contains my personal **Komorebi** configuration for my Tokyo Night setup.

Most of the configuration comes from **Darren Lingters**, whose Windows customization work has been an important reference and source of inspiration for my own setup. The configuration may sometimes be edited or adapted by me to fit my personal setup.

## Installation

### 1. Install Komorebi and whkd

The easiest way to install both **Komorebi** and **whkd** is with Scoop.

First, make sure Scoop is installed, then run:

```powershell
scoop bucket add extras
scoop install komorebi whkd
```

`whkd` is installed separately from Komorebi. It is used to handle the keyboard shortcuts that control Komorebi.

For more information and alternative installation methods, refer to the official Komorebi documentation:

[Komorebi - Official Documentation](https://lgug2z.github.io/komorebi/)

### 2. Install the configuration

1. Open your Komorebi configuration folder.
2. Back up your existing configuration files.
3. Copy the configuration files from this folder into the appropriate Komorebi configuration directories.
4. Replace the existing files if prompted.
5. Make sure your `whkdrc` configuration is placed in the appropriate `.config` directory.
6. Start Komorebi with whkd using the command below.

> **Important:** Make a backup of your existing Komorebi and whkd configuration files before replacing them.

## Basic Commands

Komorebi is controlled through the `komorebic` command-line interface.

### Start Komorebi and whkd

```powershell
komorebic start --whkd
```

This starts Komorebi together with whkd so that your configured keyboard shortcuts are active.

### Stop Komorebi and whkd

```powershell
komorebic stop --whkd
```

### View available Komorebi commands

```powershell
komorebic --help
```

You can also get help for a specific command:

```powershell
komorebic <command> --help
```

For example:

```powershell
komorebic start --help
```

## Shortcuts

Komorebi itself does not handle keyboard shortcuts.

The shortcuts are handled by **whkd**, using its `whkdrc` configuration file. The commands defined in `whkdrc` communicate with Komorebi through `komorebic`.

You can display the available Komorebi-related shortcuts with:

```powershell
komorebic toggle-shortcuts
```

You can also inspect your `whkdrc` file directly to see and modify the configured shortcuts.

## Autostart

### Enable autostart

To start Komorebi automatically when Windows starts:

```powershell
komorebic enable-autostart
```

To include whkd:

```powershell
komorebic enable-autostart --whkd
```

### Disable autostart

```powershell
komorebic disable-autostart
```

## Configuration

The configuration contains my personal setup for:

- Window management
- Workspace layouts
- Multi-monitor workspaces
- Window padding
- Window hiding behaviour
- Cross-monitor window movement
- Applications excluded from Komorebi
- whkd keyboard shortcuts

### Workspaces

**Monitor 1**

- `I` → BSP
- `II` → Grid
- `III` → UltrawideVerticalStack

**Monitor 2**

- `Home` → Rows
- `2` → Rows
- `3` → Rows

### Ignored applications

The configuration excludes several applications from Komorebi management:

- `ACShadows.exe`
- `Overwatch.exe`
- `Photos.exe`
- `PotPlayerMini64.exe`
- `AmneziaVPN.exe`
- `Elgato.WaveLink.exe`

## Quick Reference

| Action | Command |
|---|---|
| Start Komorebi + whkd | `komorebic start --whkd` |
| Stop Komorebi + whkd | `komorebic stop --whkd` |
| Show all commands | `komorebic --help` |
| Show command help | `komorebic <command> --help` |
| Show shortcuts | `komorebic toggle-shortcuts` |
| Enable autostart | `komorebic enable-autostart` |
| Enable autostart + whkd | `komorebic enable-autostart --whkd` |
| Disable autostart | `komorebic disable-autostart` |

## Credits

The majority of this configuration is based on the work of **Darren Lingters**.

His Windows customization work and videos have been an important source of inspiration for my own setup.

**Creator:** [MrDLingters](https://github.com/MrDLingters)  
**YouTube:** [@darrenlingters3512](https://www.youtube.com/@darrenlingters3512)

The configuration included here may be edited or adapted over time for my personal setup.

## Komorebi

[Komorebi GitHub](https://github.com/LGUG2Z/komorebi)

[Komorebi Documentation](https://lgug2z.github.io/komorebi/)
