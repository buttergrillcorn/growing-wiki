+++
title = "How to manage NPM packages on Arch Linux"
author = ["James"]
date = 2025-12-27T21:08:00+00:00
draft = false
+++

## What to avoid! {#what-to-avoid}

Avoid using `sudo` with `npm` to install packages as this can lead to permission issues, security risks and conflicts with the `pacman` package manager.


## The "correct" methods {#the-correct-methods}


### Method 1 - Use a Version Manager {#method-1-use-a-version-manager}

The first method is to use something like `fnm` ([Fast Node Manager](https://github.com/Schniz/fnm)) or `nvm` ([Node Version Manager](https://github.com/nvm-sh/nvm)).

These will allow you to install multiple versions of Node.js for development without the use of root privileges. Everything will be contained in your `$HOME` directory.

So if you're on Arch Linux, you can install the managers using `pacman` like:

```bash
sudo pacman -S fnm
# or pacman -S nvm
```

You will then have to set up your shell, in my case `~/.zshrc`, like:

```bash
eval "$(fnm evn --use-on-cd)"
```
