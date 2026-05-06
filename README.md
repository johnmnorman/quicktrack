# quicktrack
A python helper for using opentrack with Proton games on Linux

Quicktrack is a python script with an associated config file, designed to use protontricks-launch to execute opentrack in the same proton prefix as the game you're wanting to use headtracking in. It also makes sure that a critically-necessary dll is available in that prefix; this icuuc.dll is absent by default, which causes the 2026.1.0 version of opentrack.exe to crash.

The python code should run out of the box if you have python3. No dependencies or venv stuff needed. The script expects you to have protontricks-launch installed and visible in your $PATH. Installing protontricks via your distro's package manager should be sufficient to satisfy this requirement.

Out of the box, this supports il-2 stalingrad, Falcon BMS, Project Wingman, and Nuclear Option. The helper script is easily reconfigurable - you can add your own games. All you need to do to is to make sure the appids.cfg points to your steamapps folder (~/.steam/steam/steamapps by default) and add your game following the convention in the config file. You can find a game's appid by going to Steam and right-clicking the title in your library. Then go to Properties->Updates and look at the bottom of the window. The App ID there is the number you want.
