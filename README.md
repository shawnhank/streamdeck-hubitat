![Discord](https://img.shields.io/discord/803471871617531904?style=flat-square)
![macOS](https://img.shields.io/badge/macOS-✓-success?logo=apple&style=flat-square&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-✓-success?logo=windows-95&style=flat-square&logoColor=white)
![GitHub all releases](https://img.shields.io/github/downloads/ripnet/streamdeck-hubitat/total?style=flat-square)

# steamdeck-hubitat
[Hubitat](https://hubitat.com/) integration for the [Elgato Stream Deck](https://www.elgato.com/en/gaming/stream-deck)

![](resources/readme/example.png)

# Documentation

## Introduction
This plugin uses the Hubitat's Maker API and websockets to allow Stream Deck to control devices.

## Setup

### Hubitat
Install the [Maker API](https://docs.hubitat.com/index.php?title=Maker_API) app into Hubitat.

Make note of your `API_URL` and your `access_token`. ![](resources/readme/access_token.png)

### Stream Deck
Download the latest release from the [Releases](https://github.com/ripnet/streamdeck-hubitat/releases) page.


## A couple of notes before starting ##

> Note 1: Please refer to the official [Elgato Stream Deck documentation to create your own plugin](https://developer.elgato.com/documentation/stream-deck/sdk/create-your-own-plugin/) if the below doesn't work for you as that will have the latest and greatest information.

> Note 2: The process below was successfully completed on macOS Monterrey 12.0 Beta. The process is similar for Windows systems. Please refer to the Elgato documentation using the link in Note 1 above.

![About This Mac](https://p140.p3.n0.cdn.getcloudapp.com/items/Wnu0WXZ8/ff563859-7adb-4539-ad30-71707bbf5aa5.png?v=ce43c0296642609896ea0db0b57873c7)

> 3 - Be sure you've completely **QUIT** the Stream Deck app before going through the steps below.

**************************************************************************************************************************

## Steps

1 - Download [ripnet's latest streamdeck-hubitat release](https://github.com/ripnet/streamdeck-hubitat/releases)

2 - Unzip/Extract the zip file in whatever directory/folder you downloaded the file (~/Downloads in the screenshot)

  ![Extracted Folder in Downloads Directory](https://p140.p3.n0.cdn.getcloudapp.com/items/2Nulo99l/b4f0c41f-be75-40b2-a820-4a6d9a466f19.png?v=40ceb2e00d1b0d191d04ae5e0fe0864f)

3 - Open a new Finder window (CMD+N) and use the Shift+CMD+G shortcut key to go to this folder:

    `~/Library/Application Support/com.elgato.StreamDeck/Plugins/`

  ![Stream Deck Plugins Directory](https://p140.p3.n0.cdn.getcloudapp.com/items/Wnu0WX8b/70aa2586-b24f-44ca-97f6-314a0f3ab93f.png?v=179135f0eb35ccaf8c96c1e3ae71cbdc)

> Note the full path to the Stream Deck Plugins Directory

  ![Path to the Stream Deck Plugins Directory](https://p140.p3.n0.cdn.getcloudapp.com/items/NQuY9BA7/b3b6dabc-4b68-4a54-9747-cdde8b4b0361.png?v=26f19b00bd6262b06690471715460012)

5 - Back in the other Finder window (Downloads) drag and drop the extracted zip folder and all its contents to the Stream Deck Plugins Finder Window. Rename the folder to whatever you want. **Be sure to include the .sdPlugin extension**

  ![GIF - Moving & Renaming the streamdeck-hubitat-main folder](https://p140.p3.n0.cdn.getcloudapp.com/items/Wnu0WX9j/5209c18f-7c7f-43fb-8d31-7d398cd2e37c.gif?v=11ff77fb6adc1fc00ea8f61e90fbb152)

> If the embedded GIF doesn't show up here on GitHub, [click on this link to view it](https://share.jillandshawn.com/Wnu0WX9j)

6 - Open the Stream Deck app and you should now see the Hubitat plugin at the bottom of the listed plugins in the right column

  ![Hubitat Plugin is now Installed](https://p140.p3.n0.cdn.getcloudapp.com/items/lluoAOpA/c69cab31-4689-4686-9afe-58896ed22e47.png?v=a4f723200f3d59cad93ca0947e99d760)

7 - Continue on with ripnet's readme starting at the **Available Buttons* section.

#### Available Buttons
There are currently two buttons available
* Toggle Switch - This will toggle the state of a switch from off to on, or on to off.
* Set Switch - This will set the state of a switch to either on or off, regardless of its current state.

Drag an action button to a free button slot. Configure the button with the `API URL` of your hubitat. Paste in your `access_token` from the Maker API.
Click away from the input field and if everything has been setup properly, the list of devices should populate. Select the device you want to control and give it a name.

![](resources/readme/global_settings.png)

## Colors
Gray = No/Unknown Status

Green = Switch On

Red = Switch Off

# Support
Please use GitHub Issues for bugs or feature requests. Join me on my [Discord Server](https://discord.gg/J5tSRCMNbz) if you have any questions.

# License
`streamdeck-hubitat` is licensed under the [MIT License](LICENSE)
