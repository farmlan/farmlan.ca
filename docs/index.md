# FarmLan 2025-11-14_16

## Preperation

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

!!! warning " "
    After the LAN the network drive will not be accessable and will always show disconnected. You can Rightclick and remove the share after the LAN.

### Game Installations

!!! note " "
    If the game you are looking for isn't on this list, it should be downloaded via Steam
Below are instructions for installing any LAN specific game.

We recommend creating a specific folder on your computer for the LAN files. Common places are in the root of C:\ or a desktop folder. Transfer all files to this folder.

We also have available a bunch of optional games in the folder, feel free to poke around and see if anyone else is interested! Most of the other files with be portable or very basic installers.

#### COD MW2 - IW4x

!!! note
    If you own Call of Duty: Modern Warefare 2 on Steam, download the game via Steam to utilize LANCache. Then you're only required to copy `iw4x-launcher.exe` from the share.

1. From `\\share.farmlan.ca\public\Installers\FPS\Modern Warfare 2`, copy over `iw4x_full_game_w_files.7z`
1. Extract `iw4x_full_game_w_files.7z`
    - after it has completed, you can delete the achrive
1. From the share copy `iw4x-launcher.exe` to the exctracted folder
1. Launch iw4x-launcher.exe
1. Wait for the launcher to update and install any required files
    - If you are prompted to download DLC, select yes
1. If this is your first time playing IW4x, run the following commands
    - Open the console with ++tilde++ in the main menu
    - Type: `unlockstats`
    - Close the console, you should now see `create a class` available
1. Adjust your Video settings as required

### Blur
1. From the LAN share (Other/Blur), copy over "Blur_Win_Full-Rip.ZIP"
2. Extract contents of the ZIP
3. Run "Blur.exe"
4. Adjust display settings as required

### Battlefield 3
1. Install Battlefield 3 via Steam
2. Copy over BF3-Client.ZIP from the LAN share (FPS/BF3)
3. Extract "Core" files into "Core" folder in battlefield 3 installed folder
4. Extract remaining files into battlefield 3 installed folder
5. Run "BFULauncher"

### Rounds
1.  Install Rounds via Steam
2.  Right click on Rounds in Steam and select "Properties"
3. Select "Betas" and select "Old-rounds-for-mods"
4. Close dialogue box and let Rounds update
5.  Install "thunderwolf mod manager" - On LAN folder (FPS/Thunderstore)
6. Search for "Rounds" and select game
7. Select "Import" and "Import new profile"
8. Enter the following code
	-   	019a6621-6e49-f7a0-0d80-fe9b3ebbc8ef
10. Launch "Modded" in top right hand corner and ensure game launches

### Warcraft 3
1. From the LAN share (RTS/WarCraft3), copy over the "Warcraft III" folder into your LAN folder
2. Launch "Frozen Throne" and set display settings

### Beyond All Reason
1.  From the LAN share (RTS/Beyond-ALL-Reason), run "Beyond-All-Reason-1.2988.0.exe"
2. Change install directory to "LAN" folder
3. Run Launcher and allow it to finish installing game
4. Unpack and transfer map pack into \LAN\Beyond-All-Reason\data\maps
	- You may have to start the game once for the maps folder to appear

### Worms Armageddon
1. From the LAN share (Other/Worms), run "Worms Armageddon.exe"
2. Select options and change install directory to "Lan" folder
3.  Accept the EULA and install

### Stronghold Crusaders
1. From the LAN share (RTS/Stronghold), run "setup.exe"
	- You can't change install location
2. Delete "Extreme" shortcut from the desktop

### Unreal Tournament 2004
1. From the LAN share (FPS/Unreal), run "Setup_ut2004_2.0.0.0.6"
1. Select options and change install directory to "Lan" folder
1. Accept the EULA and install

### Power BomberMan
1. From the LAN share (Other/Bomberman), copy over Bomberman folder
2. Run "Power Bomberman.exe"
3. Setup your controls

## Connecting to Servers

Below are instructions for connecting to any dedicated server we have configured for the event. If you do not see any instructions for a particular game, you will be invited to it via a steam invite.
### COD4 - IW4x
1. Launch "iw4x-launcher.exe" in the IW4x folder
2. Select "Join Game"
3. Change "Source" to "Local"
4. Connect to FarmLAN Server01 or 02

### Natural Selection 2
1. Launch Natural Selection 2 from Steam
2. Select "Play" and then "Community Servers"
3. The FarmLAN server should be at the top of the list
	- If it is not, select "Filter" and search for "FarmLAN"
4. If neither of those options work, launch the console via "~"
5. Enter "Connect 192.168.5.7"

### Terraria
1. Launch Terraria from Steam
2. Select "Multiplayer"
3. Select "Join via IP"
4. Select or create your character
5. Enter Server IP of "192.168.5.7"
6. Enter Server Port of 7777

### Valheim
1. Launch Valheim from Steam
2. Select or create  your character
3. Select "Join Game"
4. Select "Add Server" and enter "192.168.5.7:2456"

### Counter Strike 2
We have 2 servers configured for Counter Strike 2. Server 01 is Deathmatch and Server02 is Gun Game
1. Launch Counter Strike 2 from Steam
2. Bring up the console with "~"
	- If this is the first time at the LAN, enable this option via Settings
	- "Game" and "Enable Developer Console" switched to Yes
3. Enter "Connect 192.168.5.7" for Server 01
4. Enter "Connect 192.168.5.8" for Server 02

### PowerBomberMan
1. Launch Powerbomberman
2. Select "Battle Mode"
3. Select "Online Battle"
4. Select "Connect to Server" and then "Add Server"
5. Server Address "192.168.5.8" Port "64640"
