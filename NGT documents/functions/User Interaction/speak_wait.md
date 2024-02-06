# functions

speak_wait




This function speaks some text using a screen reader which is determined automatically and wait for it to finish.


# void speak_wait(string text, bool stop = true);

## Parameters

variable| description
---|---
text | The text that is to be spoken.
stop | Toggle whether the previously speaking speech should be stopped. (Default: true)

## Return value

None

## Remarks

This function speaks some text using a screen reader which is determined automatically and pause the execution until it is spoken.

Because script execution is paused while the text inside the speak_wait method is being spoken, it cannot be stopped or interrupted.

## Example

```
void main()
{
speak_wait("I am a screen reader");
}
```
