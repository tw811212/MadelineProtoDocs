---
title: danog\MadelineProto\MTProtoSession\CallHandler: Manages method and object calls.
description: 

---
# `danog\MadelineProto\MTProtoSession\CallHandler`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages method and object calls.  




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it).  
## Method list:
* `methodRecall(string $watcherId, array $args): void`
* `methodCallAsyncRead(string $method, array|\Generator $args, array $aargs): \Generator`
* `methodCallAsyncWrite(string $method, array|\Generator $args, array $aargs): \Generator`
* `objectCall(string $object, array $args, array $aargs): \Generator`

## Methods:
### `methodRecall(string $watcherId, array $args): void`

Recall method.


Parameters:
* `$watcherId`: `string` Watcher ID for defer  
* `$args`: `array` Args  



### `methodCallAsyncRead(string $method, array|\Generator $args, array $aargs): \Generator`

Call method and wait asynchronously for response.
If the $aargs['noResponse'] is true, will not wait for a response.

Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`




### `methodCallAsyncWrite(string $method, array|\Generator $args, array $aargs): \Generator`

Call method and make sure it is asynchronously sent (generator).


Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`




### `objectCall(string $object, array $args, array $aargs): \Generator`

Send object and make sure it is asynchronously sent (generator).


Parameters:
* `$object`: `string` Object name  
* `$args`: `array` Arguments  
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`




