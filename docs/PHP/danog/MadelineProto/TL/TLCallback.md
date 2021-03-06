---
title: danog\MadelineProto\TL\TLCallback: Interface for managing TL serialization callbacks.
description: 

---
# `danog\MadelineProto\TL\TLCallback`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Interface for managing TL serialization callbacks.  




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it).  
## Method list:
* `getMethodCallbacks(): array`
* `getMethodBeforeCallbacks(): array`
* `getConstructorCallbacks(): array`
* `getConstructorBeforeCallbacks(): array`
* `getConstructorSerializeCallbacks(): array`
* `getTypeMismatchCallbacks(): array`

## Methods:
### `getMethodCallbacks(): array`

Called after serialization of method.
Pass the method name and arguments


### `getMethodBeforeCallbacks(): array`

Called right before serialization of method starts.
Pass the method name


### `getConstructorCallbacks(): array`

Called right after deserialization of object, passing the final object.



### `getConstructorBeforeCallbacks(): array`

Called right before deserialization of object.
Pass only the constructor name


### `getConstructorSerializeCallbacks(): array`

Called right before serialization of constructor.
Passed the object, will return a modified version.


### `getTypeMismatchCallbacks(): array`

Called if objects of the specified type cannot be serialized.
Passed the unserializable object,
will try to convert it to an object of the proper type.


