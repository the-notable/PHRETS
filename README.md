# PHRETS

A simple, free, open source PHP library for using [RETS](http://rets.org).

PHP + RETS = PHRETS

## Changes From Orignal phRETS Package

This repo is a fork of the original phRETS package at [troydavisson/phrets](https://packagist.org/packages/troydavisson/phrets).

**The original API has NOT been changed**

The changes are:
* All `die()` statements have been replaced with `Exception()`
* All `echo` statements now instead save messages to new messages property
* All methods and properties are now documented according to phpdoc standards
* Changed method names to `camelCase()`
* Library is now namespaced
* Added basic parameter type checking to public methods. Incompatible param types throw `Exception()`.

### Messages

Some methods return false on failure. Some will log messages internally which can be accessed by called the `getMessages()` method.

```php
if($Phrets->hasMessages()){
    foreach($Phrets->getMessages() as $message){
        echo $message;
    }
}
```

## Introduction

PHRETS provides PHP developers a way to integrate RETS functionality directly within new or existing code. A standard class of functions is made available to developers to connect and interact with a server much like they would with other APIs.

PHRETS handles the following aspects of RETS communication for you:
* Response parsing (for other non-XML responses such as HTTP multipart)
* XML Parsing
* Simple variables and arrays returned to the developer
* RETS communication (over HTTP)
* HTTP Header management
* Authentication
* Session/Cookie management


## Download

**Install via Composer** - Add [the-notable/phrets](https://packagist.org/packages/troydavisson/phrets) to your `composer.json` file, run `composer update` and you're set.  
**Manual Download** - The source code for PHRETS is available on [GitHub](http://github.com/troydavisson/PHRETS)


## Contribute

PHRETS is maintained in a public Git repository on GitHub.  Issue submissions and pull requests are encouraged if you run into issues or if you have fixes or changes to contribute.

## Documentation

View our [GitHub Wiki](https://github.com/troydavisson/PHRETS/wiki) for documentation, code snippets, examples, tips & tricks and more.
