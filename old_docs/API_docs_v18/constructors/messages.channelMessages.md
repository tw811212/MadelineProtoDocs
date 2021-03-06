---
title: messages.channelMessages
description: Channel messages
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/messages_channelMessages.html
---
# Constructor: messages.channelMessages  
[Back to constructors index](index.md)



Channel messages

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|pts|[int](../types/int.md) | Yes|[Event count after generation](https://core.telegram.org/api/updates)|
|count|[int](../types/int.md) | Yes|Total number of results were found server-side (may not be all included here)|
|messages|Array of [Message](../types/Message.md) | Yes|Found messages|
|chats|Array of [Chat](../types/Chat.md) | Yes|Chats|
|users|Array of [User](../types/User.md) | Yes|Users|



### Type: [messages.Messages](../types/messages.Messages.md)


### Example:

```php
$messages_channelMessages = ['_' => 'messages.channelMessages', 'pts' => int, 'count' => int, 'messages' => [Message, Message], 'chats' => [Chat, Chat], 'users' => [User, User]];
```  


Or, if you're into Lua:

```lua
messages_channelMessages={_='messages.channelMessages', pts=int, count=int, messages={Message}, chats={Chat}, users={User}}

```


