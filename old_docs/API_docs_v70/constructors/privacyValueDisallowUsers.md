---
title: privacyValueDisallowUsers
description: Disallow only certain users
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: privacyValueDisallowUsers  
[Back to constructors index](index.md)



Disallow only certain users

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|users|Array of [int](../types/int.md) | Yes|Users|



### Type: [PrivacyRule](../types/PrivacyRule.md)


### Example:

```php
$privacyValueDisallowUsers = ['_' => 'privacyValueDisallowUsers', 'users' => [int, int]];
```  


Or, if you're into Lua:

```lua
privacyValueDisallowUsers={_='privacyValueDisallowUsers', users={int}}

```


