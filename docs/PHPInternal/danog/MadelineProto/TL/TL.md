---
title: danog\MadelineProto\TL\TL: TL serialization.
description: 

---
# `danog\MadelineProto\TL\TL`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

TL serialization.  




## Method list:
* `getSecretLayer(): int`
* `getConstructors(bool $td): \danog\MadelineProto\TL\TLConstructors`
* `getMethods(bool $td): \danog\MadelineProto\TL\TLMethods`
* `getDescriptions(): array`
* `init(\danog\MadelineProto\Settings\TLSchema $files, \danog\MadelineProto\TL\TLCallback[] $objects): void`
* `getMethodNamespaces(): array`
* `getMethodsNamespaced(): array`
* `updateCallbacks(\danog\MadelineProto\TL\TLCallback[] $objects): void`
* `serializeObject(array $type, mixed $object, string $ctx, int $layer): \Generator`
* `serializeMethod(string $method, mixed $arguments): \Generator`
* `getLength(\resource|string $stream, array $type): int`
* `deserialize(string|\resource $stream, array $type): array`

## Methods:
### `getSecretLayer(): int`

Get secret chat layer version.



### `getConstructors(bool $td): \danog\MadelineProto\TL\TLConstructors`

Get constructors.


Parameters:
* `$td`: `bool`   


#### See also: 
* `\danog\MadelineProto\TL\TLConstructors`




### `getMethods(bool $td): \danog\MadelineProto\TL\TLMethods`

Get methods.


Parameters:
* `$td`: `bool`   


#### See also: 
* `\danog\MadelineProto\TL\TLMethods`




### `getDescriptions(): array`

Get TL descriptions.



### `init(\danog\MadelineProto\Settings\TLSchema $files, \danog\MadelineProto\TL\TLCallback[] $objects): void`

Initialize TL parser.


Parameters:
* `$files`: `\danog\MadelineProto\Settings\TLSchema` Scheme files  
* `$objects`: `\danog\MadelineProto\TL\TLCallback[]` TL Callback objects  


#### See also: 
* [`\danog\MadelineProto\Settings\TLSchema`: TL schema settings.](../Settings/TLSchema.md)
* [`\danog\MadelineProto\TL\TLCallback`: Interface for managing TL serialization callbacks.](./TLCallback.md)




### `getMethodNamespaces(): array`

Get TL namespaces.



### `getMethodsNamespaced(): array`

Get namespaced methods (method => namespace).



### `updateCallbacks(\danog\MadelineProto\TL\TLCallback[] $objects): void`

Update TL callbacks.


Parameters:
* `$objects`: `\danog\MadelineProto\TL\TLCallback[]` TL callbacks  


#### See also: 
* [`\danog\MadelineProto\TL\TLCallback`: Interface for managing TL serialization callbacks.](./TLCallback.md)




### `serializeObject(array $type, mixed $object, string $ctx, int $layer): \Generator`

Serialize TL object.


Parameters:
* `$type`: `array` TL type definition  
* `$object`: `mixed` Object to serialize  
* `$ctx`: `string` Context  
* `$layer`: `int` Layer version  


Fully typed return value:
```
\Generator<int|mixed, array|mixed, mixed, false|mixed|null|string>
```
#### See also: 
* `\Generator`




### `serializeMethod(string $method, mixed $arguments): \Generator`

Serialize method.


Parameters:
* `$method`: `string` Method name  
* `$arguments`: `mixed` Arguments  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<int>|\Amp\Promise<mixed>|\Amp\Promise<null|string>|\Amp\Promise<string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, string>
```
#### See also: 
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* [`\danog\MadelineProto\Stream\StreamInterface`: Generic stream interface.](../Stream/StreamInterface.md)
* `\Generator`




### `getLength(\resource|string $stream, array $type): int`

Get length of TL payload.


Parameters:
* `$stream`: `\resource|string` Stream  
* `$type`: `array` Type identifier  


#### See also: 
* `\resource`




### `deserialize(string|\resource $stream, array $type): array`

Deserialize TL object.


Parameters:
* `$stream`: `string|\resource` Stream  
* `$type`: `array` Type identifier  


Fully typed return value:
```
array{0: mixed, 1: \Amp\Promise}
```
#### See also: 
* `\resource`
* `\Amp\Promise`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
