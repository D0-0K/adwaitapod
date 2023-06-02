# Advanced Operations

## Installing Extra Fonts

[ image of extra fonts ]

While the default language pack only supports Latin characters, through additional language packs users can extend the supported character range of adwaitapod. 

Asian character sets for Simplified Chinese, Korean and Japanese can be installed alongside Cyrillic and extended Unicode characters in the Extra Language pack. Other languages may be supported in the future if requested by users.

To install, download the font pack from the Releases section on Github, extract and then drop the .rockbox folder into your iPod's directory. Merge the folders. On your iPod, you may need to refresh the theme. You can do this by going to the theme selection and re-selecting adwaitapod. 

[ image of larger fonts ]

For users who find the default menu fonts too small, larger fonts can also be added for menus. These are supported by adwaitapod's rounded corner system, and the pack includes files for this. The larger font packs are installed the same way as the extra language pack.

## Installing Extra Wallpapers

[ image of extra wallpapers ]

Downloadable from the Releases section on Github, the Extra Wallpapers Pack has 8 unique Wallpaper styles (including the default 'adwaita' wallpaper). Each Wallpaper comes with a light and dark variant. 

 The pack is downloaded from the Releases section on Github, from there you can pick the Wallpaper style you want from the reference image. Once you decide, go to the corresponding folder. Inside you will find a **wps** folder, copy this into the .rockbox folder in your iPod's directory. If asked, merge and replace any files. Reload the theme and enjoy!

## Alternate While Playing Screen

[ image of the thing ]

 For those seeking a simplified, album-art focused music player, the alternate While Player Screen is for you! This is a seperate WPS file that can be downloaded from the Releases section on Github, merged with the WPS folder in your iPod's .rockbox folder, and selected under the "While Playing Screen" settings in Theme Settings. Only one file is needed as it will automatically detect whether you are using light mode or dark mode.  

### Features

- Simplified Shuffle/Repeat Status: A box element in the bottom left corner will display a single icon at a time for Shuffle or Repeat. 
- Playlist Indicator: Instead of a number-based playlist indicator, forward and backward buttons show if you can go to a previous or next song. 
- Third info line. A third info line shows a songs year as well as other information like genre or file format.

## User Preferences

An innovative new feature in adwaitapod, User Preferences allow users to change elements of adwaitapod to suit their tastes. User Preferences can be accessed from the **Status-/Scrollbar** settings menu in **Theme Settings**. Each page features clear and informative menus that inform users of what the setting changes.

### Album Art Style

[ image of the page ]

 For users who don't like rounded corners on their album art, this settings allow you to turn them off in favour of squared corners. This applies to the Music Player, Mini Player as well as the Radio Player. 

Location: **Settings** > **Theme Settings** > **Status-/Scrollbar** > **Volume Display**

| Option | Preference |
| ----------- | ----------- |
| Graphic | Rounded Album Art |
| Numeric | Squared Album Art | 

### Player Secondary Text Config

[ image of the page ]

 By default, the second line of the Music Player will cycle between an Album's title and the Artist's name. However if you prefer just one of these on their own, this setting lets you set that. This settings applies to the Music Player, Mini Player and Lockscreen notification.

Location: **Settings** > **Theme Settings** > **Status-/Scrollbar** > **Status Bar**

| Option | Preference |
| ----------- | ----------- |
| Off | Album Title and Artist Name |
| Top | Album Title | 
| Bottom | Artist Name | 

### Quickscreen Config

[ image of the page beside EXP QS ]

 Adwaitapod 3.0 has a secondary, experimental Quickscreen that is intended to become the default Quickscreen in the future. Currently, it will display the name of your chosen Quickscreen settings, however it cannot show the output. A proof of concept has been hardcoded to work with a single, specific set of Quickscreen settings. In order to use this experimental Quickscreen, it is important to use these settings.

#### Manually Setting up the Quickscreen

 Quickscreen settings can be selected by long-pressing the select button on the Settings entry you wish to use. Set your Quickscreen settings according to the following table:

| Direction | Setting |
| ----------- | ----------- |
| Top Quickscreen Item | Brightness |
| Bottom Quickscreen Item | Brightness | 
| Left Quickscreen Item | Shuffle |
| Right Quickscreen Item | Repeat | 

#### Automatically Setting up the Quickscreen

On line 54 thru 62 of the adwaitapod .cfg file (found in the **themes** folder) the following can be found:
```
#-- Experimental Custom Quickscreen --#
# graphic: Rockbox Quickscreen. <-- Default
# numeric: Custom Quickscreen.
battery display: graphic
# !!! If ^ set to numeric, remove the following '#' !!! #
#qs top: brightness
#qs bottom: brightness
#qs left: shuffle
#qs right: repeat
``` 
To automatically set the Experimental Quickscreen, remove the '**#**' from the button four lines, and change the '**battery display graphic**' line to read '**battery display: numeric**'. Save the file and reload the theme on your device.

#### User Preference Reference

Location: **Settings** > **Theme Settings** > **Status-/Scrollbar** > **Volume Display**

| Option | Preference |
| ----------- | ----------- |
| Graphic | Rounded Album Art |
| Numeric | Squared Album Art | 

### Smooth Scrolling

```
#-- Smooth Scrolling --#
#scroll speed: 14
#scroll delay: 1500
#scroll step: 1
```

### Permanently Setting User Preferences

Every time adwaitapod is reloaded, your preferences will revert to their default settings. To change this behaviour, and permanently set your preferences, you must modify the config file. 

 This file can be found inside the themes folder of the .rockbox folder in your iPod's directory. Open this file and find the corresponding section for the Preferences you wish to change. The comments should inform you of what changes to make. Once you are finished, save the file and reload the theme on your iPod for everything to take affect.