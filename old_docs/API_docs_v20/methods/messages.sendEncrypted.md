---
title: messages.sendEncrypted
description: Sends a text message to a secret chat.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_sendEncrypted.html
---
# Method: messages.sendEncrypted
[Back to methods index](index.md)



Sends a text message to a secret chat.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Secret chat ID, Update, EncryptedMessage or InputEncryptedChat](../types/InputEncryptedChat.md) | Secret chat ID | Yes|
|data|[bytes](../types/bytes.md) | [DecryptedMessage](../types/DecryptedMessage.md) type | Yes|


### Return type: [messages.SentEncryptedMessage](../types/messages.SentEncryptedMessage.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_SentEncryptedMessage = $MadelineProto->messages->sendEncrypted(['peer' => InputEncryptedChat, 'data' => 'bytes', ]);
```

Or, if you're into Lua:

```lua
messages_SentEncryptedMessage = messages.sendEncrypted({peer=InputEncryptedChat, data='bytes', })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHAT_ID_INVALID|The provided chat id is invalid|
|400|DATA_INVALID|Encrypted data invalid|
|400|ENCRYPTION_DECLINED|The secret chat was declined|
|400|MSG_WAIT_FAILED|A waiting call returned an error|


