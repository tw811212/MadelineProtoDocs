---
title: danog\MadelineProto\MTProtoTools\Files: Manages upload and download of files.
description: 

---
# `danog\MadelineProto\MTProtoTools\Files`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages upload and download of files.  




## Method list:
* `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): \Generator`
* `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): \Generator`
* `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): \Generator`
* `getFileInfo(mixed $constructor): \Generator<array>`
* `getPropicInfo(mixed $messageMedia): \Generator<array>`
* `extractBotAPIFile(array $info): ?array`
* `getDownloadInfo(mixed $messageMedia): \Generator<array>`
* `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): \Generator`
* `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): \Generator Downloaded file path`
* `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): \Generator`
* `downloadToBrowser(array|string $messageMedia, callable $cb): \Generator`
* `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface $stream, callable $cb, int $offset, int $end): \Generator`
* `downloadToResponse(array|string $messageMedia, \ServerRequest $request, callable $cb): \Generator Returned response`
* `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): \Generator`
* `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): \Generator`
* `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): \Generator`

## Methods:
### `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): \Generator`

Upload file from URL.


Parameters:
* `$url`: `string|\danog\MadelineProto\FileCallbackInterface` URL of file  
* `$size`: `int` Size of file  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\Http\Client\Response>|\Amp\Promise<int>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\Http\Client\Response`
* [`\danog\MadelineProto\Stream\StreamInterface`: Generic stream interface.](../Stream/StreamInterface.md)
* `\Generator`




### `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): \Generator`

Upload file from callable.
The callable must accept two parameters: int $offset, int $size
The callable must return a string with the contest of the file at the specified offset and size.

Parameters:
* `$callable`: `mixed` Callable  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether chunks can be fetched out of order  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int, \Amp\Promise|\Amp\Promise<array>, mixed, array{_: string, id: string, parts: int, name: string, mime_type: string, key_fingerprint?: mixed, key?: mixed, iv?: mixed, md5_checksum: string}>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): \Generator`

Reupload telegram file.


Parameters:
* `$media`: `mixed` Telegram file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|array, mixed, mixed>
```
#### See also: 
* `\Amp\Promise`
* `\Generator`




### `getFileInfo(mixed $constructor): \Generator<array>`

Get info about file.


Parameters:
* `$constructor`: `mixed` File ID  


#### See also: 
* `\Generator`




### `getPropicInfo(mixed $messageMedia): \Generator<array>`

Get download info of the propic of a user
Returns an array with the following structure:.
`$info['ext']` - The file extension
`$info['name']` - The file name, without the extension
`$info['mime']` - The file mime type
`$info['size']` - The file size

Parameters:
* `$messageMedia`: `mixed` File ID  


#### See also: 
* `\Generator`




### `extractBotAPIFile(array $info): ?array`

Extract file info from bot API message.


Parameters:
* `$info`: `array` Bot API message object  



### `getDownloadInfo(mixed $messageMedia): \Generator<array>`

Get download info of file
Returns an array with the following structure:.
`$info['ext']` - The file extension
`$info['name']` - The file name, without the extension
`$info['mime']` - The file mime type
`$info['size']` - The file size

Parameters:
* `$messageMedia`: `mixed` File ID  


#### See also: 
* `\Generator`




### `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): \Generator`

Download file to directory.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$dir`: `string|\danog\MadelineProto\FileCallbackInterface` Directory where to download the file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<callable|null>|\Amp\Promise<mixed>|array|bool|mixed, mixed, false|string>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\Generator`




### `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): \Generator Downloaded file path`

Download file.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$file`: `string|\danog\MadelineProto\FileCallbackInterface` Downloaded file path  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Return value: Downloaded file path

Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<callable|null>|\Amp\Promise<mixed>|array|bool|mixed, mixed, false|string>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\Generator`




### `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): \Generator`

Download file to callable.
The callable must accept two parameters: string $payload, int $offset
The callable will be called (possibly out of order, depending on the value of $seekable).
The callable should return the number of written bytes.

Parameters:
* `$messageMedia`: `mixed` File to download  
* `$callable`: `callable|\danog\MadelineProto\FileCallbackInterface` Chunk callback  
* `$cb`: `callable` Status callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether the callable can be called out of order  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to stop downloading (inclusive)  
* `$part_size`: `int` Size of each chunk  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|array, mixed, true>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Promise`
* `\Generator`




### `downloadToBrowser(array|string $messageMedia, callable $cb): \Generator`

Download file to browser.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:
* `$messageMedia`: `array|string` File to download  
* `$cb`: `callable` Status callback (can also use FileCallback)  


#### See also: 
* `\Generator`




### `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface $stream, callable $cb, int $offset, int $end): \Generator`

Download file to stream.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$stream`: `mixed|\danog\MadelineProto\FileCallbackInterface` Stream where to download file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to end download  


Fully typed return value:
```
\Generator<int, \Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<mixed>|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Ipc\Sync\ChannelledSocket`
* `\Amp\Promise`
* `\Generator`




### `downloadToResponse(array|string $messageMedia, \ServerRequest $request, callable $cb): \Generator Returned response`

Download file to amphp/http-server response.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:
* `$messageMedia`: `array|string` File to download  
* `$request`: `\ServerRequest` Request  
* `$cb`: `callable` Status callback (can also use FileCallback)  


Return value: Returned response

Fully typed return value:
```
\Generator<mixed, array, mixed, \Amp\Http\Server\Response>
```
#### See also: 
* `\ServerRequest`
* `\Amp\Http\Server\Response`
* `\Generator`




### `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): \Generator`

Upload file to secret chat.


Parameters:
* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<int>|\Amp\Promise<mixed>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* [`\danog\MadelineProto\Stream\StreamInterface`: Generic stream interface.](../Stream/StreamInterface.md)
* `\Generator`




### `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): \Generator`

Upload file.


Parameters:
* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<\Amp\File\File>|\Amp\Promise<\Amp\Ipc\Sync\ChannelledSocket>|\Amp\Promise<int>|\Amp\Promise<mixed>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../FileCallbackInterface.md)
* `\Amp\Promise`
* `\Amp\File\File`
* `\Amp\Ipc\Sync\ChannelledSocket`
* [`\danog\MadelineProto\Stream\StreamInterface`: Generic stream interface.](../Stream/StreamInterface.md)
* `\Generator`




### `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): \Generator`

Upload file from stream.


Parameters:
* `$stream`: `mixed` PHP resource or AMPHP async stream  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<int>|\Amp\Promise<null|string>|\danog\MadelineProto\Stream\StreamInterface|array|int|mixed, mixed, mixed>
```
#### See also: 
* `\Amp\Promise`
* [`\danog\MadelineProto\Stream\StreamInterface`: Generic stream interface.](../Stream/StreamInterface.md)
* `\Generator`




## Properties
* `$settings`: `\Settings` Settings
---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
