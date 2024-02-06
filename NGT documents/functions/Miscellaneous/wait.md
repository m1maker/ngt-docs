# functions

wait




This function pauses the entire script for a certain number of milliseconds.


# void wait(int time)

## Parameters

variable| description
---|---
time | The number of milliseconds to wait. This must not be less than 0.

## Return value

none

## Remarks

This function completely interrupts the script for the specified amount of time. This includes all real-time activities such as checking timers, keyboard input, etc. It is not advisable to wait for a long time in situations where the program needs to be responsive. However, waiting for about 5 milliseconds in your main game loop as well as other loops that run for a long time is highly recommended, as it reduces the CPU usage of your program enormously without affecting its speed. If you fail to do this, your game will consume 100% of the CPU at all times.

## Example

```
// Display a message, wait for two seconds, and then display another one.
void main()
{
alert("Waiting", "About to wait for two seconds.");
wait(2000);
alert("Thanks", "Thanks for waiting for me. Goodbye dear.");
}
```
