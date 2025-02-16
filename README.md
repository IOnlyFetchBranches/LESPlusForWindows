## What is the Live Enhancement Suite (+)?

The Live Enhancement Suite (+) is a self-managing compiled [AutoHotKey](https://www.autohotkey.com/) script. At its core, is a script that uses the power to AutoHotKey to enhance your Ableton Live experience. 

This is the plus version, which has additional features such as dyamically adjustable sleep timers to suport capatabillity with current and future versions of Live.

## What are all these files?

| Name                                                 | Purpose                                                      |
| ---------------------------------------------------- | ------------------------------------------------------------ |
| `LiveEnhancementSuite.ahk`                           | The heart of LES, this is the actual AutoHotKey script that drives the Live Enhancement Suite |
| `MenuIndex.ahk`                                      | This is menu index file that assists `LiveEnhancementSuite.ahk` |
| `MIndexGen.ahk`                                      | This is the file that used to generate `MenuIndex.ahk`       |
| `menuconfig.ini`                                     | The default menu configuration file that is placed in every new LES install |
| `settings.ini`                                       | The default settings file that is placed in every new LES install |
| `logos\`                                             | The folder that contains all logos for the Live Enhancement Suite (with different colors for developer releases and stable releases) |
| *Everything Else that isn't GitHub related or legal* | Just some little fun                                         |

## Sounds cool, how can I help?

* Read our [Code of Conduct](https://github.com/LiveEnhancementSuite/LESforMacOS/blob/master/CODE_OF_CONDUCT.md) and get started contributing to the Live Enhancement Suite


## How do I build this thing?

### Building with AHK
*Presuming the location of your AutoHotKey install is `C:\Program Files\AutoHotkey\`and you have git installed*

* Clone the repository `git clone https://github.com/LiveEnhancementSuite/LESforWindows`

* Go to the folder of the repository `cd LESforWindows`

* Run the AutoHotKey compiler `"C:\Program Files\AutoHotkey\Compiler\Ahk2Exe.exe" /in LiveEnhancementSuite.ahk /out "Live Enhancement Suite.exe"` 

  ***Sidenote: If you are trying to debug the LiveEnhancementSuite script, you may run it as a normal AutoHotKey script, building is generally reserved for releases***

### Building with CompileAHK GUI
* Clone the repository `git clone https://github.com/LiveEnhancementSuite/LESforWindows`

* Download CompileAHK's GUI here: https://github.com/mercury233/compile-ahk

* Once installed, simply right click the .ahk file and choose "Compile with options"

* Hit the "Compile" button

### Building the installer
* Clone the repository `git clone https://github.com/LiveEnhancementSuite/LESforWindows`

* Download and install the latest version of Inno Setup from https://jrsoftware.org/isinfo.php

* Open the `InnoSetupScript.iss` file with Inno Setup

* Hit Ctrl + F9 to build

## Anything else?

**LES PlusforWindows is released under the MIT License**

Copyright © 2019-2025
Maintined By:
[IOnlyFetchBranches](https://linktr.ee/itscupsy)
Original:
 [Dylan Tallchief](https://twitter.com/dylantallchief) and [Inverted Silence](https://twitter.com/invertedsilence)

