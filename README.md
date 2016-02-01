# TestRainmeterGPMDP

Just a quick test to use the JSON file from Google Play Music Desktop Player from MarshallOfSound:

https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-

To use it, just change the value FileToRead in GPMDPTest.ini to the location of your file(probably the same but a different user).

```[MeasureLuaScript]
Measure=Script
ScriptFile="#CURRENTPATH#GPMDPJson.lua"
FileToRead="D:\Users\maart\AppData\Roaming\GPMDP\playback-information.json"
JSONParser="#CURRENTPATH#JSON.lua"
UpdateDivider=1
```

There probably are better ways of doing this but it's been a long time since i've done anything myself in rainmeter and the first time I develop in Lua.
