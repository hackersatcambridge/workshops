# Tools for Programmers 01: Intro to Bash

And cheat sheet!

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

- `ls` is an example executable (see [`ls`](#ls)).

- `--all` is a [long option](#long-options).

- `-lh` is a collection of [short options](#short-options), in this case `l` and `h`.

- `/home` is a parameter, in this case, a directory that `ls` will be run on.

## Commands/executables encountered in the workshop

### `man`

Learn how a given program works.

eg.

```bash
man ls
```

Will tell you everything about how `ls` works.

### `cd`

Change the current directory you are in!

`cd ..` can be used to go to the parent directory.

### `ls`

List everything in a given directory.

eg.

```bash
ls /home
```

Will list everything in the `/home` directory.

### `rm`

Remove the given file!

eg.

```bash
rm my_file.txt
```

Will delete `my_file.txt`!

Don't forget that you can use the `-r` option to
delete a directory!

### `mkdir`

Make a directory

eg.

```bash
mkdir my_directory
```

Will make a directory called `my_directory`!

### `touch`

Make a file

eg.

```bash
touch my_file.txt
```

Will make a file called `my_file.txt`!

You could then edit it with [`nano`](#nano), for example!

### `ssh`

This program can be used to securely connect to a remote shell, on another computer. Even across the internet!

eg. If you are a Cambridge student, you get access to your own space on University machines!

```bash
ssh crsid@linux.ds.cam.ac.uk
```

### `echo`

Print all the arguments as text!

eg.

```bash
echo this is some text
```

### `cat`

View the contents of a given file.

eg.

```bash
cat my_file.txt
```

To show the contents of `my_file.txt`.

### `nano`

A helpful little text editor.

Use Ctrl+X to quit!

eg.

```bash
nano my_file.txt
```

To edit `my_file.txt`.

### `grep`

Search within the file contents.

eg.

```bash
grep toby my_file.txt
```

This example will find all lines in `my_file.txt` containing the word `toby`.

This is really good for finding things in program logs!

### `su`

Change user.

eg.

```bash
su doctor_strange
```

Try to change to the user 'doctor strange'

### `sudo`

Perform commands which need elevated privileges!

eg.

```bash
sudo apt install blender
```

Will install blender (on Debian and Ubuntu).

## Options

Lot's of executable programs in bash (and other terminals) will take options which are prepended by a `-` or `--`. These are useful if you want programs to do slightly different things that the designers of the program have added to them. In order to see what options a program will take, you can always use [`man`](#man)

### Long Options

eg. `--all`, these options are written out as English words and are very readable, but may require a lot of typing.

### Short Options

eg. `-a`, these options are quick and easy to type, but remembering what they are can be a bit tricky sometimes. However, a nice feature is that you can list a bunch of them together. Eg. `-la` means, "Do option `-a` AND option `l`". However,
this is by convention, and some programs will require options to be separate parameters, even in short form.

## Helpful Shortcuts

### Ctrl+C

Close the current program!

Alternatives are Ctrl+D, Ctrl+Z, quit(), and exit()! Unfortunately, what will work varies by program. :'(

### Ctrl+Shift+C

Copy the selected piece of text!

### Ctrl+Shift+V

Paste the piece of text in the clipboard!

### 'Up'

Choose a recent command.

### 'Tab'

Autocomplete what you currently have.


## Useful Places to know

- `/etc` (system configuration files)

- `/tmp` (temporary storage area)

- `/home` (home directories)

- `/usr/bin` (most programs live here)


## Pipes and redirection

Lots of programs read things in from something known as the "standard input". Furthermore, many programs will give output to something known as the "standard output" or "standard error", which in the most common case will be your shell.

However, you can chain programs together, by "piping" their outputs to the inputs of other programs. (Imagine trying to do this with graphical programs!)

Here are some of the operators you can use for piping:

### `|`

The most common one - this operator will take the output of the command to the left of it, and feed it to the input of the command to its right.

eg.

```bash
cat my_file.txt | grep hello | grep goodbye
```

This examples will cause the output of `cat my_file.txt` to flow to the input of `grep hello` whos output will go to `grep goodbye`. The effect of this is that we will see ever line in the file `my_file.txt` that has both `hello` and `goodbye` in it.

### `>`

Write the standard output of the command on the left to the file on the right.

### `>>`

Append the standard output of the command on the left to the file in the right.

### `<`

Send the contents of the file on the right to the input of the command on the left.


## Wargames

Go to [http://overthewire.org/wargames/bandit/](http://overthewire.org/wargames/bandit/)
Level 0:
ssh bandit0@bandit.labs.overthewire.org
(password: bandit0)

For practice, have a look there!

## Further Reading

What is covered here is exceptionally brief, please look here for some of the topics mentioned briefly in the presentation which weren't elaborated on!

- [What is Bash shell scripting?](https://en.wikibooks.org/wiki/Bash_Shell_Scripting)

- [Introduction to Package Managers](https://www.linode.com/docs/tools-reference/linux-package-management)

- [What are Linux permissions?](https://ryanstutorials.net/linuxtutorial/permissions.php)

- [What is the standard input and the standard output?](http://www.linfo.org/stdio.html)

-