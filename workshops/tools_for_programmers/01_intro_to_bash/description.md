# Tools for Programmers 01: Intro to Bash

## Facebook Event

[https://www.facebook.com/events/245447659318325](https://www.facebook.com/events/245447659318325)

## Feedback Form

[http://goo.gl/cJdBuQ](http://goo.gl/cJdBuQ)

## Slides
[https://docs.google.com/presentation/d/1OXMbABYQYuiq8tqymXsbSQiFyhNJblwqEb-XeWrXqjk/edit?usp=sharing](https://docs.google.com/presentation/d/1OXMbABYQYuiq8tqymXsbSQiFyhNJblwqEb-XeWrXqjk/edit?usp=sharing)

## Syntax Summary

Given an example bash command:

```bash
root@hal9000:/tmp$ ls --all -lh /home
```

The following parts mean the following things:

- `root` is the username.

- `hal900` is the "hostname" (the computer you are on).

- `/tmp` is the current directory.

- `ls` is an example executable (see [ls](#ls)).

- `--all` is a [long option](#long-options).

- `-lh` is a collection of [short options](#short-options), in this case `l` and `h`.

- `/home` is a parameter, in this case, a directory that `ls` will be run on.

## Commands/executables encountered in the workshop

### `ls`

TODO:

### `man`

TODO:

### `ssh`

This program can be used to securely connect to a remote shell, on another computer. Even across the internet!

## Options

Lot's of executable programs in bash (and other terminals) will take options which are prepended by a `-` or `--`. These are useful if you want programs to do slightly different things that the designers of the program have added to them. In order to see what options a program will take, you can always use [`man`](#man)

### Long Options

eg. `--all`, these options are written out as English words and are very readable, but may require a lot of typing.

### Short Options

eg. `-a`, these options are quick and easy to type, but remembering what they are can be a bit tricky sometimes. However, a nice feature is that you can list a bunch of them together. Eg. `-la` means, "Do option `-a` AND option `l`". However,
this is by convention, and some programs will require options to be separate parameters, even in short form.

### Helpful Shortcuts