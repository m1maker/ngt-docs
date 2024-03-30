# tts_voice

tts_voice object

This method will speak a given string, interrupting all other queued strings, and will pause execution until the string is spoken.

# bool speak_interrupt_wait(string text)

## Parameters

variable | description
---|---
text | The text to speak.

## Return value

true on success, false on failure.

## Remarks

All previous text queued by the speak or speak_interrupt method will be cleared, and the new text spoken straight away.

Because script execution is paused while the text inside the speak_interrupt_wait method is being spoken, it cannot be stopped or interrupted.

## Example

```
tts_voice speech;

void main()
{
speech.speak_interrupt_wait("This is test, interrupting all previous announcements, and wait.");
}
```