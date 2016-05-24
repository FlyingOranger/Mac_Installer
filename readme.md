# Mac Installer

Currently the mac installer is not created, but I've done most of the heavy lifting if you want to help.

### Dependencies
Flying Oranger runs with 

* Java
* Node.js

So it really should be cross platform. 

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
