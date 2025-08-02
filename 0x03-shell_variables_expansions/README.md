# Shell Variables & Expansions
This directory contains solutions for ALX task 0x03.# 0x03. Shell, init files, variables and expansions

## Overview

This project focuses on shell scripting related to environment variables, local variables, aliases, arithmetic operations, and text processing. You'll learn how to manipulate shell environments, perform calculations using shell variables, and use scripting to accomplish various Linux tasks.

---

## Task Descriptions

### 0. `<o>` - **Alias creation**

Creates a script that defines an alias `ls` which behaves as `rm *`. Used to demonstrate alias manipulation.

### 1. `Hello you`

Prints `hello user`, where `user` is the currently logged-in Linux username. Uses environment variables like `$USER` or command like `whoami`.

### 2. `The path to success is to take massive, determined action`

Appends `/action` to the `PATH` variable, making it the last place the shell looks for executables.

### 3. `If the path be beautiful, let us not ask where it leads`

Counts how many directories are listed in the current `PATH` variable.

### 4. `Global variables`

Displays all environment (global) variables using `printenv` or similar commands.

### 5. `Local variables`

Displays all local variables, environment variables, and defined shell functions.

### 6. `Local variable`

Creates a new local variable `BEST` with the value `School`.

### 7. `Global variable`

Creates a new global environment variable `BEST` with the value `School`.

### 8. `Every addition to true knowledge is an addition to human power`

Prints the sum of `128` and the value stored in environment variable `TRUEKNOWLEDGE`.

### 9. `Divide and rule`

Prints the result of division between the environment variables `POWER` and `DIVIDE`.

### 10. `Love is anterior to life...`

Raises the value of `BREATH` to the power of `LOVE` using shell arithmetic.

### 11. `There are 10 types of people...`

Converts a binary number (base 2) stored in `$BINARY` to a decimal (base 10).

### 12. `Combination`

Prints all combinations of two lowercase letters from `a` to `z`, excluding `oo`. Output is sorted.

### 13. `Floats`

Prints the value of the `NUM` environment variable formatted with two decimal places.

### 14. `Decimal to Hexadecimal`

Converts a base-10 number stored in `$DECIMAL` to hexadecimal (base 16).

### 15. `Everyone is a proponent of strong encryption`

Applies ROT13 encryption to standard input text, encoding and decoding it as a basic cipher.

### 16. `The eggs of the brood need to be an odd number`

Prints every other line from input, starting with the first line, mimicking a filter behavior.

### 17. `I'm an instant star. Just add water and stir.`

Adds two numbers stored in custom base systems using `tr` for base conversion, and prints the result in a third base system called `bestchol`.

---

## Final Note

All scripts are required to be:

* Exactly two lines long (excluding the shebang)
* End with a new line
* Use only allowed shell built-ins and commands (e.g., no `bc`, `awk`, `sed` unless allowed)
* Made executable with `chmod +x`

This project tests foundational shell scripting skills used in automation, DevOps, and systems administration.
