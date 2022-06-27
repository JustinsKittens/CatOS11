This is the repository for CatOS11. To use CatOS11 on the web, go to this url: https://justinskittens.github.io/CatOS11/ To use CatOS11 on Windows 10, go to the releases and download the latest catos.zip file.

CatOS11 Developer Program
==========================
Heres how to develop a game or app for CatOS11.

If you want a quickstart, download the exampleApp.sb3 file, go to turbowarp.org and make sure you meet the Easy Developing requirements below, then load the file into the editor and start making changes. If not, read the documentation below.

## Requirements ##

### EASY DEVELOPING REQUIREMENTS ###
#### A web browser ####
If you're on Windows 10, then you'll need a web browser once. Otherwise, you'll need a web browser every time you use or develop for CatOS11.
For Windows 10, you can go to https://desktop.turbowarp.org and download the desktop version of Turbowarp. For anything else, go to https://turbowarp.org and use it from there.
#### Addons ####
So from Turbowarp click the Addons button in the top left and make sure you have these things enabled:
Developer Tools
    ENHANCE "CLEAN UP BLOCKS"
File Drag and Drop
    USE HD UPLOADS
Pause Button
Mouse Position
HD Image Uploads
    Original Size
Variable Mananger
Gamepad Support (If you want to use controllers in your app or game)
Sprite Folders
Block Switching
   Every Option
   Arguments in own custom block
Remove Curved Stage Border
Grab Single Block with Ctrl key
Hide New Variables
Extra Key Support
   ENABLE EXPERIMENTAL KEYS
   ENABLE SHIFT KEYS
   ENABLE TURBOWARP KEYS
Do Not Shift Pasted Items
Duplicate scripts with Alt key
Switch variables between "For all sprites" and "For this sprite only"
Enable some other addons if you want to.

### Sprites ###
1 Icon sprite per app
    It must have 2 types: taskbar and desktop.
    When you click it, it must send a broadcast named (appName)Open (Replace {appName} with the name of your app.)
    each type must have 3 states with these EXACT names:
    
             Taskbar  | Desktop
        ------------- | -------------
    taskbar           | desktop
    taskbarMouseHover | desktopMouseHover
    taskbarMouseClick | desktopMouseClick
    
    The ghost square in the MouseHover and MouseClick states must be 1.65625x1.0625 times larger than the icon itself.
    For examples, go to turbowarp.org and load the catos11.sb3 file in the editor.
    
    
A background sprite
     It can be a GIF, multiple images, or just 1 image. Just make sure they are all COSTUMES not SPRITES.
     To use multiple backgrounds, use code to switch costumes.
     It must ALWAYS follow the dragBar sprite
     
A "dragbar" sprite
     It must be widthOfAppx21 in size
     It must be set to draggable

a "dragExit" sprite
     It must have 3 states: X, XMouseHover, and XMouseClick
     It must ALWAYS follow the dragBar sprite
     When you click it, it must send a broadcast named {appName}Close (Replace {appName} with the name of your app.)
       
It can have other sprites, like buttons, a loading sprite, etc.
       
       
