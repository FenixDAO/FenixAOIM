<img width="645" height="642" alt="image" src="https://github.com/user-attachments/assets/f1fd3c11-fd5a-4953-a72d-2c00544f7c02" />

# FenixAOIM
An interactive map for Anarchy Online, where you can teleport by clicking the warp markers, with multiple characters. Works great for blitzing nanos.

## Overview

- An Interactive map for Anarchy Online, in the form of an AOSharp plugin. See [here](https://gitlab.com/never-knows-best/aosharp) for more information on AOSharp.
- This tool allows you to have a fully zoomable map, with clickable markers to initiate teleports utilising Scottyboi's ingame warpers. It also allows you to initiate this from multiple characters at once. 
- All missions are shown, and clicking them sets them active ingame (This was for setting the waypoint on a mission before hitting nearest warp).
- A hotbar is also located at the top of the screen to allow for common places / frequently used warps to be added. (This can be customised easily; See usage guide below).
- The ingame coordinates / pins are stored as .JSON information; the aim was to make it easily customisable, allowing for the introduction of new tags, or adding your own custom warp bots. 

NOTE: This is early in the development, and may not be fully optimised or stable. Use at your own risk. I do not provide any support with the application, and by downloading and using it you are accepting responsibility for its use. 

Recommendations:
One of the main issues (That I still have to solve), is when you are hovering the map and scroll out, your AO client also zooms out; I use this to lock the camera
1. Hit F10
2. Controls > Mouse
3. Mouse scroll wheel over world = No effect

Also, if using SyncManager plugin already, set the TeamInviteOutside to on, so that it auto accepts the warp invite.

## Usage Guide
**Setting up**
1. Add it just like any other AOSharp plugin. 
2. <img width="213" height="14" alt="Image" src="https://github.com/user-attachments/assets/37c99a8b-9cdd-45af-97d9-8737a4a54418" />
3. Type "/map" (Currently only lowercase). This should launch the map in a new window.

NOTE: This is opened for the character who initiates it, and cannot be opened on other characters unless first closed on the previous character.

If you see this when you attempt to warp <img width="343" height="20" alt="image" src="https://github.com/user-attachments/assets/a13b2622-6018-473c-84ec-ce51f86dee8b" />
it means that your character_ids.txt file does not contain Scottyboi or his ID (Or the ID of the custom player if you have custom warps).
Scottyboi's ID is 1425923920, found from [here](https://rubi-ka.net/) 
Adding additional entries should look like this:

<img width="266" height="64" alt="image" src="https://github.com/user-attachments/assets/f9021c2c-aa66-4f71-b44c-d479bf8cf0be" />

**General Usage**
In the bottom left is three buttons (From left to right)
1. Move to Player (Centers the player).
2. Move to next mission (Cycles through them)
3. Follows the player if enabled. Clicking on the map disables this.

**Quick Markers**
quick_access.txt is Located in the MapData folder. Open this to modify or customise your favourite teleports. There are multiple examples.

**Making Markers**
From the Markers tab located on the Menu Bar, You can select Add Marker at Player (Creates a new marker with the current position / playfield already prefilled).
1. Label: A custom label can be written here (And disabled by the "Show label on map" at the bottom).
2. Prefix: The user that the message will be sent to. You can change the user for custom warp bots (Though they will need to be added to character_ids.txt) Character ID's can be found [here](https://rubi-ka.net/)
3. Message: What will be sent to the user.
4. Group: This can be used to create a grouping of buttons. (This allows for controlling whole groups layer height and size, and even to enable and disable them from specific layers on the main map)
5. Z-Order: This is the height of the markers (Highest being front).
6. Show on: This enables the markers only on the maps selected.
7. Zone: Which zone the marker is in (Should be autopopulated on "Add Marker at Player").
8. X/Y: The coordinates for X and Y
9. Color: Hex colour value for the marker.
10. Icon: This is where a custom marker can be selected (More can be added to the "/MapData/Icons/" folder).
11. Clickable: If the button can be clicked (To initiate warp message).
12. Show label on Map: If you want this label to be shown.

NOTES: The information is saved between creations, such as icon / group. To aid in the creation of mapping out groups such as fixer grid.

**Editing Markers**
From the Markers tab located on the Menu Bar, You can select Edit Markers to open the Edit Markers Panel.
1. Group Z-Order: Under the menu bar, there is the groups of current pins.
2. Raise: The selected group will have all it's markers add +1 to their z-layer.
3. Lower: The selected group will have all it's markers remove -1 from their z-layer.
4.  Set Layers: This allows you to set the groups visibility per map layer.
5.  Set Size: Allows you to set the size of the pins in the group.

**Map Layers**
The application will auto switch between layers depending on zoom level. If you would prefer this to remain static, just select which layer you would like active in Map, located on the Menu Bar.
Alternatively, to re-enable autoswitching, just select Auto Layer by Zoom.

## Aims and goals
- Realistically, I would like a clean copy of the map. That would be a huge undertaking unless one was obtainable from Saavicks. (That way I could compile 3-5 versions of the map at varying qualities and it would be much more consistent, and all the pins would be done via .JSON configs).
- I would eventually like to have all the map information translated
- Add the ability to resize individual pins.
- Will release the source code when I'm happy with it!
- I plan on adding a revising "Label" to be "Description" and adding a further field for "Visual name". For situations where you want to shorten the map identifier (This could also be a remedy for tags with the same name (Like fixer grid exists)).

## Support
Support me [here](https://ko-fi.com/fenixdao)
