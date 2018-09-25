# darkmode

Set macOS dark mode and Alfred dark theme at sunset.

This shell script pulls sunrise and sunset data from the Yahoo weather API and automates the setting up of two user launch agents for sunrise and sunset, which then take over running the script thereafter. If your mac was asleep/off during the solar times, launchd will run the script when you're next logged in!

##### High Sierra and below
![HighSierra](resources/highsierra.gif "High Sierra dark menu bar and dock")

##### Mojave
![Mojave](resources/mojave.gif "Mojave Dark Mode")

### Usage
```
$ ./darkmode.sh
```
 
### Notes

Compatible with macOS Mojave Dark Mode. Press OK to the security dialogs to allow control to System Events that appear when first running the script.

This script pulls your location from ipinfo.io. If you would not like the script to gather your location, hard code your location in the solar function in variables 'loc' (city) and 'nat' (nation) e.g. loc=seattle nat=usa

If you have a custom Alfred theme, you can change the name of the theme in the darkMode function. Change the second quote in the osascript commands.

A log file is stored in ~/Library/Logs which logs solar time changes and script errors.

To uninstall: $ ./darkmode.sh /u