# MacOS Tips

- **Tile window in a direction**
    - `Fn + Control + Arrow Key`
- **Return a window tile to its previous size**
    - `Fn + Control + R`
- **Right click with keyboard shortcut**
    - `Control + Enter`

<br>

- **Page up and down on mac os is Fn + Up Arrow or Fn + Down Arrow**

<br>

- **How to move the pointer to where the keyboard focus is:**

  - `Tab + C`
    - **_Must have full keyboard access on_**

<br>

- **Search for items:**

  - `Tab + f`

- **How to delete to the beginning of a line in mac os:**

  - `cmd + delete`

- **How to delete to the beginning of a word:**

  - `option + delete`

- **How to delete from the cursor to the end of a line:**

  - `ctrl + k`

- **How to delete to the end of a word:**

  - `alt + fn + delete`

- **How to jump to the beginning of a line in a search bar:**

  - `cmd + left arrow`

- **How to jump to the end of a line in a search bar:**

  - `cmd + right arrow`

- **How to move to the end a word in a search bar in mac os:**

  - `option + right arrow`

- **How to move to the beginning of a word in a search bar in mac os:**

  - `option + left arrow`

- **How to move to the end of a word in a search bar in mac os:**

  - `option + right arrow`

- **How to move to the end of a all text:**

  - `cmd + down arrow`

- **How to move to the end of a all text:**

  - `cmd + up arrow`

- **Select text to beginning of a line:**

  - `shift + cmd + left arrow`

- **Select text to the end of the line:**

  - `shift + cmd + right arrow`

- **Select text to the the beginning of the word:**

  - `shift + option + left arrow`

- **Select text to the the end of the word:**

  - `shift + option + right arrow`

- **Select text to the the end of all the text:**

  - `shift + cmd + down arrow`

- **Select text to the the beginning of all the text:**

  - `shift + cmd + up arrow`

- **How to highlight the contents of a search bar in mac os:**

  - `cmd + a`

- **How to take a screen shot of a selected area and save it to a file:**

  - `cmd + shift + 4`

- **How to copy a picture of selected area to the clipboard:**

  - `control + shift + cmd + 4`

- **How to to take a picture of screen and save it as a file:**

  - `cmd + shift + 3`

- **How to copy a picture of the screen to the clipboard:**

  - `control + shift + cmd + 3`

- **Screenshot and recording options:**

  - `cmd + shift + 5`

- **Change the default name of your screenshots:**

  - `defaults write com.apple.screencapture name "<name>"`

- **How to change the default file type of screenshots:**

  - `defaults write com.apple.screencapture type <file_type>`
    - **example** `defaults write com.apple.screencapture type jpg`

- **How to change the location of where your screenshots are saved:**

  - `defaults write com.apple.screencapture location <path>`
    - **example:** `defaults write com.apple.screencapture location ~/Desktop/`

- **How to switch between windows:**

  - **_Must have stage manager mode enabled_**
  - **_Then use the following keyboard shortcut to switch between windows:_**
    - **cmd + `**

- **How to fullscreen an app:**

  - `control + cmd + f`

- **How to minimize a window:**

  - `cmd + m`

- **How to close a window:**

  - `cmd + w`

- **How to quickly cycle and switch apps:**

  - `cmd + tab`

- **How to move a window to the left (set a custom keyboard shorcut):**

  - `shift + cmd + left arrow key`

- **How to move a window to the right (set a custom keyboard shorcut):**

  - `shift + cmd + right arrow key`

- **How to move forward when navigating ui elements:**

  - **_First you must enable "Full keyboard access" from the accessibility shortcuts._**

    - `Press option + cmd + F5 to open accessibility shortcuts`

  - **Move forward:**

    - `Tab`

  - **Move backwards:**

    - `Shift + Tab`

  - **To select:**
    - `Spacebar`

- **How to open spotlight search:**

  - `cmd + space`

- **How to open mission control:**

  - `control + up arrow key`

- **How to navigate between windows when mission control is activated:**

  - `control + left arrow key or control + right arrow key`

- **How to open up additional workspaces:** -**_Open mission control_**

  - `Press the "+" ui button to add additional workspaces`

  - **How to move between workspaces:**
    `control + left arrow key or control + right arrow key`

- **How to move focus to menu bar (menu at top left side):**

  - `control + F2`

- **How to toggle "keyboard access" on and off**

  - `control + F1`

- **How to move focus to the window toolbar:**

  - `control + F5`

- **How to move focus the floating window:**

  - `control + F6`

- **How to move focus to status menus:**

  - `control + F8`

- **How to open Control Center:**

  - `Fn + C`

- **How to show desktop:**
  - `F11`

<br>

# Dock shortcuts

- **Jump to the Dock:**

  - `Fn + a`

- **How to hide or show the Dock:**

  - `options + cmd + d`

- **How to access the dock:**

  - `control + F3`

- **Move through the Dock:**

  - `left arrow and right arrow`

- **Open the Dock app's menu:**

  - `up arrow key`

- **Open the Dock app's force quite menu:**

  - `options + up arrow key`

- **Jump to a specific app in the Dock (first letter of app name):**
- `letter keys`

- **Move the selected app to a different spot in the Dock:**

  - `Hold the options key and use the left and right arrow keys`

- **How to scroll iterm2 terminal:**

  - `cmd + up arrow key or cmd + down arrow key`

- **How to scroll iterm2 terminal faster:**

  - `fn + cmd + up arrow key or fn + cmd + down arrow key`

- **How to clear terminal:**

  - `ctrl + l`

- How to pause Full Keyboard Access:

  - `ctrl + option + cmd + p`

- Shortcut keys to access developer tools:

  - `cmd + option + i`

- **Open the Application Chooser:**

  - `Tab + a`

- **Open the Window Chooser:**
  - `Tab + w`

<br>

# Terminal Commands

- **How to view all services on macos:**

  - `sudo launchctl list`

- **How to view all homebrew services on mac:**
- $ `brew services list`

- **To keep your workstation awake and it from sleeping while the terminal is open run the following command in your terminal:**

  - $ `caffeinate`

- **To pipe any command output to your clipboard pipe command output to the following command:**

  - $ `pbcopy`

- **To paste from clipboard without formating use the following keyboard shortcut:**

  - `cmd + options + shift + v`

- **MacOS saves download history into a sqlite database... to view download history from the sqlite database use the following command:**

  - $ `sqlite3 ~/Library/Preferences/com.apple.LaunchServices.QuarantineEventsV* 'select LSQuarantineDataURLString from LSQuarantineEvent'`

- **How to see all homebrew services and if they are running:**
  - $ `brew services list`

<br>

# Finder Shortcuts

- **Duplicate the selected files:**

  - `cmd + d`

- **Create a new folder:**

  - `shift + cmd + n`

- **Create a new Smart Folder:**

  - `option + cmd + n`

- **Get the Get Info window for a selected file:**

  - `cmd + i`

- **(1) When an alias is selected in the Finder: show the original file for the selected alias. (2) In some apps, such as Calendar or Safari, refresh or reload the page. (3) In Software Update, check for software updates again:**

  - `cmd + r`

- **Move the selected item to the trash:**

  - `cmd + delete`

- **Empty the Trash:**

  - `shift + cmd + delete`

- **Empty the trash without confirmation dialog:**

  - `option + shift + cmd + delete`

- **Show or hide the tab bar in Finder windows:**

  - `shift + cmd + t`

- **Show or hide the Preview pane in Finder windows:**

  - `shift + cmd + p`

- **Move the files in the Clipboard from their original location to the current location:**

  - `option + cmd + v`

- **Use Quick Look to preview the selected files:**

  - `cmd + y`

- **View a Quick Look slideshow of the selected files:**

  - `option + cmd + y`

- **To copy path name of file:**

  - `option + right click mouse -> select copy as path name" from the menu`

- **Go to the previous folder:**

  - `cmd + [`

- **Go to the next folder:**

  - `cmd + ]`

- **Make an alias of the selected item:**

  - `ctrl + cmd + a`

- **Add the selected item to the Dock:**

  - `ctrl + shift + cmd + t`

- **Add the selected item to the sidebar:**

  - `ctrl + cmd + t`

- **Hide or show the path bar in Finder windows:**

  - `option + cmd + p`

- **Hide or show the Sidebar in Finder windows:**

  - `options + cmd + s`

- **Hide or show the status bar in Finder windows:**

  - `cmd + /`

- **Show View Options:**

  - `cmd + j`

- **Eject the selected disk or volume:**

  - `cmd + e`

- **Open a new Finder window:**

  - `cmd + n`

- **View the items in the Finder window as icons:**

  - `cmd + 1`

- **View the items in a Finder window as a list:**

  - `cmd + 2`

- **View the items in a Finder window in columns:**

  - `cmd + 3`

- **View the items in a Finder window in a gallery:**

  - `cmd + 4`

- **Open the folder that contains the current folder:**

  - `cmd + up arrow`

- **Open the folder tht contains the current folder in a new window:**

  - `cmd + ctrl + up arrow`

- **Open the selected item:**

  - `cmd + down arrow`

- **Open the selected folder. This works only when in list view:**

  - `right arrow`

- **Close the selected folder. This works only when in list view:**

  - `left arrow`

- **Open the Home folder of the current macOS user account:**

  - `shift + cmd + h`

- **Open the documents folder:**

  - `shift + cmd + o`

- **Open the Computer window:**

  - `shift + cmd + c`

- **Open icloud drive:**

  - `shift + cmd + i`

- **Open the downloads folder:**

  - `option + cmd + l`

- **Open a Go to Folder window:**

  - `shift + cmd + g`

- **Open the desktop folder:**
  - `shift + cmd + d`

<br>

# Apple Notes Keyboard Shortcuts

- **How to search through all notes:**

  - `cmd + option + f`

- **Create a new note:**

  - `cmd + n`

- **Duplicate note:**

  - `cmd + d`

- **Create a new folder:**

  - `Shift + cmd + n`

- **Show notes in a list:**

  - `cmd + 1`

- **Show notes in a gallery view:**

  - `cmd + 2`

- **Show attachments:**
  - `cmd + 3`

# Edit Notes

- **Attach a file:**

  - `Shift + cmd + a`

- **Create a link to a webpage:**

  - `cmd + k`

- **Insert a table:**

  - `Option + Cmd + t`

- **Apply Title format:**

  - `Shift + cmd + t`

- **Apply Heading format:**

  - `Shift + cmd + h`

- **Apply Subheading format:**

  - `Shift + cmd + j`

- **Apply Body format:**

  - `Shift + cmd + b`

- **Apply Monospaced format:**

  - `Shift + Command + M`

- **Apply Bulleted List format:**

  - `Shift + Cmd + 7`

- **Apply Dashed List format:**

  - `Shift + cmd + 8`

- **Apply Numbered List format:**

  - `Shift + cmd + 9`

- **Apply Checklist format:**

  - `Shift + cmd + l`

- **Apply Block Quote format:**

  - `Command + '`

- **Increase font size:**

  - `cmd + +`

- **Decrease font size:**
  - `cmd + -`

# Mouse tips

- **_You can double click the corner of a window to full screen it_**

# Fonts & Emojis

- **How to Access Emojis and Character Viewer**

  - Open emoji pane:

    - cmd + ctrl + spacebar

      - **Then click button at top right corners**
        - to type a superscript character type superscript in the searchbar

[Link to apple guide on keyboard shortcuts & gestures.](https://support.apple.com/guide/notes/keyboard-shortcuts-and-gestures-apd46c25187e/mac)

# Freeform Tips

- **How to make selected text bold:**

  - `Cmd + b`

- **How to make selected text italicized:**

  - `Cmd + I`

- **How to underline selected text:**

  - `Cmd + u`

- **Show the Colors Window:**

- **Group multiple items to become one unit:**

  - `Option + cmd + g`

- **Ungroup items:**
  - `Option + shift + cmd + g`

<br>

# How to view macOS Keyboard ansci escape sequences

- **_Use the following command_**
  - $ `od`
    - **Type keyboard key**

<br>

# MacOS SIP

- [Link to video](https://book.hacktricks.xyz/macos-hardening/macos-security-and-privilege-escalation/macos-security-protections/macos-sip***)

<br>

# MacOS Automator

- You can use automator **quick actions** to run an apple script that will execute an executable for you.

  - You can then bind a keyboard shortcut to this quick action by navigating to **keyboard shortcuts** in **System Settings** finding your quick action under the **Services** section.
  - **_Quick Actions_** are stored in `~/Library/Services`.

- [Link to video](https://www.youtube.com/watch?v=toqgOjcvZvI)

<br>

# Scheduling Timed Jobs on MacOS

- You can use **_cronjobs_** like most unix operating systems but MacOS prefers you use **_launchd_**.

- `man launchd`, `man lunchd.plist`, `man plist` - **_help pages_**

- [Apple Developer Docs:](https://developer.apple.com/library/archive/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/ScheduledJobs.html)

<br>

# Manual Pages

- The following command will search for the man pages of any program you provide and detail the paths it uses to look for them and config file it uses.
  - $ `man -d alacritty`

<br>

# Troubleshooting

- **_If the keyboard shortcut tab + cmd doesn't open up application windows its because stage manager is not enabled._**

- **_If stage manager is not enabled and you minimize a window... to open it back up you must do so from the dock... either by clicking on its icon in the dock or selecting the instance of the application from the options menu of the application icon on the dock._**

- **_If full keyboard access has to be installed from the accessibilty shortcuts menu for tab c shortcut to make mouse follow focus to work_**

- **_Full keyboard access mode might conflict with rectangle pro_**
