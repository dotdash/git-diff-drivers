# git diff drivers

## Usage

To use any of these diff drivers, add them to your `$PATH`, add a git config
entry to your (global) git config and then set a matching git attribute for the
files you want to use the driver for. There's a config and attribute example
given for each driver.

Note that many git tools, like `git log` and `git show` will only utilize diff
drivers if you use the `--ext-diff` flag.

## composer-lock-diff-driver

The composer-lock-diff-driver utilizes
[composer-lock-diff](https://github.com/davidrjonas/composer-lock-diff) to
display changes to `composer.lock` files in a more readable way.

### git config

```bash
git config --global diff.composer-lock-diff.command composer-lock-diff-driver
```

### .gitattributes

```
composer.lock diff=composer-lock-diff
```
