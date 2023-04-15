## Write Library

This document describes included functions in the `PhpRepos\Cli\IO\Write` library.

### output

```php
function output(string $string): void
```

#### Description

Print the given `string` directly in the stdout with the default font color.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\output;

output('Hello World!');
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

Write\output('Hello World!');
```

#### Examples

```php
output('Hello World!'); // Output => Hello World! 
```

### assert_output

```php
function assert_output(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `output` function and resulted in the `actual` output.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\assert_output;

$output = shell_exec('command');
assert_output($expected, $output);
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_output($expected, $output);
```

### line

```php
function line(string $string): void
```

#### Description

Print the given `string` directly in the stdout with the default font color and adds a `PHP_EOL` to the end of given string.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\line;

line('Hello World!');
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

Write\line('Hello World!');
```

#### Examples

```php
line('Hello World!'); // Output => Hello World! \n
```

### assert_line

```php
function assert_line(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `line` function and resulted in the `actual` output.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\assert_line;

$output = shell_exec('command');
assert_line($expected, $output);
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_line($expected, $output);
```

### success

```php
function success(string $string): void
```

#### Description

Print the given `string` directly in the stdout with green font color and adds a `PHP_EOL` to the end of given string.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\success;

success('Hello World!');
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

Write\success('Hello World!');
```

#### Examples

```php
success('Hello World!'); // Output(With a green font color) => Hello World! \n
```

### assert_success

```php
function assert_success(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `success` function and resulted in the `actual` output.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\assert_success;

$output = shell_exec('command');
assert_success($expected, $output);
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_success($expected, $output);
```

### error

```php
function error(string $string): void
```

#### Description

Print the given `string` directly in the stdout with red font color and adds a `PHP_EOL` to the end of given string.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\error;

error('Hello World!');
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

Write\error('Hello World!');
```

#### Examples

```php
error('Hello World!'); // Output(With a red font color) => Hello World! \n
```

### assert_error

```php
function assert_error(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `error` function and resulted in the `actual` output.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Write\assert_error;

$output = shell_exec('command');
assert_error($expected, $output);
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_error($expected, $output);
```
