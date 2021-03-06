---
title: messages.getFullChat
description: Returns full chat info according to its ID.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getFullChat.html
---
# Method: messages.getFullChat
[Back to methods index](index.md)



Returns full chat info according to its ID.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|chat\_id|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) |  | Optional|


### Return type: [messages.ChatFull](../types/messages.ChatFull.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_ChatFull = $MadelineProto->messages->getFullChat(['chat_id' => InputPeer, ]);
```

Or, if you're into Lua:

```lua
messages_ChatFull = messages.getFullChat({chat_id=InputPeer, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CHAT_ID_INVALID|The provided chat id is invalid|
|400|PEER_ID_INVALID|The provided peer id is invalid|
|401|SESSION_PASSWORD_NEEDED|2FA is enabled, use a password to login|


