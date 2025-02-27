![image](https://github.com/user-attachments/assets/7ab29922-0716-4f3d-bba2-aa1a7ee33171)

# Basics - Shell Scripting

This directory contains a series of shell scripts that perform fundamental operations such as printing the current working directory, listing files in various formats, navigating directories, and manipulating files. These exercises are designed to help you master basic shell commands and scripting techniques.

---

## Table of Contents

1. [Where am I?](#where-am-i)
2. [What’s in there?](#whats-in-there)
3. [There is no place like home](#there-is-no-place-like-home)
4. [The long format](#the-long-format)
5. [Hidden files](#hidden-files)
6. [I love numbers](#i-love-numbers)
7. [Welcome](#welcome)
8. [Betty in my first directory](#betty-in-my-first-directory)
9. [Bye bye Betty](#bye-bye-betty)
10. [Bye bye My first directory](#bye-bye-my-first-directory)
11. [Back to the future](#back-to-the-future)
12. [Lists](#lists)
13. [File type](#file-type)
14. [We are symbols, and inhabit symbols](#we-are-symbols-and-inhabit-symbols)
15. [Copy HTML files](#copy-html-files)
16. [Let’s move](#lets-move)
17. [Clean Emacs](#clean-emacs)
18. [Tree](#tree)

---

## Where am I?
**File:** `0-current_working_directory`

Write a script that prints the absolute path of the current working directory.

**Example:**
```sh
$ ./0-current_working_directory
/basics
$
```

---

## What’s in there?
**File:** `1-listit`

Display the contents list of your current directory.

**Example:**
```sh
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop         Downloads   Library   Music   Public
$
```

---

## There is no place like home
**File:** `2-bring_me_home`

Write a script that changes the working directory to the user’s home directory without using any shell variables.

**Example:**
```sh
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
```

---

## The long format
**File:** `3-listfiles`

Display the current directory contents in a long format.

**Example:**
```sh
$ ./3-listfiles
total 40
-rwxr-xr-x 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x 1 sylvain staff 19 Jan 25 00:23 1-listit
...
```

---

## Hidden files
**File:** `4-listmorefiles`

Display current directory contents, including hidden files (starting with `.`), using the long format.

**Example:**
```sh
$ ./4-listmorefiles
total 48
drwxr-xr-x  6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x  1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
...
```

---

## I love numbers
**File:** `5-listfilesdigitonly`

Display current directory contents in long format with user and group IDs shown numerically and include hidden files.

**Example:**
```sh
$ ./5-listfilesdigitonly
total 56
drwxr-xr-x  6 501 20 204 Jan 25 00:29 .
drwxr-xr-x 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x  1 501 20 18 Jan 25 00:19 0-current_working_directory
...
```

---

## Welcome
**File:** `6-firstdirectory`

Create a script that creates a directory named `my_first_directory` in the `/tmp/` directory.

**Example:**
```sh
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
```

---

## Betty in my first directory
**File:** `7-movethatfile`

Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`.

**Example:**
```sh
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
```

---

## Bye bye Betty
**File:** `8-firstdelete`

Delete the file `betty` from `/tmp/my_first_directory`.

**Example:**
```sh
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
```

---

## Bye bye My first directory
**File:** `9-firstdirdeletion`

Delete the directory `my_first_directory` in `/tmp`.

**Example:**
```sh
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
```

---

## Back to the future
**File:** `10-back`

Write a script that changes the working directory to the previous one.

**Example:**
```sh
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp
```

---

## Lists
**File:** `11-lists`

Write a script that lists all files (including hidden ones) in the current directory, the parent directory, and the `/boot` directory, in long format.

---

## File type
**File:** `12-file_type`

Write a script that prints the type of the file named `iamafile` (which will be located in `/tmp` when the script runs).

**Example:**
```sh
$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, stripped
```

---

## We are symbols, and inhabit symbols
**File:** `13-symbolic_link`

Create a symbolic link to `/bin/ls` named `__ls__` in the current directory.

**Example:**
```sh
$ ./13-symbolic_link
$ ls -la
...
lrwxrwxrwx 1 user user 7 Sep 20 03:24 __ls__ -> /bin/ls
```

---

## Copy HTML files
**File:** `14-copy_html`

Create a script that copies all HTML files from the current directory to the parent directory. Only copy files that either do not exist in the parent or are newer than the ones in the parent. (All HTML files have the extension `.html`.)

---

## Let’s move
**File:** `15-lets_move`

Create a script that moves all files beginning with an uppercase letter to the directory `/tmp/u`.  
_You can assume that `/tmp/u` exists when the script is run._

**Example:**
```sh
$ ./15-lets_move
$ ls -la /tmp/u
# Only files with names beginning with uppercase letters should be moved.
```

---

## Clean Emacs
**File:** `16-clean_emacs`

Create a script that deletes all files in the current directory that end with the character `~`.

**Example:**
```sh
$ ./16-clean_emacs
# Files ending with ~ are removed.
```

---

## Tree
**File:** `17-tree`

Create a script that creates the directories `welcome/`, `welcome/to/`, and `welcome/to/school` in the current directory.  
_Constraint:_ You are allowed to use only two spaces (and lines) in your script.

**Example:**
```sh
$ ./17-tree
$ ls
17-tree  welcome
$ ls welcome/
to
$ ls welcome/to
school
```

---

Happy scripting!
