## Installation
Windows/Linux: Install via exe/commandline, use web GUI
Android: Syncthing-Fork app from play store

## Usage
1. Open web GUI by searching for "syncthing configuration page" in start menu
2. Find folder path of default folder under "Folders", copy Vault contents to that folder
3. Under "Remote Devices", select "Add Remote Device" and enter the device ID of the new device (shown under "Actions" in that new device's Syncthing interface).
4. On the new device, create a new folder with the same ID as the folder of original device (here, `default`)  and turn on the original device under "Devices" while creating the folder. Note: For Android, don't use the default Syncthing folder, as Obsidian doesn't allow access from there. Just use a folder in Documents or something.
5. Now files should be synced. 

## Advantages
- Unlike the Google Drive method, this doesn't rely on additional third-party apps to sync the files to Android, allowing for a cleaner, ad-free experience.
- I found this method also copies the `.obsidian` folder which contains themes, plugins, etc, making them available on mobile.

### Notes
`25/08/25` Desynced Windows, since it seems to be causing some conflicts with Linux. Perhaps it's to do with the two machines sharing the same IP address.
`28/08/25` I thought the issue could be because of time desyncing, but later realized I hadn't enabled Fedora in the windows syncthing web UI.