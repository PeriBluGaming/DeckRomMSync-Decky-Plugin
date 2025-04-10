# Decky-DeckRomMSync
DeckRomMSync is a plugin for Decky-Loader (A plugin for the Steam Deck), a RomM synchronization Client.
It automatically synchronize your RomM Collections to the Steam Deck directly to your retrodeck installation.

No more manual copying of games to your Steam Deck!

## Notice
Please note that the project is currently in alpha. Issues may occur.

## Requirement
- RomM Installation (v.3.8.1)
- Steam Deck with Decky-Plugin ([Install Decky-Plugin](https://github.com/SteamDeckHomebrew/decky-loader))

## Key Features
- automatically detect changes of your RomM Collecction (adding/removing Games)
- enable/disable automatically synchronize for your RomM Collections
- Platform (Game System) matching
- Resync Game
- Delete Game from Steamdeck

## planned Features
- Browse your RomM Library directly on the Steamdeck and download Games
- Save / State synchronization

## How to Install
1. [Install Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader)
2. Download `DeckRomMSync.zip` from releases
3. Transfer zip-file to Steamdeck (or copy url from releases files)
4. Open Decky-Loader > Settings > Enable `Developer options` in main Settings
5. Decky-Loader > Developer
   - `Install Extension from Zip-File` > select `DeckRomMSync.zip` and press `Install`
   - Or paste the url from releases to `Install Extension from url` and press `Install`

## How to configure DeckRomMSync
1. Open Quick Menu > Decky > DeckRomMsync
2. Click on `Go to Settings`
3. The DeckRomMSync Setting Page will show up
4. Go to Tab `ROMM API` and fill in your RomM Settings (RomM API URL, RomM Username, RomM Password)
5. After that press `Save` > A Message will showing up `Connected` or `Disconnected`
   - If the Message showing `Disconnected`, please check your RomM Settings and try again
   - When the RomM Settings are correct and the Message showing `Connected` you can go forward
6. Go to Tab `PLATFORM MATCHING` and fill in your Retrodeck ROM Path (it can be on the Steam Deck or on the SD-Card)
   - After that click `Save`
   - Now you see all your Platforms (Game Systems) under Platforms
   - Then you can matching your available RomM Platforms with the retrodeck Platform paths (select the correct Platform path from the Dropdowns)
   - After selecting a Platform path it will automatically save your settings
7. Go to Tab `COLLECTION SYNC`
   - On this Page you can activate the background synchronization, synchronization interval
   - underneath you see your RomM Collections, with the slider Buttons you can activate the synchronization
   - Every Game has a status icon on the right side
      - green -> Game is synchronized
      - yellow -> Game is not synchronized yet
     - red -> Error (The target Platform has no `Platform matching`). Go to the `PLATFORM MATCHING` Tab and check the Platform matching settings. The synchronization will try again on the next cycle

## Troubleshooting
If you have any problems, it is advisable to check the logs. Go to the DeckRomMSync Settings > `LOG` Tab.
Select the last Logfile from the Dropdown and looking for Errors.

Also try to reload the Plugin: Decky Settings > Extensions > DeckRomMSync > ... > Reload

There is also a Description Tab for detailed configuration descriptions

### RomM API Settings showing `Disconnected`
- Check RomM API URL -> It must start with `http://` or `https://`
- Check IP-Adress and Port
- URL must end with `/api`
- Example URL: `http://192.168.2.180:8001/api`

