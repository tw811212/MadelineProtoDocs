---
title: decryptedMessageLayer
description: Sets the layer number for the contents of an encrypted message.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: decryptedMessageLayer\_17  
[Back to constructors index](index.md)



Sets the layer number for the contents of an encrypted message.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|layer|[int](../types/int.md) | Yes|Layer number. Mimimal value - **17** (the layer in which the constructor was added).|
|in\_seq\_no|[int](../types/int.md) | Yes|2x the number of messages in the sender's inbox (including deleted and service messages), incremented by 1 if current user was not the chat creator<br>Parameter added in [Layer 17](https://core.telegram.org/api/layers#layer-17).|
|out\_seq\_no|[int](../types/int.md) | Yes|2x the number of messages in the recipient's inbox (including deleted and service messages), incremented by 1 if current user was the chat creator<br>Parameter added in [Layer 17](https://core.telegram.org/api/layers#layer-17).|
|message|[DecryptedMessage](../types/DecryptedMessage.md) | Yes|The content of message itself|



### Type: [DecryptedMessageLayer](../types/DecryptedMessageLayer.md)


### Example:

```php
$decryptedMessageLayer_17 = ['_' => 'decryptedMessageLayer', 'layer' => int, 'in_seq_no' => int, 'out_seq_no' => int, 'message' => DecryptedMessage];
```  


Or, if you're into Lua:

```lua
decryptedMessageLayer_17={_='decryptedMessageLayer', layer=int, in_seq_no=int, out_seq_no=int, message=DecryptedMessage}

```


