---
title: account.setGlobalPrivacySettings
description: account.setGlobalPrivacySettings parameters, return type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_setGlobalPrivacySettings.html
---
# Method: account.setGlobalPrivacySettings
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|settings|[GlobalPrivacySettings](../types/GlobalPrivacySettings.md) | Yes|


### Return type: [GlobalPrivacySettings](../types/GlobalPrivacySettings.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$GlobalPrivacySettings = $MadelineProto->account->setGlobalPrivacySettings(['settings' => GlobalPrivacySettings, ]);
```

Or, if you're into Lua:

```lua
GlobalPrivacySettings = account.setGlobalPrivacySettings({settings=GlobalPrivacySettings, })
```

