# Carefully read these setup instructions


## For a self updating instance:
  1. Install Prism Launcher from prismlauncher.org and log in with your Minecraft account.
  2. Create a new instance with Minecraft 1.21.1 and NeoForge 21.1.230.
  3. Download packwiz-installer-bootstrap.jar from github.com/packwiz/packwiz-installer-bootstrap/releases,
     place it in your instances minecraft folder (right-click instance → Open Folder).
  4. In Prism, right-click the instance → Edit → Custom Commands → check the pre-launch box and paste: 
	    ```"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Sofmethod/Modrinth-modpack/main/pack.toml```
For more performance, add this to your java arguments in your instance settings: ```-XX:+UseZGC -XX:+UnlockExperimentalVMOptions -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xms512m -Xmx16384m```

## Setting up the local repository (if you'd like to add mods, refer to the next section)
  1. Install GitHub Desktop from desktop.github.com and log in with your GitHub account.
  2. Go to the repo on github.com, click the green Code button and copy the URL.
  3. In GitHub Desktop go to File → Clone Repository → URL, paste the URL and choose where to save it on your PC, then click Clone.
  4. Install Go from golang.org/dl.
  5. Open a terminal and run: ```go install github.com/packwiz/packwiz@latest```


## Adding mods, configs, datapacks
  Make sure you followed the steps to set up your local repository.
  
***READ THIS*** MAIN RULES:
  ***NEVER COMMIT OR PUSH TO MAIN*** always put it in a branch and make a pull request.

## Step before you add anything
  1. In Github Desktop, at the top click *current branch*.
  2. Click *new branch*, name it something descriptive.
     ## After you've made your changes:
     1. Press *commit* at the bottom left.
     2. Click *publish branch*.
     3. Go to the repo on github.com and *Compare & pull request*, describe your changes.
     4. It will be viewed and merged to main, after that everyone's modpack instance updates on launch.

### Adding mods from Modrinth or Curseforge
  Open terminal, navigate to your local repository (cd C:examplefolder\yourrepository, then use this command: ```packwiz modrinth/curseforge add <modname>```

### Updating a mod
  Refer to Open terminal... above, then enter this command: ```packwiz update <modname>```

### Updating or adding a config/datapack/resourcepack
   Navigate to the instance folder inside your local repository, paste your file in its dedicated folder.
   WARNING! Open your repo in the terminal and run ```packwiz refresh``` otherwise it will not register your change.
  
