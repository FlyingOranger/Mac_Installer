# Mac Installer

Currently the mac installer is not created, but I've done most of the heavy lifting if you want to help.

### As it stands
Currently the program should run on a mac and linux, but it won't work on startup or anything.
If you want to start development or just get it running on your machine, follow these steps:

```
mkdir FLyingOranger
cd FlyingOranger
git clone https://github.com/FlyingOranger/FlyingOranger.git
git clone https://github.com/FlyingOranger/Notification_Apps.git

// download https://github.com/FlyingOranger/JavaGUI/releases/download/test2/JavaGUI.jar 
// place it in the main directory

cd FLyingOranger

// now start it
node .
```

### What needs to be done
There are three main things that have to be created:

#### Installer
This will 

1. create the directory FlyingOranger in the correct appdata directory
2. Download a local version of node.js from https://nodejs.org/en/download/
3. If java doensn't exist, download java using the dljava.js script (needs to be modified slightly to download from [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)
4. Create any startmenu items 
4. call `node start install` ( we need to modify dlapp.js to support unzipping on mac I think )

#### Flying Oranger Modifications
We need to modify FlyingOranger/lib/startupManager.js to register `node start` to run on startup (depending on what the user wants)

#### Uninstall
Self explainatory, remove all files and exit. 
Need to call `node start uninstall` to kill the current running process and then remove it from the systems startup


#### Contact

Feel free to contact me if you're interested in helping, either message me on reddit (Jarofhearts) or open an issue or something.
