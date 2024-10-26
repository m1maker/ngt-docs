# Application Behavior

## Window

To display a window, use the show_window function. If you plan to utilize rendering, make sure to set the enable_renderer flag to true in show_window; otherwise, no graphics will be displayed.

## Application Loop

Use
```
while (!quit_requested);
```
to create a loop that continues until the user exits the program. To optimize the application's loop and prevent the CPU from being overloaded, consider using
```
wait(5);
```
if background operations need to be performed alongside window management. Alternatively, use
```
wait_event();
```
if your program should completely wait for user events.

Important: It is essential to call one of these functions if rendering is enabled; failing to do so may cause the window to become unresponsive.

You can modify the value of `update_window_freq` (which controls the screen refresh rate in milliseconds) at any time. However, be aware that increasing this frequency may slow down event processing. Use window_present when you have completed all scenes for rendering.

## Exiting

When a quit request event is received from the user, the loop is terminated gracefully. This is the preferred method for exiting the program, as it allows automatic control objects to call their destructors and free resources properly. Avoid overusing the exit function unless there is a compelling reason to terminate the program unexpectedly. If you need to return a return code, declare main as int main.

