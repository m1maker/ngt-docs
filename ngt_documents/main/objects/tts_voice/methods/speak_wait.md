# tts_voice

tts_voice object

This method will speak a given string and will pause execution until the string is spoken.

# bool speak_wait(string text)

## Parameters

variable | description
---|---
text | The text to speak.

## Return value

true on success, false on failure.

## Remarks

Because script execution is paused while the text inside the speak_wait method is being spoken, it cannot be stopped or interrupted.

## Example

```
// Speak some text.
tts_voice speech;
void main()
{
speech.speak_wait("hey, welcome to ngt!");
}
```