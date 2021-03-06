---
title: danog\MadelineProto\Db\RedisArray: Redis database backend.
description: 

image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# `danog\MadelineProto\Db\RedisArray`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Redis database backend.  




## Method list:
* `initStartup(): \Generator`
* `initConnection(\danog\MadelineProto\Settings\Database\Redis $settings): \Generator`
* `offsetSet(string $index,  $value)`
* `isset( $key): \Promise<bool> true if the offset exists, otherwise false`
* `offsetUnset(string $index): \Amp\Promise`
* `getArrayCopy(): \Amp\Promise<array>`
* `count(): \Promise<int> The number of elements or public properties in the associated
array or object, respectively.`
* `clear(): \Amp\Promise`
* `getTable(): string`
* `setTable(string $table): self`
* `getInstance(string $table, \danog\MadelineProto\Db\DbArray|array|null $previous, \danog\MadelineProto\Settings\Database\DatabaseAbstract $settings): \Amp\Promise`

## Methods:
### `initStartup(): \Generator`

Initialize on startup.


#### See also: 
* `\Generator`




### `initConnection(\danog\MadelineProto\Settings\Database\Redis $settings): \Generator`

Initialize connection.


Parameters:
* `$settings`: `\danog\MadelineProto\Settings\Database\Redis`   


#### See also: 
* [`\danog\MadelineProto\Settings\Database\Redis`: Redis backend settings.](../Settings/Database/Redis.md)
* `\Generator`




### `offsetSet(string $index,  $value)`

Set value for an offset.


Parameters:
* `$index`: `string` <p>
The index to set for.
</p>  
* `$value`: ``   



### `isset( $key): \Promise<bool> true if the offset exists, otherwise false`

Check if key isset.


Parameters:
* `$key`: ``   


Return value: true if the offset exists, otherwise false


### `offsetUnset(string $index): \Amp\Promise`

Unset value for an offset.


Parameters:
* `$index`: `string` <p>
The offset to unset.
</p>  


#### See also: 
* `\Amp\Promise`




### `getArrayCopy(): \Amp\Promise<array>`

Get array copy.


#### See also: 
* `\Amp\Promise`




### `count(): \Promise<int> The number of elements or public properties in the associated
array or object, respectively.`

Count elements.


Return value: The number of elements or public properties in the associated
array or object, respectively.


### `clear(): \Amp\Promise`

Clear all elements.


#### See also: 
* `\Amp\Promise`




### `getTable(): string`

Get the value of table.



### `setTable(string $table): self`

Set the value of table.


Parameters:
* `$table`: `string`   



### `getInstance(string $table, \danog\MadelineProto\Db\DbArray|array|null $previous, \danog\MadelineProto\Settings\Database\DatabaseAbstract $settings): \Amp\Promise`




Parameters:
* `$table`: `string`   
* `$previous`: `\danog\MadelineProto\Db\DbArray|array|null`   
* `$settings`: `\danog\MadelineProto\Settings\Database\DatabaseAbstract`   


Fully typed return value:
```
\Amp\Promise<static>
```
#### See also: 
* [`\danog\MadelineProto\Db\DbArray`: DB array interface.](./DbArray.md)
* [`\danog\MadelineProto\Settings\Database\DatabaseAbstract`: Base class for database backends.](../Settings/Database/DatabaseAbstract.md)
* `\Amp\Promise`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
