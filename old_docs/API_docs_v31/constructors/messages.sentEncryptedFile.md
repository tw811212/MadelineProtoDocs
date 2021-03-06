---
title: messages.sentEncryptedFile
description: Message with a file enclosure sent to a protected chat
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/messages_sentEncryptedFile.html
---
# Constructor: messages.sentEncryptedFile  
[Back to constructors index](index.md)



Message with a file enclosure sent to a protected chat

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|date|[int](../types/int.md) | Yes|Sending date|
|file|[EncryptedFile](../types/EncryptedFile.md) | Optional|Attached file|



### Type: [messages.SentEncryptedMessage](../types/messages.SentEncryptedMessage.md)


### Example:

```php
$messages_sentEncryptedFile = ['_' => 'messages.sentEncryptedFile', 'date' => int, 'file' => EncryptedFile];
```  


Or, if you're into Lua:

```lua
messages_sentEncryptedFile={_='messages.sentEncryptedFile', date=int, file=EncryptedFile}

```


