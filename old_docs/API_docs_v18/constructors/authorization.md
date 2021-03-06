---
title: authorization
description: Logged-in session
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: authorization  
[Back to constructors index](index.md)



Logged-in session

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|hash|[long](../types/long.md) | Yes|Identifier|
|device\_model|[string](../types/string.md) | Yes|Device model|
|platform|[string](../types/string.md) | Yes|Platform|
|system\_version|[string](../types/string.md) | Yes|System version|
|api\_id|[int](../types/int.md) | Yes|[API ID](https://core.telegram.org/api/obtaining_api_id)|
|app\_name|[string](../types/string.md) | Yes|App name|
|app\_version|[string](../types/string.md) | Yes|App version|
|date\_created|[int](../types/int.md) | Yes|When was the session created|
|date\_active|[int](../types/int.md) | Yes|When was the session last active|
|ip|[string](../types/string.md) | Yes|Last known IP|
|country|[string](../types/string.md) | Yes|Country determined from IP|
|region|[string](../types/string.md) | Yes|Region determined from IP|



### Type: [Authorization](../types/Authorization.md)


### Example:

```php
$authorization = ['_' => 'authorization', 'hash' => long, 'device_model' => 'string', 'platform' => 'string', 'system_version' => 'string', 'api_id' => int, 'app_name' => 'string', 'app_version' => 'string', 'date_created' => int, 'date_active' => int, 'ip' => 'string', 'country' => 'string', 'region' => 'string'];
```  


Or, if you're into Lua:

```lua
authorization={_='authorization', hash=long, device_model='string', platform='string', system_version='string', api_id=int, app_name='string', app_version='string', date_created=int, date_active=int, ip='string', country='string', region='string'}

```


