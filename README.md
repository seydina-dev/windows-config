# Windows Terminal and PowerShell Configuration

This repository contains the configuration files for Windows Terminal and PowerShell `$PROFILE`.

## Windows Terminal Configuration

The Windows Terminal configuration is stored in the `terminal-settings.json` file. This file includes custom key bindings, profiles, and color schemes.

### Key Bindings

- **Copy**: `Ctrl+C`
- **Paste**: `Ctrl+V`
- **Find**: `Ctrl+Shift+F`
- **Split Pane**: `Alt+Shift+D`

### Profiles

#### PowerShell

- **Command Line**: `"C:\\Users\\badia\\AppData\\Local\\Microsoft\\WindowsApps\\Microsoft.PowerShell_8wekyb3d8bbwe\\pwsh.exe" -nologo`
- **GUID**: `{574e775e-4f2a-5b96-ac1e-a2962a402336}`
- **Color Scheme**: `Tokyo Night`
- **Font**: `JetBrainsMono Nerd Font`
- **Opacity**: `78`
- **Use Acrylic**: `true`

#### Arch

- **Background Image**: `C:\\Users\\badia\\Pictures\\archlinux_bg.png`
- **Background Image Opacity**: `0.8`
- **Bell Style**: `none`
- **Color Scheme**: `Tokyo Night`
- **GUID**: `{a5a97cb8-8961-5535-816d-772efe0c6a3f}`
- **Icon**: `C:\\Users\\badia\\Pictures\\archlinux_icon.png`
- **Opacity**: `57`

### Color Schemes

- **Tokyo Night**
- **Tokyo Night Storm**
- **Catppuccin Mocha**
- **Catppuccin Macchiato**
- **Catppuccin Frappe**
- **Catppuccin Latte**

## PowerShell `$PROFILE` Configuration

The PowerShell `$PROFILE` configuration is stored in the `profile.ps1` file. This file includes custom aliases and module imports.

### Aliases

- **`ll`**: `Get-ChildItem | Format-Wide`
- **`which`**: `Get-Command`
- **`rm`**: `Remove-Item`
- **`clr`**: `clear`
- **`pn`**: `pnpm`
- **`px`**: `pnpx`
- **`arch`**: `Arch.exe`
- **`phone`**: `./ -noconsole.vbs`

### Modules

- **Oh My Posh**: `oh-my-posh init pwsh | Invoke-Expression`
- **Terminal Icons**: `Import-Module -Name Terminal-Icons`

### Installation Steps

To install the required modules, follow these steps:

1. **Install Oh My Posh**:

   ```sh
   Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://ohmyposh.dev/install.ps1'))
   ```

2. **Install Terminal Icons**:

   ```sh
   Install-Module -Name Terminal-Icons -Repository PSGallery -Force
   ```

## Usage

To use these configurations, copy the [terminal-settings.json](http://_vscodecontentref_/0) file to the appropriate location for Windows Terminal settings and the [profile.ps1](http://_vscodecontentref_/1) file to your PowerShell `$PROFILE` path.

```sh
# Copy terminal-settings.json to Windows Terminal settings location
cp terminal-settings.json $env:LOCALAPPDATA\\Packages\\Microsoft.WindowsTerminal_8wekyb3d8bbwe\\LocalState\\settings.json

# Copy profile.ps1 to PowerShell $PROFILE path
cp profile.ps1 $PROFILE
```
