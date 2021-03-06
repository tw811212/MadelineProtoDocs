---
title: danog\MadelineProto\VoIP\AuthKeyHandler: Manages the creation of the authorization key.
description: https://core.telegram.org/mtproto/auth_key
https://core.telegram.org/mtproto/samples-auth_key

---
# `danog\MadelineProto\VoIP\AuthKeyHandler`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages the creation of the authorization key.  

https://core.telegram.org/mtproto/auth_key
https://core.telegram.org/mtproto/samples-auth_key


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it).  
## Method list:
* `requestCall(mixed $user): \Generator`
* `acceptCall(array $call): \Generator`
* `confirmCall(array $params): \Generator`
* `completeCall(array $params): \Generator`
* `callStatus(int $id): int`
* `getCall(int $call): array`
* `discardCall(array $call, array $reason, array $rating, bool $need_debug): \Generator`

## Methods:
### `requestCall(mixed $user): \Generator`

Request VoIP call.


Parameters:
* `$user`: `mixed` User  


#### See also: 
* `\Generator`




### `acceptCall(array $call): \Generator`

Accept call.


Parameters:
* `$call`: `array` Call  


#### See also: 
* `\Generator`




### `confirmCall(array $params): \Generator`

Confirm call.


Parameters:
* `$params`: `array` Params  


#### See also: 
* `\Generator`




### `completeCall(array $params): \Generator`

Complete call handshake.


Parameters:
* `$params`: `array` Params  


#### See also: 
* `\Generator`




### `callStatus(int $id): int`

Get call status.


Parameters:
* `$id`: `int` Call ID  



### `getCall(int $call): array`

Get call info.


Parameters:
* `$call`: `int` Call ID  



### `discardCall(array $call, array $reason, array $rating, bool $need_debug): \Generator`

Discard call.


Parameters:
* `$call`: `array` Call  
* `$reason`: `array`   
* `$rating`: `array` Rating  
* `$need_debug`: `bool` Need debug?  


#### See also: 
* `\Generator`




