# how to set up factorio mod development

1. download factorio headless
2. read the doc on how to run factorio headless : https://wiki.factorio.com/Multiplayer#Dedicated/Headless_server
3. copy over the mod-list.json from this folder
4. download all the mods. the easiest way to do this is to use the shell script in factoriotools github repo (https://github.com/factoriotools/factorio-docker). remember to provide username + token (https://factorio.com/profile). Note that UPDATE_MODS_ON_START is bugged in that dockerfile -- just export the bash script instead of using the docker image
5. also check out https://wiki.factorio.com/Mod_portal_API#/api/mods/{mod_name}/full if you want to rewrite that bash script.
6. unfortunately username + pw is required -- /full gives a link to the GH repo but requires some extra automation to download from github.
5. copy a non-zip copy of angelsdev-unit-test into the mod folder (https://github.com/Arch666Angel/mods/blob/master/angelsdev-unit-test). remember to name it properly (angelsdev-unit-test_0.0.1)
6. add it to mod-list.json manually
7. create a new save
8. run the new save
9. download https://mods.factorio.com/mod/big-data-string in order to be able to inspect data at the data.lua and data-updates.lua etc. phases, if needed for unit testing
10. remember https://forums.factorio.com/viewtopic.php?t=25419 to use this for logging if needed
11. check out https://github.com/ZwerOxotnik/factorio-example-mod for some sample code and to bootstrap your mod
12. read the official factorio docs, especially https://lua-api.factorio.com/1.1.70/Instrument.html and https://lua-api.factorio.com/1.1.70/ and https://wiki.factorio.com/Prototype_definitions
13. Hot edit angelsdev to do every tick, instead of every 60 ticks
14. Run the server, and type a message in chat to force the game to process a tick -- otherwise the unit tests will never run!!
14. Dont use the python scripts in angelsdev-unit-test, they not helpful. mod_downloader.py too.

Other misc links:

https://raw.pics.io/#
https://raw.githubusercontent.com/kirazy/reskins-angels/master/graphics/icons/refining/intermediates/slag.png
https://github.com/kirazy/reskins-angels/blob/34a58e3a1671348e65391f3ed705d6b01eafb9c6/prototypes/items/smelting.lua
https://github.com/kirazy/reskins-angels/blob/34a58e3a1671348e65391f3ed705d6b01eafb9c6/prototypes/items/smelting-updates.lua
https://github.com/kirazy/reskins-angels/blob/34a58e3a1671348e65391f3ed705d6b01eafb9c6/prototypes/items/smelting.lua
https://github.com/kirazy/reskins-angels/blob/34a58e3a1671348e65391f3ed705d6b01eafb9c6/prototypes/items/smelting.lua
https://github.com/kirazy/reskins-angels/blob/master/data-final-fixes.lua
https://github.com/kirazy/reskins-angels/blob/master/data-final-fixes.lua
https://github.com/kirazy/reskins-angels/blob/master/data-updates.lua
https://github.com/kirazy/reskins-angels/search?q=adjust_alpha


https://github.com/kirazy/reskins-angels/blob/master/prototypes/functions/triggers.lua
https://github.com/kirazy/reskins-angels/tree/master/prototypes/functions
https://github.com/kirazy/reskins-library/blob/master/prototypes/functions/tints.lua
https://github.com/kirazy/reskins-library/tree/master/prototypes/functions
https://github.com/kirazy/reskins-angels/blob/master/prototypes/items/smelting/ores.lua

https://pixlr.com/x/#editor

https://github.dev/Arch666Angel/mods/tree/master/angelsrefining

https://github.com/Arch666Angel/mods/blob/145d2fd2b676715d1943d07421c20a92432c0858/angelsrefining/graphics/icons/iron-slag.png

https://raw.githubusercontent.com/Arch666Angel/mods/145d2fd2b676715d1943d07421c20a92432c0858/angelsrefining/graphics/icons/slag.png

https://github.com/Arch666Angel/mods/blob/145d2fd2b676715d1943d07421c20a92432c0858/angelsrefining/prototypes/angels-functions.lua

https://github.com/Arch666Angel/mods/blob/6e8239e58eb075371e83b8031aaf33fa07db1e1e/angelsrefining/data.lua
https://github.com/Arch666Angel/mods/search?q=angelsmods.trigger.ores

https://docs.google.com/document/d/1M4zmg96l6Mm5K9t1igQwRkMsr0vYv6kkVIyHHlg3DPA/edit


