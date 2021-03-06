---
title: updates.channelDifferenceEmpty
description: There are no new updates
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/updates_channelDifferenceEmpty.html
---
# Constructor: updates.channelDifferenceEmpty  
[Back to constructors index](index.md)



There are no new updates

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|final|[Bool](../types/Bool.md) | Optional|Whether there are more updates that must be fetched (always false)|
|channel\_pts|[int](../types/int.md) | Yes|
|timeout|[int](../types/int.md) | Optional|Clients are supposed to refetch the channel difference after timeout seconds have elapsed|



### Type: [updates.ChannelDifference](../types/updates.ChannelDifference.md)


### Example:

```php
$updates_channelDifferenceEmpty = ['_' => 'updates.channelDifferenceEmpty', 'final' => Bool, 'channel_pts' => int, 'timeout' => int];
```  


Or, if you're into Lua:

```lua
updates_channelDifferenceEmpty={_='updates.channelDifferenceEmpty', final=Bool, channel_pts=int, timeout=int}

```


