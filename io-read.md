## Read Library

This document describes included functions in the `PhpRepos\Cli\IO\Read` library.

### argument

```php
function argument(int $number, ?string $default = null): ?string
```

#### Description

Returns the `number`th argument passed to the PHP file from CLI. 
Default passed value or `null` will be returned if the given `nth` argument is not passed.

#### Usages

```php
use function PhpRepos\Cli\IO\Read\argument;

$name = argument(1);
$email = argument(2, 'my-email@example.com');
```

```php
use PhpRepos\Cli\IO\Read;

$name = Read\argument(1);
$email = Read\argument(2, 'my-email@example.com');
```

#### Examples

```shell
php my-file.php // argument(1) => `null`
php my-file.php command add // argument(1) => `command`
php my-file.php command add // argument(2) => `add`
php my-file.php command -f add // argument(2) => `add`
php my-file.php command -f --parameter=anything add // argument(2) => `add`
php my-file.php command -f --parameter=anything add // argument(3) => `null`
```

### command

```php
function command(): ?string
```

#### Description

Returns the first command passed to the PHP file. It will return null if the first argument start with `-` or `--`. 
This is a shorthand for `argument(1, null)`.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Read\command;

$command = command();

```

Using namespace import:

```php
use PhpRepos\Cli\IO\Read;

$command = Read\command();
```

#### Examples

```shell
php my-file.php -v // command() => `null`
php my-file.php --version // command() => `null`
php my-file.php add anything // command() => `add`
php my-file.php help // command() => `help`
php my-file.php -version help // command() => `null`
```

### parameter

```php
function parameter(string $name, ?string $default = null): ?string
```

#### Description

Returns the `name` parameter passed to the PHP file. 
If `name` not passed, then it returns `null` or passed default value.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Read\command;

$name = parameter('name');
$email = parameter('email', 'john@example.com');

```

Using namespace import:

```php
use PhpRepos\Cli\IO\Read;

$name = Read\parameter('name');
$email = Read\parameter('email', 'john@example.com');
```

#### Examples

```shell
php my-file.php -v // parameter('name') => `null`
php my-file.php -v name // parameter('name') => `null`
php my-file.php -v -name // parameter('name') => `null`
php my-file.php -v --name=John // parameter('name') => `John`
php my-file.php -v --name="John Doe" // parameter('name') => `John Doe`
```

### option

```php
function option(string $name): bool
```

#### Description

Returns boolean to detect if the given `name` option passed to the PHP file.

#### Usages

Using function import:

```php
use function PhpRepos\Cli\IO\Read\command;

$versionPassed = option('version');
```

Using namespace import:

```php
use PhpRepos\Cli\IO\Read;

$versionPassed = Read\option('version');
```

#### Examples

```shell
php my-file.php // option('version') => `false`
php my-file.php -v // option('version') => `false`
php my-file.php -version // option('version') => `true`
php my-file.php --version // option('version') => `true`
php my-file.php --version= // option('version') => `true`
php my-file.php --version=false // option('version') => `true`
```
