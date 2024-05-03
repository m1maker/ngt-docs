# speedstop

The speedstop object allows you to prevent cheat speed hacking within your programs.

## Methods

Name | Description | Type | Variable Type
---|---|---|---
default_slack_time | The time in which the speed hack should look, usually default is 50. | Property | int
reset | This resets everything, usually you should do this before the loop to run. The optional parameter is user_reset, which reset all. Usually this is true by default, and therefore you don't necessarily need to specify. | Function | void
get_hacking | Checks if the speedhack is detected, usually should run within loops. The time parameter is required, usually 50 is the good one. | Function | bool
hacking | Checks if the speedhack is detected, usually should run within loops. This uses the default_slack_time variable for the time, so it is not necessary to specify the slack time. | Property | bool
enable | Enables the speedhack detection. | Function | void
disable | Disables the speedhack detection. | Function | void
