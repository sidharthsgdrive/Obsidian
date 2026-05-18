# Voxy setup

## Mods required
- [Voxy](https://modrinth.com/mod/voxy/versions?version=26.1) -- enables LODs, allowing for vastly improved render distances
- [Chunky](https://modrinth.com/mod/chunky/versions?version=26.1) -- pregenerates chunks, so you don't have to manually travel and load them
- [Sodium](https://modrinth.com/mod/sodium/versions?version=26.1&loader=fabric) -- general rendering performance improvement
- [Iris](https://modrinth.com/mod/iris/versions?version=26.1&loader=fabric) -- shader support
- [Photon](https://modrinth.com/shader/photon-shader/versions?version=26.1) -- the shader with best support for Voxy

## Installation
1. Download the above mods.
2. Using your preferred launcher, install Fabric 26.1. A guide: https://www.youtube.com/watch?v=nVYlozhptC0
3. Add the above mods to your `mods` folder.
4. Launch the game.

## Usage
1. Create a singleplayer world with the downloaded backup of the server, or whichever world you want to use Voxy on. To do this, just copy the `world` folder in the server backup to your `saves` folder (the `saves` folder can be found by clicking edit on any singleplayer world, and clicking on open saves folder)
2. Inside the singleplayer world, do Pause Menu -> Open to LAN (Gamemode Creative, Allow Commands On) -> Start LAN world
3. Get the coordinates you want to center the LODs on, and run `/chunky center <x> <z>`
4. Run `/chunky radius <r>c` to set the render distance you're going for, in chunks. For example, `/chunky radius 256c`
5. Run `/chunky start`. The pregeneration will take a while.
6. Once chunky's pregeneration is complete, run `/voxy import world <world_name>`. This will import LODs of the generated chunks to Voxy.
7. Enter the server or world you want to use Voxy on, and run the same command `/voxy import world <world_name>`, with `world_name` being the name of the singleplayer backup world you ran the previous commands on.
8. Enable Photon shaders by pressing K -> open shaders folder -> drag and drop the shaders zip file into the folder. I recommend going into the shader folder and disabling clouds for a cleaner experience.
9. Lower your render distance to 8 or 12 in video settings, for improved performance. Also adjust Voxy's render distance as needd.