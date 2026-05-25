# Carefully read these setup instructions

---

## For a self updating instance:
  1. Install Prism Launcher from prismlauncher.org and log in with your Minecraft account
  2. Create a new instance with Minecraft 1.21.1 and NeoForge 21.1.230
  3. Download packwiz-installer-bootstrap.jar from [packwiz jar](github.com/packwiz/packwiz-installer-bootstrap/releases),
     place it in your instance folder (right-click instance → Open Folder)
  4. In Prism, right-click the instance → Edit → Custom Commands → check the pre-launch box and paste: 
	    ```"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://github.com/Sofmethod/Modrinth-modpack/new/main/pack.toml```

---

## Setting up the local repository (if you'd like to add mods, refer to the next section)
  1. Install GitHub Desktop from [github desktop](desktop.github.com) and log in with your GitHub account
  2. Go to the repo on github.com, click the green Code button and copy the URL
  3. In GitHub Desktop go to File → Clone Repository → URL, paste the URL and choose where to save it on your PC, then click Clone
  4. Install Go from [go install](golang.org/dl)
  5. Open a terminal in the repo folder (in GitHub Desktop go to Repository → Open in Terminal) and run: ```go install github.com/packwiz/packwiz@latest```

---
## Adding mods, configs, datapacks
  Make sure you followed the steps to set up your local repository
  
***READ THIS*** MAIN RULES:
  ***NEVER COMMIT OR PUSH TO MAIN*** always put it in a branch and make a pull request

## Step before you add anything
  1. In Github Desktop, at the top click *current branch*
  2. Click *new branch* name it something descriptive
     # After you've made your changes:
     1. Press *commit* at the bottom left
     2. Click *publish branch*
     3. Go to the repo on github.com and *Compare & pull request*, describe your changes
     4. It will be viewed and merged to main, after that everyone's modpack instance updates on launch.

# Adding mods from Modrinth or Curseforge
  Open terminal, navigate to your local tepository (cd C:examplefolder\yourrepository, then use this command: ```packwiz modrinth/curseforge add <modname>```

# Updating a mod
  Refer to Open terminal... above, then enter this command: ```packwiz update <modname>```

#Updating or adding a config/datapack/resourcepack
   Navigate to the overwrite\ folder inside your local repository, paste your file in its dedicated folder
   Alternatively if you adjusted a file inside of your local repository you only have to follow the main rule.
  
