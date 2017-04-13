# stingray-place-units-from-data

A quick-and-dirty script to place objects in the Stingray editor from Lua data.

When you run this script, the editor reads the desired unit names and their desired positions from a Lua script file. It then spawns the requested units into the current level. When you save the level, the units will get saved along with the rest of the level.

## To use this plug-in

1.  Save the *.stingray-plugin* file into your project, or install it using the **Plugin Manager** in the Stingray editor.

2.  Export the data for your units into a file called `place-units.lua` in the root folder of your project.

3.  Hit **F5** in the editor to force a re-compile of the project and the `place-units` file.

4.  The plug-in adds a new **Create > Place units from file** option to the main menu. Choose this to run the script.

## Data file format

The script assumes that your data file is structured as follows:

```lua
local objects = {
    {
        unit      = "content/models/props/ChamfBox",
        x         = -10,
        y         = -10,
        z         = 0,
        rot_angle = 5
    },
    {
        unit      = "content/models/props/ChamfBox",
        x         = -5,
        y         = -10,
        z         = 0,
        rot_angle = 10
    },
    -- ... add more objects to this array
}

return objects
```
