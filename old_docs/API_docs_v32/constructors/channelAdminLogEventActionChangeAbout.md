---
title: channelAdminLogEventActionChangeAbout
description: The description was changed
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: channelAdminLogEventActionChangeAbout  
[Back to constructors index](index.md)



The description was changed

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|prev\_value|[string](../types/string.md) | Yes|Previous description|
|new\_value|[string](../types/string.md) | Yes|New description|



### Type: [ChannelAdminLogEventAction](../types/ChannelAdminLogEventAction.md)


### Example:

```php
$channelAdminLogEventActionChangeAbout = ['_' => 'channelAdminLogEventActionChangeAbout', 'prev_value' => 'string', 'new_value' => 'string'];
```  


Or, if you're into Lua:

```lua
channelAdminLogEventActionChangeAbout={_='channelAdminLogEventActionChangeAbout', prev_value='string', new_value='string'}

```


