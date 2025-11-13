# FarmLan 2025-11-14_16

## Preparation

### Disable Steam Direct Transfers

We utilize LANCache to allow local cached downloads. Having this setting enabled will interfere with LANCache.

Disable it with these steps.

1. Open the Steam client on your PC.
1. Go to the `Settings` menu.
1. Select the `Downloads` tab.
1. Under the `Game File Transfer over Local Network` section, toggle the option to `Off`.

### LAN Provided Files

All LAN games and files that aren't hosted on steam will be located at the following share. The share does not have a password.

1. Open your file browser of choice or press ++windows+r++
1. Enter `\\share\public`
1. Username: `share`

Alternatively you can open `Windows Terminal` or `PowerShell` and copy the command below to map as a network drive. At the `credentials prompt`, just press ++enter++, since there is no password

```powershell
New-PSDrive -Name "A" -Root "\\share.farmlan.ca\public" -Persist -PSProvider "FileSystem" -Credential share -ErrorAction Ignore
```

!!! warning
    After the LAN the network drive will not be accessible and will always show disconnected. You can Rightclick and remove the share after the LAN.

## Connecting to Servers

!!! note
    If you do not see any instructions for a particular game, the invites are handled by Steam.

Below are instructions for connecting to the dedicated server we have configured for the event.

### COD4 - IW4x

1. Launch `iw4x-launcher.exe` in the IW4x folder
1. Select `Join Game`
1. Change `Source` to `Local`
1. Connect to `FarmLAN Server01 or 02`

### Natural Selection 2

1. Launch Natural Selection 2 from `Steam`
1. Select `Play` and then `Community Servers`
1. The FarmLAN server should be at the top of the list
	- If it is not, select `Filter` and search for `FarmLAN`
1. If neither of those options work, launch the console via `~`
1. Enter `Connect 192.168.5.7`

### Terraria

1. Launch Terraria from `Steam`
1. Select `Multiplayer`
1. Select `Join via IP`
1. Select or create your character
1. Enter Server IP of `192.168.5.7`
1. Enter Server Port of `7777`

### Valheim

1. Launch Valheim from Steam
1. Select or create  your character
1. Select `Join Game`
1. Select `Add Server` and enter `192.168.5.7:2456`

### Counter Strike 2

!!! note
    If the ++tilde++ key doesn't show up when pressed, enable the option via Settings `Game` and `Enable Developer Console` switched to `Yes`

1. Launch Counter Strike 2 from Steam
1. Bring up the console with ++tilde++
1. Enter `Connect 192.168.5.7` for Deathmatch
1. Enter `Connect 192.168.5.8` for Gun Game

### PowerBomberMan

1. Launch Powerbomberman
1. Select `Battle Mode`
1. Select `Online Battle`
1. Select `Connect to Server` and then `Add Server`
1. Server Address `192.168.5.8` Port `64640`


## Game Installations

!!! note
    If the game you are looking for isn't on this list, it should be downloaded via Steam
Below are instructions for installing any LAN specific game.

We recommend creating a specific folder on your computer for the LAN files. Common places are in the root of C:\ or a desktop folder. Transfer all files to this folder.

We also have available a bunch of optional games in the folder, feel free to poke around and see if anyone else is interested! Most of the other files with be portable or very basic installers.

### COD MW2 - IW4x

!!! note
    If you own Call of Duty: Modern Warfare 2 on Steam, download the game via Steam to utilize LANCache. Then you're only required to copy `iw4x-launcher.exe` from the share.

1. From `\\share.farmlan.ca\public\Installers\FPS\Modern Warfare 2`, copy over `iw4x_full_game_w_files.7z`
1. Extract `iw4x_full_game_w_files.7z`
    - after it has completed, you can delete the archive
1. From the share copy `iw4x-launcher.exe` to the extracted folder
1. Launch iw4x-launcher.exe
1. Wait for the launcher to update and install any required files
    - If you are prompted to download DLC, select yes
1. If this is your first time playing IW4x, run the following commands
    - Open the console with ++tilde++ in the main menu
    - Type: `unlockstats`
    - Close the console, you should now see `create a class` available
1. Adjust your Video settings as required

### Blur

1. From `\\share.farmlan.ca\public\Installers\Other`, copy over `Blur_Win_EN_Full-Rip.zip`
1. Extract `Blur_Win_EN_Full-Rip.zip`
1. Run "Blur.exe"
1. Adjust display settings as required

### Battlefield 3
1. Install Battlefield 3 via `Steam`
1. From `\\share.farmlan.ca\public\Installers\FPS\Battlefield 3` copy `BF3-Client.zip` then extract
1. From `*\BF3-Client\BF3\Core` copy the `winhttp.dll` file to "Core" folder into Steam installation Path
1. From `*\BF3-Client\BF3\` copy the remaining files to the root folder of the Steam installation Path
1. Run `BFULauncher`

### Rounds
1. Install Rounds via `Steam`
1. Right click on Rounds in Steam and select `Properties`
1. Select `Betas` and select `Old-rounds-for-mods`
1. Close dialogue box and let Rounds update
1. From `\\share.farmlan.ca\public\Installers\FPS` copy `Thunderstore Mod Manager - Installer.exe` then install it
1. Open `Thunderstore Mod Manager` and search for `Rounds` and select game
1. Select `Import` then `Import new profile`
1. Enter `019a6621-6e49-f7a0-0d80-fe9b3ebbc8ef`
1. Launch `Modded` in top right hand corner and ensure game launches

### Warcraft 3

1. From `\\share.farmlan.ca\public\Installers\RTS\Warcraft 3 - portable`, copy the `Warcraft III` folder to your LAN folder
1. Launch `Frozen Throne` and set display settings

### Beyond All Reason

!!! warning
    You may have to start the game once for the maps folder to appear

1. From `\\share.farmlan.ca\public\Installers\RTS\Beyond-All-Reason` copy `Beyond-All-Reason-1.2988.0.exe` to your LAN folder
1. Run Launcher and complete the installation
1. From `\\share.farmlan.ca\public\Installers\RTS\Beyond-All-Reason` copy `Beyond-All-Reason-Maps.7z` to your LAN folder
1. Extract `Beyond-All-Reason-Maps.7z` into `*\Beyond-All-Reason\data\maps`


### Worms Armageddon

1. From `\\share.farmlan.ca\public\Installers\Other\Worms Armageddon`, copy `Worms Armageddon.exe` to your LAN folder
1. Run `Worms Armageddon.exe` and accept the EULA

### Stronghold Crusaders

1. From `\\share.farmlan.ca\public\Installers\RTS\Stronghold Crusaders`, copy `setup.exe` to your LAN folder
1. Run `setup.exe` and complete the installation
1. Delete "Extreme" shortcut from the desktop

### Unreal Tournament 2004

1. From `\\share.farmlan.ca\public\Installers\FPS\Unreal.Tournament.2004.Editor's.Choice.Edition-GOG`, copy `setup_ut2004_2.0.0.6.exe` to your LAN folder
1. Run `setup_ut2004_2.0.0.6.exe` and complete the installation

### Power BomberMan

1. From `\\share.farmlan.ca\public\Installers\Other`, copy `Power Bomberman` directory to your LAN folder
1. Run `Power Bomberman.exe` and complete the installation
1. Setup your controls