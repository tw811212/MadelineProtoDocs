---
title: channel
description: Channel/supergroup info
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: channel  
[Back to constructors index](index.md)



Channel/supergroup info

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|id|[int](../types/int.md) | Yes|ID of the channel|
|access\_hash|[long](../types/long.md) | Yes|Access hash|
|title|[string](../types/string.md) | Yes|Title|
|username|[string](../types/string.md) | Optional|Username|
|photo|[ChatPhoto](../types/ChatPhoto.md) | Optional|Profile photo|
|date|[int](../types/int.md) | Yes|Date when the user joined the supergroup/channel, or if the user isn't a member, its creation date|
|version|[int](../types/int.md) | Yes|Version of the channel (always `0`)|



### Type: [Chat](../types/Chat.md)


### Example:

```php
$channel = ['_' => 'channel', 'id' => int, 'access_hash' => long, 'title' => 'string', 'username' => 'string', 'photo' => ChatPhoto, 'date' => int, 'version' => int];
```  


Or, if you're into Lua:

```lua
channel={_='channel', id=int, access_hash=long, title='string', username='string', photo=ChatPhoto, date=int, version=int}

```


