# TestRainmeterGPMDP

Just a quick test to use the JSON file from Google Play Music Desktop Player from MarshallOfSound:

https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-

To use this in your own skins:

- Copy GPMDPJson.lua and JSON.lua to your directory
- Copy these variables from GPMDPTest.ini and change the values to the name of your skin: 
```
MeterTitleName=MeterTitle
MeterArtistName=MeterArtist
MeterAlbumName=MeterAlbum
```
- Copy these measures from GPMDPTest.ini:
```
[MeasureLuaScript]
Measure=Script
ScriptFile="#CURRENTPATH#GPMDPJson.lua"

; Change this path to your playback-information, this should be the same location except with a different user ofcourse. So "Maart" should be your username
FileToRead="D:\Users\maart\AppData\Roaming\GPMDP\playback-information.json"
JSONParser="#CURRENTPATH#JSON.lua"
UpdateDivider=1

[MeasureImageDownload]
Measure=Plugin
Plugin=WebParser
url=#CoverUrl#
Download=1
DynamicVariables=1
DownloadFile=image1.jpg
```
