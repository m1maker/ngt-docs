# NGT Global Constants
These are properties that can be used globally, meaning from anywhere.

## Script properties

| Property | Description | Type |
|---|---|---|
| SCRIPT_COMPILED | Returns true if the script is compiled into executable, false otherwise. | bool |

## OS properties

| Property | Description | Type |
|---|---|---|
| cpu_count | Returns the number of threads your OS has. | int |
| system_ram | Returns the ram of your operating system, in MB. | int |
| platform | Returns the name of your operating system, eg Windows. | string |
| window_active | Returns true or false whether the current window is active, meaning if it has keyboard set focus. | bool |
| window_title | Sets the title of the current window. | string |
| window_closeable | Sets whether the window can be closed using the companation of ALT+F4. | bool |
| window_fullscreen | Sets whether the window should be in full screen. | bool |

## General properties

| Property | Description | Type |
|---|---|---|
| sound_storage | Sets or gets the sound storage. | string |
| sound_pack | Sets or gets the sound pack. | pack@ |
| master_volume | Sets or gets the master main volume of all sounds plaied in the script. | float |

## Screen reader properties

| Property | Description | Type |
|---|---|---|
| screen_reader_interrupt | Sets or gets the interrupting of screen reader. | bool |