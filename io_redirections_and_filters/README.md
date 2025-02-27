![image](https://github.com/user-attachments/assets/7ab29922-0716-4f3d-bba2-aa1a7ee33171)

# I/O Redirections and Filters - Shell Scripting

This directory contains a series of shell scripts that explore various aspects of input/output redirections, filtering, and text manipulation in Unix-like systems. The exercises range from printing text and displaying file contents to processing and transforming text and managing files. These tasks help you master essential shell commands and scripting techniques.

---

## Table of Contents

0. [Hello World](#hello-world)  
1. [Confused Smiley](#confused-smiley)  
2. [Let's Display a File](#lets-display-a-file)  
3. [What About 2?](#what-about-2)  
4. [Last Lines of a File](#last-lines-of-a-file)  
5. [First 10 Lines of a File](#first-10-lines-of-a-file)  
6. [Line #2](#line-2)  
7. [Create a Special File](#create-a-special-file)  
8. [Save Current State of Directory](#save-current-state-of-directory)  
9. [Duplicate Last Line](#duplicate-last-line)  
10. [No More JavaScript](#no-more-javascript)  
11. [Count Directories](#count-directories)  
12. [What's New](#whats-new)  
13. [Unique Words](#unique-words)  
14. [Find That Word](#find-that-word)  
15. [Count That Word](#count-that-word)  
16. [What's Next?](#whats-next)  
17. [I Hate Bins](#i-hate-bins)  
18. [Letters Only Please](#letters-only-please)  
19. [A to Z](#a-to-z)  
20. [Without C, You Would Live in Hiago](#without-c-you-would-live-in-hiago)  
21. [esreveR](#esrever)  
22. [DJ Cut Killer](#dj-cut-killer)

---

## Hello World
**File:** `0-hello_world`

Write a script that prints “Hello, World”, followed by a new line to the standard output.

**Example:**
```sh
$ ./0-hello_world
Hello, World
```

---

## Confused Smiley
**File:** `1-confused_smiley`

Write a script that displays a confused smiley:  
```
"(Ôo)'
```

**Example:**
```sh
$ ./1-confused_smiley
"(Ôo)'
```

---

## Let's Display a File
**File:** `2-hellofile`

Display the content of the `/etc/passwd` file.

**Example:**
```sh
$ ./2-hellofile
# (Contents of /etc/passwd)
```

---

## What About 2?
**File:** `3-twofiles`

Display the content of `/etc/passwd` and `/etc/hosts`.

**Example:**
```sh
$ ./3-twofiles
# (Contents of /etc/passwd)
# (Contents of /etc/hosts)
```

---

## Last Lines of a File
**File:** `4-lastlines`

Display the last 10 lines of `/etc/passwd`.

**Example:**
```sh
$ ./4-lastlines
# (Last 10 lines of /etc/passwd)
```

---

## First 10 Lines of a File
**File:** `5-firstlines`

Display the first 10 lines of `/etc/passwd`.

**Example:**
```sh
$ ./5-firstlines
# (First 10 lines of /etc/passwd)
```

---

## Line #2
**File:** `6-third_line`

Display the third line of the file `iacta` located in the working directory.  
*Note:* You’re not allowed to use sed.

**Example:**
```sh
$ ./6-third_line
Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius
```

---

## Create a Special File
**File:** `7-file`

Create a file with the exact name:  
```
*\'"Best School"\'\*$?*****:)
```
that contains the text `Best School` followed by a new line.

**Example:**
```sh
$ ./7-file
$ ls -l
-rw-rw-r-- 1 user user 17 Jan 20 06:40 '*\'"Best School"\'\*$?*****:)'
$ cat -e '*\'"Best School"\'\*$?*****:)'
Best School$
```

---

## Save Current State of Directory
**File:** `8-cwd_state`

Write a script that writes the output of `ls -la` into a file called `ls_cwd_content`.  
If the file exists, it should be overwritten; otherwise, create it.

**Example:**
```sh
$ ./8-cwd_state
$ cat ls_cwd_content
# (Output matching ls -la)
```

---

## Duplicate Last Line
**File:** `9-duplicate_last_line`

Duplicate the last line of the file `iacta` (located in the working directory).

**Example:**
```sh
$ ./9-duplicate_last_line
$ cat iacta
# (Original content with the last line repeated)
```

---

## No More JavaScript
**File:** `10-no_more_js`

Delete all regular files with a `.js` extension in the current directory and all its subdirectories.

**Example:**
```sh
$ ./10-no_more_js
$ ls -lR
# (No .js files present)
```

---

## Count Directories
**File:** `11-directories`

Count the number of directories and sub-directories in the current directory (excluding `.` and `..`).

**Example:**
```sh
$ ./11-directories
3
```

---

## What's New
**File:** `12-newest_files`

Display the 10 newest files in the current directory, one per line, sorted from newest to oldest.

**Example:**
```sh
$ ./12-newest_files
12-newest_files
11-directories
10-no_more_js
...
```

---

## Unique Words
**File:** `13-unique`

Take a list of words from standard input and print only the words that appear exactly once, sorted alphabetically.

**Example:**
```sh
$ cat list | ./13-unique
C
C++
Go
```

---

## Find That Word
**File:** `14-findthatword`

Display lines containing the pattern “root” from the file `/etc/passwd`.

**Example:**
```sh
$ ./14-findthatword
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
...
```

---

## Count That Word
**File:** `15-countthatword`

Display the number of lines that contain the pattern “bin” in `/etc/passwd`.

**Example:**
```sh
$ ./15-countthatword
81
```

---

## What's Next?
**File:** `16-whatsnext`

Display lines containing the pattern “root” and the 3 lines that follow from `/etc/passwd`.

**Example:**
```sh
$ ./16-whatsnext
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico
_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false
_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false
--
_cvmsroot:*:212:212:CVMS Root:/var/empty:/usr/bin/false
...
```

---

## I Hate Bins
**File:** `17-hidethisword`

Display all the lines in `/etc/passwd` that do not contain the pattern “bin”.

**Example:**
```sh
$ ./17-hidethisword
# (All lines from /etc/passwd without "bin")
```

---

## Letters Only Please
**File:** `18-letteronly`

Display all lines of `/etc/ssh/sshd_config` that start with a letter (uppercase or lowercase).

**Example:**
```sh
$ ./18-letteronly
SyslogFacility AUTHPRIV
AuthorizedKeysFile  .ssh/authorized_keys
...
```

---

## A to Z
**File:** `19-AZ`

Replace all characters `A` and `c` from the input with `Z` and `e` respectively.

**Example:**
```sh
$ echo 'Replace all characters `A` and `c` from input to `Z` and `e`.' | ./19-AZ
Replaee all eharaeters `Z` and `e` from input to `Z` and `e`.
```

---

## Without C, You Would Live in Hiago
**File:** `20-hiago`

Remove all letters `c` and `C` from the input.

**Example:**
```sh
$ echo Chicago | ./20-hiago
hiago
```

---

## esreveR
**File:** `21-reverse`

Reverse the input.

**Example:**
```sh
$ echo "Reverse" | ./21-reverse
esreveR
```

---

## DJ Cut Killer
**File:** `22-users_and_homes`

Display all users and their home directories, sorted by username, based on the `/etc/passwd` file.

**Example:**
```sh
$ ./22-users_and_homes
_apt:/nonexistent
avahi-autoipd:/var/lib/avahi-autoipd
avahi:/var/run/avahi-daemon
backup:/var/backups
betty:/home/betty
...
julien:/home/julien
...
```

---

Happy scripting! Enjoy exploring I/O redirections and filters with these exercises.
