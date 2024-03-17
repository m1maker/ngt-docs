# custom_menu

custom_menu object


This method adds the slider to the menu.

# bool add_slider(string i, string ref, double sdindex, double sdmin, double sdmax)

## Parameters

Variable| Description
---|---
i | The name of the slider.
ref | The reference of the slider to access.
sdindex | The position that the slider will be focused. 0 is default.
sdmin | The minimum possible value of the slider. 0 is default.
sdmax | The maximum possible value of the slider. 100 is default.

## Return Value

True on success, false on failure.

## Remarks

A slider can be changed its index value with left and right arrow keys. Combine with control will change by 10 percent.
