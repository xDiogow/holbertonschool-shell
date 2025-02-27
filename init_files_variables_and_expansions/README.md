![image](https://github.com/user-attachments/assets/7ab29922-0716-4f3d-bba2-aa1a7ee33171)

# Init Files, Variables and Expansions - Shell Scripting

This directory contains a collection of shell scripts that explore shell initialization files, variable creation and expansion, and basic arithmetic and text transformations. Each exercise helps you understand how to manipulate the shell environment and perform simple computations.

---

## Table of Contents

0. [Alias](#alias)  
1. [Hello you](#hello-you)  
2. [Add /action to PATH](#path)  
3. [Count Directories in PATH](#paths)  
4. [Global Variables](#global-variables)  
5. [Local Variables](#local-variables)  
6. [Create a New Local Variable](#create-local-variable)  
7. [Create a New Global Variable](#create-global-variable)  
8. [True Knowledge Addition](#true-knowledge)  
9. [Divide and Rule](#divide-and-rule)  
10. [Love Exponent Breath](#love-exponent-breath)  
11. [Binary to Decimal](#binary-to-decimal)  
12. [Combinations](#combinations)  
13. [Print Float](#print-float)  
14. [Decimal to Hexadecimal](#decimal-to-hexadecimal)

---

## Alias
**File:** `0-alias`

Create a script that creates an alias named `ls` with the value `rm -f *`.  
After sourcing this script, running `ls` will remove all files in the current directory, so you can still use the original `ls` command by prefixing it with a backslash.

**Example:**
```sh
$ ls
0-alias  file1  file2
$ source ./0-alias
$ ls
# (Current directory is now empty because rm -f * ran)
$ \ls
# (Lists the directory contents using the original ls)
```

---

## Hello you
**File:** `1-hello_you`

Create a script that prints "hello \<user\>", where `<user>` is the current Linux user.

**Example:**
```sh
$ id
uid=1000(julien) gid=1000(julien) groups=...
$ ./1-hello_you
hello julien
```

---

## Add /action to PATH
**File:** `2-path`

Add `/action` as the last directory in the PATH variable.  
After sourcing the script, `/action` should appear at the end of your PATH.

**Example:**
```sh
$ echo $PATH
/home/julien/bin:...:/snap/bin
$ source ./2-path
$ echo $PATH
/home/julien/bin:...:/snap/bin:/action
```

---

## Count Directories in PATH
**File:** `3-paths`

Create a script that counts the number of directories in the PATH variable.  
Empty entries should be counted as directories.

**Example:**
```sh
$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/bin
$ . ./3-paths
3
```

---

## Global Variables
**File:** `4-global_variables`

Write a script that lists all environment (global) variables.

**Example:**
```sh
$ source ./4-global_variables
CC=gcc
CFLAGS=-O2 -fomit-frame-pointer
...
```

---

## Local Variables
**File:** `5-local_variables`

Write a script that lists all local variables, environment variables, and functions.

**Example:**
```sh
$ . ./5-local_variables
BASH=/bin/bash
COLUMNS=133
...
```

---

## Create a New Local Variable
**File:** `6-create_local_variable`

Create a script that creates a new local variable with:  
**Name:** BEST  
**Value:** School

---

## Create a New Global Variable
**File:** `7-create_global_variable`

Create a script that creates a new global variable with:  
**Name:** BEST  
**Value:** School

---

## True Knowledge Addition
**File:** `8-true_knowledge`

Write a script that prints the result of adding 128 to the value stored in the environment variable `TRUEKNOWLEDGE`, followed by a new line.

**Example:**
```sh
$ export TRUEKNOWLEDGE=1209
$ ./8-true_knowledge
1337
```

---

## Divide and Rule
**File:** `9-divide_and_rule`

Write a script that prints the result of dividing the environment variable `POWER` by `DIVIDE`.

**Example:**
```sh
$ export POWER=42784
$ export DIVIDE=32
$ ./9-divide_and_rule
1337
```

---

## Love Exponent Breath
**File:** `10-love_exponent_breath`

Write a script that prints the result of raising the environment variable `BREATH` to the power of `LOVE`, followed by a new line.

**Example:**
```sh
$ export BREATH=4
$ export LOVE=3
$ ./10-love_exponent_breath
64
```

---

## Binary to Decimal
**File:** `11-binary_to_decimal`

Write a script that converts a number from base 2 to base 10.  
The binary number is stored in the environment variable `BINARY`.

**Example:**
```sh
$ export BINARY=10100111001
$ ./11-binary_to_decimal
1337
```

---

## Combinations
**File:** `12-combinations`

Create a script that prints all possible combinations of two lowercase letters (from a to z) except the combination "oo".  
Each combination should be printed on its own line in alphabetical order, starting with "aa".  
*Constraint:* Your script file must contain a maximum of 64 characters.

**Example:**
```sh
$ ./12-combinations | wc -l
675
$ ./12-combinations | tail -10
oi
oj
ok
ol
om
on
op
oq
or
os
```

---

## Print Float
**File:** `13-print_float`

Write a script that prints a number stored in the environment variable `NUM` with two decimal places, followed by a new line.

**Example:**
```sh
$ export NUM=3.14159265359
$ ./13-print_float
3.14
```

---

## Decimal to Hexadecimal
**File:** `14-decimal_to_hexadecimal`

Write a script that converts a number from base 10 to base 16.  
The decimal number is stored in the environment variable `DECIMAL`.

**Example:**
```sh
$ export DECIMAL=1337
$ ./14-decimal_to_hexadecimal
539
```

---

Happy scripting!
