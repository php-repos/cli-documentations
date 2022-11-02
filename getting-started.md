# CLI Package

## Introduction

CLI Package has a set of useful functions to work with CLI.
You can use these functions to interact with CLI.

## Requirements

This package uses the `php-mbstring` extension. Make sure you have this extension installed.

## Installation

You can simply install this package by running the following command:

```shell
saeghe add git@github.com:saeghe/cli.git
```

## Usage

You can use CLI functions by importing the function directly:

```php

use function Saeghe\Cli\IO\Write\success;

function my_function() {
    success('This is a success message.');
}

```

Or importing the file you need to use:

```php
use Saeghe\Cli\IO\Write;

function my_function() {
    Write\success('This is a success message.');
}

```

## Libraries

CLI Package is consist of several functions that are separated under these libraries:

- [IO Read Library](https://saeghe.com/packages/cli/documentations/io-read)
- [IO Write Library](https://saeghe.com/packages/cli/documentations/io-write)

