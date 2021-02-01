![Live Enhancement Suite](https://raw.githubusercontent.com/LiveEnhancementSuite/LESforMacOS/master/Hammerspoon/Images.xcassets/AppIcon.appiconset/icon_256x256.png)

[![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2FLiveEnhancementSuite%2FLESforWindows%2Fbadge%3Fref%3Dmaster&style=flat)](https://actions-badge.atrox.dev/LiveEnhancementSuite/LESforWindows/goto?ref=master)

## What is the Live Enhancement Suite?

The Live Enhancement Suite is a self-managing compiled [AutoHotKey](https://www.autohotkey.com/) script. At its core, is a script that uses the power to AutoHotKey to enhance your Ableton Live experience. 

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
* Dig some pennies from the couch and help fund the development of LES with [PayPal](https://paypal.me/enhancementsuite)

## How do I build this thing?

*Presuming the location of your AutoHotKey install is `C:\Program Files\AutoHotkey\`and you have git installed*

* Clone the repository `git clone https://github.com/LiveEnhancementSuite/LESforWindows`

* Go to the folder of the repository `cd LESforWindows`

* Run the AutoHotKey compiler `"C:\Program Files\AutoHotkey\Compiler\Ahk2Exe.exe" /in LiveEnhancementSuite.ahk /out "Live Enhancement Suite.exe"`

  ***Sidenote: If you are trying to debug the LiveEnhancementSuite script, you may run it as a normal AutoHotKey script, building is generally reserved for releases***

## Anything else?

**LESforWindows is released under the MIT License**

Copyright © 2019-2020 [Dylan Tallchief](https://twitter.com/dylantallchief) and [Inverted Silence](https://twitter.com/invertedsilence)

