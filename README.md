php.vim
=======

This project is a fork of [php.vim--Garvin][garvin] which in turn is an update of the [php.vim][php-vim] script which in turn is an updated version of the php.vim syntax file distributed with Vim. Whew!

  [garvin]:  https://github.com/vim-scripts/php.vim--Garvin
  [php-vim]: http://www.vim.org/scripts/script.php?script_id=2874

Configuration
-------------

- `g:php_syntax_extensions_enabled`, `g:php_syntax_extensions_disabled`  
  `b:php_syntax_extensions_enabled`, `b:php_syntax_extensions_disabled`

  A list of extension names (lowercase) for which built-in functions, constants, classes and interfaces is enabled / disabled.

Updating
--------

The project comes with a Dockerfile which can be used to rebuild the syntax file.

```bash
docker build -t stanangeloff/php.vim .
docker run -i -t stanangeloff/php.vim scripts/update-vim-syntax.php | sed 's/\x0D$//' > syntax/php.vim
```
