# Mini Shell Project

This project contains multiple implementations of simple shell programs in C, along with utilities and a `Makefile` for building the full-featured shell. The shells demonstrate command execution, piping, redirection, background processes, and basic variable handling.

---

## Files

* **Makefile** – Build instructions for compiling the full-featured shell.
* **key.c** – Utility program for detecting keyboard input and arrow keys.
* **myshell.c** – Full-featured shell implementation using `readline`.
* **shell2.c** – Simple shell with background execution (`&`) and output redirection (`>`).
* **shell3.c** – Shell with support for a single pipe between two commands, background execution, and output redirection.

---

## Build Instructions

Make sure you have `gcc` and the `readline` library installed.

```bash
# Compile the full-featured shell
make
```

This will generate an executable named `myshell`.

To clean compiled files:

```bash
make clean
```

---

## Usage

### myshell (full-featured)

```bash
./myshell
```

Features:

* Execute commands in foreground or background (`&`)
* Support for pipes: `ls | grep txt`
* Output redirection: `>` (overwrite) or `>>` (append)
* Built-in commands: `cd`, `echo $?`, `read`, `prompt=`, `exit`
* Command history and retrieval using `!!`
* Variable assignment and substitution: `$var=value`, `echo $var`
* Simple `if-then-else` conditional execution

### shell2 (basic shell)

```bash
gcc shell2.c -o shell2
./shell2
```

Supports:

* Basic command execution
* Background execution (`&`)
* Output redirection (`>`)

### shell3 (shell with pipes)

```bash
gcc shell3.c -o shell3
./shell3
```

Supports:

* Single pipe between two commands
* Background execution (`&`)
* Output redirection (`>`)

### key.c (keyboard input utility)

```bash
gcc key.c -o key
./key
```

* Detects arrow keys and prints direction
* Prints normal character input with ASCII code
* Useful for testing terminal input handling
