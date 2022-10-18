# Multiplayer bandwidth fix settings for Satisfactory

## Important notes before you get started
**DO NOT**__ copy the .ini files over your own. Only change the settings provided below in your own.
By default, the game's maximum bandwidth appears to be throttled at 64 KB/s. 
By editing the config files, this limit is increased to 800 Mbit/s.
At lower-end machines or internet connections, use 480000 everywhere there is 104857600, this sets the limit to 480 KB/s or ~3.66 Mbit/s. 

## The process
* Step 0: Understand that you assume all risk for anything you break on your system making these changes
* Step 1: Open explorer or a run bar and paste this in the text field `%AppData%\..\Local\FactoryGame\Saved\Config\Windowsnoeditor\`
* Step 2: Make a copy of all your original files and move them somewhere safe
* Step 3: Edit your .ini files with the items listed in reference changes
* Step 4: For each file edited, right click --> Properties --> check the box for "read only"
* Step 5: change network quality in game to medium
* Step 6: change network quality in game to ultra

## Windows .ini file location
`%AppData%\..\Local\FactoryGame\Saved\Config\Windowsnoeditor\`

## Linux (Proton) .ini file location
/home/../.local/share/Steam/steamapps/compatdata/526870/pfx/drive_c/users/steamuser/AppData/Local/FactoryGame/Saved/Config/WindowsNoEditor/

## Reference changes
**SET THE FILES AS READ-ONLY OTHERWISE SATISFACTORY WILL OVERWRITE THEM**
```
# Engine.ini
[/Script/Engine.Player]
ConfiguredInternetSpeed=104857600
ConfiguredLanSpeed=104857600

[/Script/OnlineSubsystemUtils.IpNetDriver]
MaxClientRate=104857600
MaxInternetClientRate=104857600

[/Script/SocketSubsystemEpic.EpicNetDriver]
MaxClientRate=104857600
MaxInternetClientRate=104857600 ```

# Game.ini
[/Script/Engine.GameNetworkManager]
TotalNetBandwidth=104857600
MaxDynamicBandwidth=104857600
MinDynamicBandwidth=10485760

# Scalability.ini
[NetworkQuality@3]
TotalNetBandwidth=104857600
MaxDynamicBandwidth=104857600
MinDynamicBandwidth=10485760
```
## Fandom Wiki Link
https://satisfactory.fandom.com/wiki/Multiplayer
