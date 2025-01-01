# Application Behavior

## Window

To manage the application window effectively, utilize the show_window function. Setting the enable_renderer flag to true is crucial if your application requires rendering graphics or supports input devices like joysticks or gamepads. If these features are not used, you may set the flag to false, allowing the window to handle events in the background without being tied to the rendering loop.

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

## Background Tasks

For applications that require concurrent processing, consider implementing a dedicated thread for background tasks. This can help maintain responsiveness in the main application loop while performing resource-intensive operations such as loading assets or processing data.

## Exiting

When a quit request event is received from the user, the loop is terminated gracefully. This is the preferred method for exiting the program, as it allows automatic control objects to call their destructors and free resources properly. Avoid overusing the exit function unless there is a compelling reason to abort execution. If you need to return a return code, declare main as int main.
