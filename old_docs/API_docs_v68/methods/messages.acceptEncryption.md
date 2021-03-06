---
title: messages.acceptEncryption
description: You cannot use this method directly, see https://docs.madelineproto.xyz for more info on handling secret chats
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_acceptEncryption.html
---
# Method: messages.acceptEncryption  
[Back to methods index](index.md)


You cannot use this method directly, see https://docs.madelineproto.xyz for more info on handling secret chats

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Secret chat ID, Update, EncryptedMessage or InputEncryptedChat](../types/InputEncryptedChat.md) | You cannot use this method directly, see https://docs.madelineproto.xyz for more info on handling secret chats | Yes|
|g\_b|[bytes](../types/bytes.md) | You cannot use this method directly, see https://docs.madelineproto.xyz for more info on handling secret chats | Yes|
|key\_fingerprint|[long](../types/long.md) | You cannot use this method directly, see https://docs.madelineproto.xyz for more info on handling secret chats | Yes|


### Return type: [EncryptedChat](../types/EncryptedChat.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$EncryptedChat = $MadelineProto->messages->acceptEncryption(['peer' => InputEncryptedChat, 'g_b' => 'bytes', 'key_fingerprint' => long, ]);
```

Or, if you're into Lua:

```lua
EncryptedChat = messages.acceptEncryption({peer=InputEncryptedChat, g_b='bytes', key_fingerprint=long, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHAT_ID_INVALID|The provided chat id is invalid|
|400|ENCRYPTION_ALREADY_ACCEPTED|Secret chat already accepted|
|400|ENCRYPTION_ALREADY_DECLINED|The secret chat was already declined|


