# functions

stop_speech




This function will stop any information that is currently being spoken by the screen reader.


# void stop_speech()

## Parameters

None

## Return value

None

## Remarks

This function will stop any information that is currently being spoken by the screen reader.

## Example

```
// Speak some text and stop it after 3 seconds.
void main()
{
speak("Hi. I'm now speaking for 3 seconds, before which the speech is stopped. I hope everything is fine, and take care of yourself! have a nice day!");
wait(3000);
stop_speech();
}
```
