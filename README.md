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
MeterTotalTime=MeterLength
MeterCurrentTime=MeterPosition
```

- Copy these measures from GPMDPTest.ini:
```
[MeasureLuaScript]
Measure=Script
ScriptFile="#CURRENTPATH#GPMDPJson.lua"
; Change this path to your playback-information, this should be the same location except with a different user ofcourse. So "Maart" should be your username and for most people it's probably drive C
FileToRead="D:\Users\maart\AppData\Roaming\Google Play Music Desktop Player\json_store\playback.json"
JSONParser="#CURRENTPATH#JSON.lua"

[MeasureImageDownload]
Measure=Plugin
Plugin=WebParser
url=#CoverUrl#
Download=1
DynamicVariables=1
DownloadFile=image1.jpg

[MeasureCalcProgress]
Measure=Calc
Formula= #Length#
DynamicVariables=1
```
- Use MeasureImageDownload as the measure for your album cover
- Use MeasureCalcProgress as the measure for the time bar or roundline
