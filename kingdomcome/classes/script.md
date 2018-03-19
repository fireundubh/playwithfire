<!-- TITLE: Script -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Script
## Methods

Method | Return Type | Description
--- | --- | ---
`LoadScript(string: scriptName)` | int | Loads the script
`ReloadScripts()` | int | Reloads all the scripts
`ReloadScript()` | int | Reload the script
`ReloadEntityScript(string: className)` | int | Reloads the specified entity script
`UnloadScript()` | int | Unloads the script
`DumpLoadedScripts()` | int | Dumps all the loaded scripts
`SetTimer(nMilliseconds, luaFunction, [, userData, [, bUpdateDuringPause]])` | timerId | Set a general script timer, when timer expires will call back a specified lua function
`SetTimerForFunction(nMilliseconds, luaFunction [, userData [, bUpdateDuringPause]])` | timerId | Set a general script timer, when timer expires will call back a specified lua function
`KillTimer( nTimerId )` | int | Stops a timer set by the SetTimer function.