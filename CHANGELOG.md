# Changelog

## Alpha 3.0

* Added changelog
* Fixed bugs with the save new version command; the project name should now be correct more often!
  added way more scales to the scale menu in the piano roll
* Further improvements to overall system stability and other minor adjustments have been made to enhance the user experience

## Alpha 3.1

* Added support for dividing lines in the plugin menu. Add "--" to the text file to add them anywhere, even in submenus!
* Added temporary drm because dont leak pls
* Further improvements to overall system stability and other minor adjustments have been made to enhance the user experience

## Alpha 3.2

* Fixed a bug with the "save as new version" feature
* Added a new icon
* Added startup a setting in settings.ini
* Fixed a massive issue where the program wouldn't ever properly read settings.ini
* Settings.ini is now loaded dynamically just like menuconfig.ini
* Moved resources to a resources folder for a more organized look
* Further improvements to overall system stability and other minor adjustments have been made to enhance the user experience

## Beta 1.0

* Fixed multi-monitor usage
* Added a new dynamic icon that turns red when you pause it
* Made save new version more stable on laggy projects
* Removed beta testing drm
* Added publisher info so smartscreen no longer trips up hopefully

## Beta 1.1

* Added the ctrl + shift + z redo feature
* Added a prompt at the start that asks you if you want to add the program to startup, rather than just doing it without asking.
* Updated the readme to be more accurate for the release version
* Lowered piano roll scan range so you don't accidentally trigger it with as easily
* Removed a bunch of old junk testing code
* Removed Herobrine

## Beta 1.2

* Further improved multimonitor support (you can now use LES and Ableton as a small window as well)

* Double press 0 to delete (for people who don't have a delete key)

* Added a new envelope mode shortcut "alt + E", use it in the piano roll!

* Superspeedmode! Huge performance gains can be had by disabling the safety delays in autohotkey: it makes the script a breeze to use. (Superspeedmode can be disabled in the settings.ini file)

* Massively overhauled the readme

* Changed default settings
  	- Resettobrowserbookmark is now off by default
  
   - Added the ability to change the piano roll macro, courtesy of my German friends
      Removed a bunch more old junk testing code

* "Generators" are now called "Instruments" in the default menuconfig

* Serum now actually opens serum for most people in the default menuconfig

## Beta 1.3

* Fixed a bug where windowed mode wouldn't be detected properly
* Added the ability to stamp piano roll scales by holding shift+tilde
* You can now instantly create a playlist marker with right shift + L (left shift doesn't work what are you doing that's literally on the opposite side of the keyboard)

## Beta 1.4

* LES now extracts resources from the exe! yay for slick presentation
* Tray:
  * Added a website tray button
  * Added a debug toggle and tray button
* Configure:
  - Added a toggle to disable the double 0 feature
  - Added a manual piano roll mode in case the automatic detection makes the script slow or misbehaves
  - Added a smart icon mode, where the tray icon is automagically hidden if you haven't used ableton live for a while

* Improved stamp usage and added powerchords and octaves to "chords" in the stamp menu.
* Added a secret ""cheat"" menu
* Improved piano roll search accuracy.
* Added a fix for multi-monitor usage on multiple displays with different high dpi scaling settings
* Added the Chromatic "scale" but I don't know why you'd ever use it.

## Beta 1.5 (a.k.a RC-1)

* Added two new absolutereplace keyboard shortcuts. These can be used to paste copy and paste over something else without merging. (just don't use it on tracks)
  * The shortcut for absolute paste is ctrl + alt + v
  * The shortcut for absolute duplicate is ctrl + alt + d 
* There is a toggle in settings.ini for if you want to use the video shortcut.
* Fixed the save as new version command for people with picky clipboards >:(

## Beta 1.6 (a.k.a RC-2)

* Added shortcuts for closing plugin windows more quickly:

* Cleaned up readme
* Added a notification at the start that tells you to double right click
* Changed the way you remove the readme from the plugin menu, it's now part of the default menuconfig, rather than a toggle in the settings.
* Added a video to the settings.ini that explains how to get coordinates for bookmarkx and bookmarky
* Fixed a bug where the tray menu wouldn't show up properly before opening Ableton Live.
* Added a bunch of randomized tray flairs

## Release 1.0/1.0.1

* Changed the version number to release 1.0 (and then 1.0.1 after some hotfixes)
* Added more cheats
* "Reload" is now always in the tray, even when debug is off
* Added two short one tutorial videos to settings.ini
* Added major 9 and minor 9 chords
* Added gypsy scale
* Added "fold" chords to the scale menu

## Release 1.0.2

* Quick first day hotfix that allows you to make midi clips even when you have disableloop turned off (whooops)

## Release 1.1

* Increased maximum pluginmenu item limit to 2000
* Submenus in submenus!!
  	- Add more slashes to go deeper
  	- `//` would be inside the submenu above it starting with `/`
  	- `///` would be inside submenu `//` above it etc.
  	- infinite submenus!
  	- go back one layer with `..`
  	- every submenu needs to have at least one item in it (other than another submenu)

* Added a toggle in settings.ini to remap the right shift + L command to right alt instead
* Fixed a bug where you can't use ampersands in plugin menu titles
* Hold left control to temporarily invert the auto add option (so: if autoadd is on, plugins will not autoadd while holding control and vice versa)
* Changelog.txt now updates automatically
* LES now asks you to replace the settings.ini file with the new default automatically when it's out of date.
* Fixed a bug where the marker shortcut wouldn't work properly in Live 9
* You can now quickly and safely view automation by clicking a knob while holding the pianoroll macro (tilde `)

	- you can also add the clicked knob to a new automation lane if you hold down shift as well.
	- pianorollmacro + left click resets the knob to default! so be careful not to get the two mixed up :)
Added a check adn a warning for when you're running Ableton Live as an Administrator.

## Release 1.2

*Didn't think there was going to be another massive content update to LES, yet here we are.*

- Mac version release - LES has been rewritten from scratch in LUA and hammerspoon so it can be used on MacOS.
- Cross platform menuconfig.ini!
- Dynamic reloads! Set dynamicreload to 1 in settings.ini and now you never have to worry about reloading ever again!
- Reorganized documentation in the ini files
- Manuals! LES is actually properly documented now...
- Reorganized the scale menu
- Added new scales from the Ableton Push 2 library that were previously missing.
  	- Super Locrian
  	  	- Bhairav
  	  	- Hungarian Minor
  	  	- Minor Gypsy
  	  	- Traditional Japanese scales: Insen, Hirajoshi, Iwato, Kumoi
  	  	- Pelog
  	   - Spanish
* Project time tracker! Les will now track how much time you spend on a project. To check out how much time you've spent, simple click "Project Time" in the tray.
  	  	- The project time tracker only clocks your time when you're actively using Live. Time spent browsing reddit in your browser is not going to add up to the talley :)
   - Though, if you want the timer to cut you some slack, you can disable "Strict Time" in the tray.
    	  	- Rewrite of the settings.ini parser. It's now faster and less prone to telling you to reset randomly
            	     - Fixed a bug where holding shift while middle clicking would block all keyboard input until restart
     - Fixed a bug where LES would click on a random spot
     - Fixed a bug where the changelog wouldn't properly update
     - Fixed a bug where divider lines would duplicate
   - Massively improved performance on the Cmd + Alt + S shortcut, don't blink!
    	  	- Two new shortcuts  (just don't use these on groups!):
            	    	  	- Press Alt + X while hovering over a track (or multiple selected tracks) to clear its playlist contents.
         
  - Press Alt + C while hovering over a track to recolour the track's clips.

## Release 1.2.1

*More options is always better!*

### Windows

* The plugin menu should now ALWAYS adds items properly, even if you're in a huge project and your computer is being unresponsive and slow.
* The show automation lanes shortcut now also works even if you're using Live in different languages.
  Added the ability to disable the Ctrl + W command.

### macOS

* Added the ability to disable the absolute duplicate commands.
* Added the ability to disable the Ctrl + W command.
* Made the piano roll macro error much more friendly looking (with added instructions!).
* The show automation lanes shortcut now also works even if you're using Live in different languages.

## Release 1.2.2

### Windows

* Improved 10.1 compatibility
* Slightly better menu performance since 1.2.2
* You can now close VST3 container windows with Ctrl + W (and Ctrl + Alt + W)
* Clear track (Alt + X) now works on all languages
* Save as new version (Ctrl + Alt + S) now works on all languages again

### macOS

* Improved 10.1 compatibility
* Clear track (Option + X) now works on all languages
* Save as new version (Cmd + Alt + S) now works on all languages
* Improved absolute duplicate (Cmd + Alt + S and Cmd + Alt + D) performance and reliability
* Both of these absolute duplicate commands now work on all langages
* Place track marker (Alt + L) now works on all languages
* Added a fallback shortcut for opening the plugin menu (Cmd + Shift + H)

## Release 1.3

## Windows

* Fixed middle click to pan on logitech office mice, including all mice in the MX master series.
  the search query is now always properly cleared, even when loading large vsts; without using the overly complicated bookmark feature.
* The "strict time" setting is now stored across sessions
* LES now warns you when users when it is executed from within the temp folder
* Piano roll detection should now misdetect slightly less
* Added Buplicate!
  * Use Ctrl + B to duplicate something 7 times! Press Ctrl + B again on the same element duplicate again 8 times!
  * Quickly duplicate an initial single clip in blocks of Eight
  * It's more useful than you'd think

* It's time for VST specific shortcuts!
  * Xfer Serum:
    	- use the 1,2,3 and 4 key to switch tabs between osc, fx, matrix and global respectively.
  * Fabfilter Pro Q 3 (vst2, or vst3 without custom resizing):
     - For some reason Ableton Live doesn't properly communicate undo's to pro Q. This macro fixes undo and redo actions inside the plugin by remapping the undo and redo shortcuts to click the buttons at the top.
     - Since I'm not a magician, the undos and redos will behave jank as usual when the plugin window is unfocussed.
  * Kick 2
     * The same thing as pro-q, except for Kick 2

  * Sylenth1
    	- use the 1 and 2 keys to switch between A and B tabs. (Although it's a toggle so you can also just hit 1 constantly)
  * Massive
     * Use keys 1 through 5 to mute and unmute oscillators 1 through 5 (this includes PM/RM and noise)
  * Phase Plant (Beta):
    * These shortcuts are disabled and will not work unless a cheat is entered. 
      *There is a problem with them that I cannot figure out how to fix, but I left them in in case someone wants to play around with them.*
    * If you want to access the Phaseplant shortcuts, enable debug mode in the settings. Then, spam press hit both shift keys at once while in ableton live to open the cheat menu.
      Enter "kilohearts" to enable the shortcuts.
      * Use Alt + A to add an analog oscillator
      * Use Alt + N to add a noise oscillator
      * Use Alt + S to add a sample oscillator
      * Use Alt + W to add a wavetable oscillator
      * Use Alt + D to add a distortion oscillator
      * Use Alt + F to add a filter oscillator
      * Use Alt + O to add an output.
      * Use Alt + L to add an LFO

* VST specific shortcuts can be toggled on and off in the settings.
* Ctrl + F1 or the PAUSE key can be used to toggle LES functionality on and off with ease.
  * You can toggle LES off if a VST shortcut is conflicting with something else you want to do

* Added more safety checks to shortcuts so you can't trigger them out of context as much.
* **Added an option to increase scrolling speed, scroll around faster by changing the value in settings.ini**
* Removed "superspeedmode" from the settings. LES has been stable enough for a while to the point that it's no longer nescesary to have a toggle for this.
* Removed the safe automation open shortcut. Changes to the 10.1 context menus cause it to malfunction too often.
* Changed a japanese word in the black midi easter egg joke so it means "death" rather than telling the users to "die"

### macOS

* Fixed unintentional behavior where single character menu items would be cleared
* Added more safety checks to shortcuts so you can't trigger them out of context as much.
* Added a safeguard for if a different type of quote character is used in the menuconfig file
* Removed the safe automation open shortcut. Changes to the 10.1 context menus cause it to malfunction too often.
* Performance improvements to all shortcuts related to mouse movement
* Updated the main build to Hammerspoon 0.9.76, allowing LES to be used on MacOS catalina.
* fixed a bug where hitting "strict time" would add a check the wrong menu item in the menubar menu
  the "strict time" setting is now stored across reloads.
* the bookmark feature now works in windowed mode
* Added Buplicate!
  * Use Cmd + B to duplicate something 7 times! Press Ctrl + B again on the same element duplicate again 8 times!
  * Quickly duplicate an initial single clip in blocks of Eight
  * It's more useful than you'd think
* Cmd + can be used to toggle LES functionality on and off with ease.
  - you can toggle LES off if a VST shortcut is conflicting with something else you want to do
* it's time for VST specific shortcuts!
  * Xfer Serum:
    	- use the 1,2,3 and 4 key to switch tabs between osc, fx, matrix and global respectively.
  * Fabfilter Pro Q 3 (vst2, or vst3 without custom resizing):
     * For some reason Ableton Live doesn't properly communicate undo's to pro Q 3. This macro fixes undo and redo actions inside the plugin by remapping the undo and redo shortcuts to click the buttons at the top.
    * Since I'm not a magician, the undos and redos will behave jank as usual when the plugin window is unfocussed.

  * Kick 2:
    	- The same thing as pro-q, except for Kick 2

  * Sylenth1:
    	- use the 1 and 2 keys to switch between A and B tabs. (Although it's a toggle so you can also just hit 1 constantly)
  * Massive:
    	- Use keys 1 through 5 to mute and unmute oscillators 1 through 5 (this includes PM/RM and noise)
* VST specific shortcuts can be toggled on and off in the settings.
* Cmd + 1 can be used to toggle LES functionality on and off with ease.
* You can toggle LES off if a VST shortcut is conflicting with something else you want to do

## Release 1.3.2

* Depeicated the vst shortcuts bound to the number keys.
* Added a button to install InsertWhere, a M4L companion plugin that changes where plugins are inserted. (Thank you Mat Zo!)
  * Hit the "Install InsertWhere" to extract the plugin.
  * To use InsertWhere, place the plugin on your master channel. It will now change the location where plugins are auto inserted.
  * If the location is set to "right", plugins will be autoinserted to the right of the one you have selected, rather than at the end.
  * Set insertwhere to "end" to mimmick default behavior.
  * Insertwhere's buttons can be keymapped, and the included oscillator can be used to hear which setting it is currently set to, without looking at the UI.	

If you want to use InsertWhere on a Mac, please click [here](https://cdn.discordapp.com/attachments/202817364264222720/805140617289138176/InsertWhere.amxd)

* Attempted to fix a problem where the mouse would get stuck on middle click to pan. Let me know how that *pans* out.
* Fixed a problem where alt+x cleartracks would not work right on the new Live 11 Beta (thank you bmason12149!)
* Implemented a function in settings.ini where you can switch the fucntions of shift + tab and tab around. (thank you bmason12149!)
* Fixed a problem where sometimes user input would get locked up when using Ctrl+Alt+S 
* Added some extra notes to menuconfig.ini
* Added a warning that annoys people into not running LES from within a few protected system directories.
* Improved some phrasing in dialog boxes
* Made the "Save File As" dialog close automatically after deciding to not save an untitled project as a new file

## Release 1.3.3

* Added shortcuts for Freezing (alt + F) and Flattening tracks (alt + shift + F) 
* Small fix for Quick Marker on different live versions
* Removed a tray flair thing that celebrates the 1.2 release since we're on 1.3 by now


## Release 1.4.0

* Now supports Live 12, Rebrand to LES Plus to prevent confusion.
* Include the abillity to change sleep timings on demand in case menu stops functioning 
* Updated Icons and Tray menu 
* Installer Updated
* Donate removed for now, however check FUNDING.yml to support the original devs