## Write Library

This document describes included functions in the `Saeghe\Cli\IO\Write` library.

### line

```php
function line(string $string): void
```

#### Description

Print the given `string` directly in the stdout with the default font color.

#### Usages

```php
use function Saeghe\Cli\IO\Write\line;

line('Hello World!');
```

```php
use Saeghe\Cli\IO\Write;

Write\line('Hello World!');
```

#### Examples

```php
line('Hello World!'); // Output => Hello World! 
```

### assert_line

```php
function assert_line(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `line` function and resulted in the `actual` output.

#### Usages

```php
use function Saeghe\Cli\IO\Write\assert_line;

$output = shell_exec('command');
assert_line($expected, $output);
```

```php
use Saeghe\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_line($expected, $output);
```

### success

```php
function success(string $string): void
```

#### Description

Print the given `string` directly in the stdout with green font color.

#### Usages

```php
use function Saeghe\Cli\IO\Write\success;

success('Hello World!');
```

```php
use Saeghe\Cli\IO\Write;

Write\success('Hello World!');
```

#### Examples

```php
success('Hello World!'); // Output(With a green font color) => Hello World!
```

### assert_success

```php
function assert_success(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `success` function and resulted in the `actual` output.

#### Usages

```php
use function Saeghe\Cli\IO\Write\assert_success;

$output = shell_exec('command');
assert_success($expected, $output);
```

```php
use Saeghe\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_success($expected, $output);
```

### error

```php
function error(string $string): void
```

#### Description

Print the given `string` directly in the stdout with red font color.

#### Usages

```php
use function Saeghe\Cli\IO\Write\error;

error('Hello World!');
```

```php
use Saeghe\Cli\IO\Write;

Write\error('Hello World!');
```

#### Examples

```php
error('Hello World!'); // Output(With a red font color) => Hello World!
```

### assert_error

```php
function assert_error(string $expected, string $actual): bool
```

#### Description

Assert to see the `expected` string has been printed using the `error` function and resulted in the `actual` output.

#### Usages

```php
use function Saeghe\Cli\IO\Write\assert_error;

$output = shell_exec('command');
assert_error($expected, $output);
```

```php
use Saeghe\Cli\IO\Write;

$output = shell_exec('command');
Write\assert_error($expected, $output);
```
