# CLI Package

## Introduction

CLI Package has a set of useful functions to work with CLI.
You can use these functions to interact with CLI.

## Requirements

This package uses the `php-mbstring` extension. Make sure you have this extension installed.

## Installation

You can simply install this package by running the following command:

```shell
phpkg add https://github.com/php-repos/cli.git
```

You may find it necessary to include the `--force` option when adding the `cli` to your project. This is because 
the `cli` relies on the `test-runner`, and the two may occasionally utilize different versions of each other. This 
discrepancy can potentially disrupt the dependency resolution check.

```shell
phpkg add https://github.com/php-repos/cli.git --force
```

## Usage

You can use CLI functions by importing the function directly:

```php

use function PhpRepos\Cli\Output\success;

function my_function() {
    success('This is a success message.');
}

```

Or importing the file you need to use:

```php
use PhpRepos\Cli\Output;

function my_function() {
    Output\success('This is a success message.');
}

```

## Libraries

CLI Package is consist of several functions that are separated under these libraries:

- [Output Library](https://phpkg.com/packages/cli/documentations/output)

