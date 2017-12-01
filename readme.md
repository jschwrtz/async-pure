# Async Pure

> Pretty, minimal and fast ZSH prompt based on Pure

This is a fork of [sindresorhus/pure](https://github.com/sindresorhus/pure), which aims towards:

- fully async git integration
- [Monokai](https://github.com/deepsweet/Monokai-Soda-iTerm) friendly colors --- for machines and people!

<img src="https://raw.githubusercontent.com/jschwrtz/async-pure/master/screenshot_iterm.png" width="auto" style="display:block; margin: 0 auto;">

## Overview

Most prompts smash way too much together into an unreadable heap which creates a cluttered, ugly, and ridiculously slow environment. I wanted something visually pleasing that stayed out of my way while still providing the functionality that I need.

### Variations

- Comes with `λ` as the prompt character because I like lambdas. Changed with PURE_PROMPT_SYMBOL variable.
- Shows `git` branch, whether it has modified/staged/untracked files and upstream status with up/down triangles. *All checks are asynchronous.*
- Prompt character turns red if the last command didn't exit with `0`.
- Command execution time displays if it exceeds the set threshold.
- Username and host colored depending on UID and presence of the SSH session.
- Shows the current path in the title and the current command when a process is running.
- Makes a perfect starting point for your own custom prompt.

## Install

Requires Git 2.0.0+ and ZSH 5.2+. Older versions of ZSH work, but they are **not** recommended.

1. I don't care. Install it with whatever tools you want. No hipster-style `npm --global` installation or other bullshit included.

1. Symlink `async_pure.zsh` to somewhere in [`$fpath`](http://www.refining-linux.org/archives/46/ZSH-Gem-12-Autoloading-functions/) with the name `prompt_pure_setup`.

1. Symlink `async.zsh` in `$fpath` with the name `async`.

### npm

```console
$ npm install --global async-pure
```

or

```
$ yarn global add async-pure
```

That's it. Skip to [Getting started](#getting-started).

### Manually

```console
$ ln -s "$PWD/async_pure.zsh" /usr/local/share/zsh/site-functions/prompt_pure_setup
$ ln -s "$PWD/async.zsh" /usr/local/share/zsh/site-functions/async
```

*Run `echo $fpath` to see possible locations.*

For a user-specific installation (which would not require escalated privileges), simply add a directory to `$fpath` for that user:

```sh
# .zshenv or .zshrc
fpath=( "$HOME/.zfunctions" $fpath )
```

Then install the theme there:

```console
$ ln -s "$PWD/async_pure.zsh" "$HOME/.zfunctions/prompt_pure_setup"
$ ln -s "$PWD/async.zsh" "$HOME/.zfunctions/async"
```

## Getting started

Initialize the prompt system (if not so already) and choose `pure`:

```sh
# .zshrc
autoload -U promptinit; promptinit
prompt pure
```

## Options

| Option                          | Explanation                                                     | Default      |
| ------------------------------- | --------------------------------------------------------------- | ------------ |
| `PURE_CMD_MAX_EXEC_TIME`        | max execution time of a process before it is shown              | `5` seconds  |
| `PURE_GIT_FETCH`                | automatic `git fetch`, done only once per repo                  | `1`          |
| `PURE_GIT_FETCH_RETRY`          | timeout between `git fetch` retries if failed                   | `10` seconds |
| `PURE_GIT_UNTRACKED`            | enables untracked files in worktree check (disable for speedup) | `1`          |
| `PURE_GIT_DELAY_WORKTREE_CHECK` | timeout between git worktree checks, when they take > 2 seconds | `60`         |
| `PURE_GIT_DELAY_UPSTREAM_CHECK` | timeout between git upstream checks, when they take > 2 seconds | `60`         |
| `PURE_PROMPT_SYMBOL`            | the command prompt symbol                                       | `λ`   |
| `PURE_GIT_DOWN_ARROW`           | git info symbol: branch behind its upstream                     | `▼`          |
| `PURE_GIT_UP_ARROW`             | git info symbol: branch ahead of its upstream                   | `▲`          |
| `PURE_GIT_DIRTY`             | git info symbol: branch has uncommited changes                   | `x`          |
| `PURE_GIT_EVEN_ARROW`           | git info symbol: branch is even with its upstream               | empty string |
| `PURE_GIT_FETCH_IN_PROGRESS`    | git info string: async fetch in progress                        | `(fetch...)` |
| `PURE_GIT_FETCH_FAILED`         | git info string: async fetch failed, will retry                 | `(fetch!)`   |
| `PURE_GIT_UPSTREAM_NA`          | git info string: async upstream check in progress               | `?u`         |
| `PURE_GIT_WORKTREE_NA`          | git info string: async worktree check in progress               | `?w`         |
| `PURE_DEBUG`                    | debug output in systemd journal (`journalctl -t zshpure`)       | `0`          |
| `PURE_ALWAYS_SHOW_USER`         | show `user@host` always, not only when connected through SSH    | `0`          |

The worktree/upstream checks throttle when the last check takes > 2 seconds. This is to save CPU time.

### Custom handlers

There is a global array `prompt_pure_pieces` comprised of functions generating
pieces of the preprompt. To add a custom entry to the preprompt, declare a function
generating custom text and insert its name as an entry into the `prompt_pure_pieces`
array.

The custom function must return generated text by appending new entries to the
`preprompt` array (declared in a parent scope) See below for an example.

#### Handler Example

```sh
# .zshrc

autoload -U promptinit; promptinit

# optionally define some options
PURE_CMD_MAX_EXEC_TIME=10

# optionally define custom generators
prompt_custom() {
    preprompt+=( custom )
}

prompt pure

# add the generator where it's needed
prompt_pure_pieces=(
    ${prompt_pure_pieces:0:2}
    prompt_custom
    ${prompt_pure_pieces:2}
)

```

## Tips

In the screenshot you see Async Pure running in [iTerm2](https://www.iterm2.com) with the [monokai-soda](https://github.com/deepsweet/Monokai-Soda-iTerm) theme and Source Code Pro for Powerline font.

The [Tomorrow Night Eighties](https://github.com/chriskempson/tomorrow-theme) theme with the [Droid Sans Mono](https://fonts.google.com/specimen/Droid+Sans+Mono) font (15pt) is also a [nice combination](https://github.com/sindresorhus/pure/blob/95ee3e7618c6e2162a1e3cdac2a88a20ac3beb27/screenshot.png).<br>
_Just make sure you have anti-aliasing enabled in your terminal._

To have commands colorized as seen in the screenshot, install [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting).

## Integration

### [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

1. Set `ZSH_THEME=""` in your `.zshrc` to disable oh-my-zsh themes.
1. Follow the Pure [Install](#install) instructions.

**NOTE:** `oh-my-zsh` overrides the prompt so Pure must be activated _after_ `source $ZSH/oh-my-zsh.sh`.

OR

1. Symlink async-pure.zsh to async-pure.zsh-theme.
    ```console
    ln -s "$PWD/async_pure.zsh" "$HOME/.oh-my-zsh/custom/themes/async-pure.zsh-theme"
    ```
1. Set ZSH_THEME="async-pure" in your .zshrc.

### [antigen](https://github.com/zsh-users/antigen)

Update your `.zshrc` file with the following two lines (order matters). Do not use the `antigen theme` function.

```sh
antigen bundle mafredri/zsh-async
antigen bundle jschwrtz/async-pure
```

### [antibody](https://github.com/getantibody/antibody)

Update your `.zshrc` file with the following two lines (order matters):

```sh
antibody bundle mafredri/zsh-async
antibody bundle jschwrtz/async-pure
```

### [zplug](https://github.com/zplug/zplug)

Update your `.zshrc` file with the following two lines:

```sh
zplug mafredri/zsh-async, from:github
zplug jschwrtz/async-pure, use:async_pure.zsh, from:github, as:theme
```

## License

Original code: MIT© [Sindre Sorhus](http://sindresorhus.com)

Further work: Copyright (c) 2017 Jay Schwartz

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
