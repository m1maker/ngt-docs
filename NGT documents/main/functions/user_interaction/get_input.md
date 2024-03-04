# functions

get_input




This function traps any characters that are sent to the game window.


# string get_input()

## Parameters

None

## Return value

A string containing any characters that have been pressed inside the game window since the last call.

## Remarks

This function only traps printable characters such as letters, numbers, punctuation, symbols, etc. All other keys such as tab, control, escape, and enter are ignored.

## Example

```
// Give the user eight seconds to do some typing and display the result.
timer wait_time;

void main()
{
alert("Waiting", "You have eight seconds to type some text.");
show_game_window("Typing test");
while(true)
{
update_game_window();
if(wait_time.elapsed_second() >= 8000)
{
wait_time.pause();
alert("Thanks", "Thanks for waiting for me. You typed the following characters within 8 seconds: " + get_input() + ". Goodbye.");
exit();
}
}
}
```
