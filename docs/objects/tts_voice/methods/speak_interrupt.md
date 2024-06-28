# tts_voice


tts_voice object

This method will speak a given string, interrupting all other queued strings.

# bool speak_interrupt(string text)

## Parameters

variable | description
---|---
text | The text to speak.

## Return value

true on success, false on failure.

## Remarks

All previous text queued by the speak or speak_interrupt method will be cleared, and the new text spoken straight away.

## Example

```
tts_voice speech;
void main()
{
speech.speak_interrupt("This is test interrupting all previous announcements.");
}
```