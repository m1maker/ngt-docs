# network

network object


This method will send the given message known as packet unreliably to the network

# bool send_unreliable(uint id, string packet, int channel)

## Parameters

Variable | Description
---|---
id | The peer id you want to send to. This is 0 for all peer ids.
packet | The message or known as packet to send to the id.
channel | The channel to send.

## Return value

true on success, false on failure.