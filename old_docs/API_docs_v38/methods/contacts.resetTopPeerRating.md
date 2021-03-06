---
title: contacts.resetTopPeerRating
description: Reset [rating](https://core.telegram.org/api/top-rating) of top peer
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/contacts_resetTopPeerRating.html
---
# Method: contacts.resetTopPeerRating
[Back to methods index](index.md)



Reset [rating](https://core.telegram.org/api/top-rating) of top peer

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|category|[TopPeerCategory](../types/TopPeerCategory.md) | Top peer category | Yes|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | Peer whose rating should be reset | Optional|


### Return type: [Bool](../types/Bool.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->contacts->resetTopPeerRating(['category' => TopPeerCategory, 'peer' => InputPeer, ]);
```

Or, if you're into Lua:

```lua
Bool = contacts.resetTopPeerRating({category=TopPeerCategory, peer=InputPeer, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|PEER_ID_INVALID|The provided peer id is invalid|


