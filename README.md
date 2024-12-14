# Custom Linux Shell

This is a custom Linux shell implemented in C, designed by **Arushi Vaidya** and **Aryan Gupta**. It supports basic shell functionalities, including executing system commands, built-in commands, and handling pipes.

---

## Features

- **Execute System Commands**: Run standard Unix commands such as `ls`, `cat`, `pwd`, etc.
- **Built-in Commands**:
  - `cd`: Change the current directory.
  - `help`: Display a help menu with supported commands.
  - `exit`: Exit the shell.
  - `hello`: Greet the current user.
- **Pipe Handling**: Supports commands with pipes (e.g., `ls | grep shell`).
- **Improper Space Handling**: Handles extra spaces in the command input.
- **Command History**: Uses the `readline` library for command-line input and maintains a history of commands.

---

## Prerequisites

1. **GCC**: Install GCC if not already installed.
2. **Readline Library**: Ensure the `readline` library is installed:
   ```bash
   sudo apt-get install libreadline-dev  # On Ubuntu/Debian
   brew install readline                 # On macOS (Homebrew)
   ```

---

## Compilation

To compile the shell program, use the following command:

```bash
gcc shell.c -o shell -lreadline
```

On macOS with Homebrew-installed `readline`, you may need to specify the include and library paths:

```bash
gcc shell.c -I/opt/homebrew/include -L/opt/homebrew/lib -lreadline -o shell
```

---

## Usage

1. Run the shell:

   ```bash
   ./shell
   ```

2. Enter commands in the shell prompt (`>>>`).
   - Example:
     ```bash
     >>> ls
     >>> cd ..
     >>> ls | grep txt
     ```

3. Exit the shell using the `exit` command.

---

## Built-in Commands

| Command   | Description                                                   |
|-----------|---------------------------------------------------------------|
| `cd`      | Change directory (e.g., `cd /path/to/directory`).             |
| `help`    | Display a help menu with supported commands.                  |
| `exit`    | Exit the shell program.                                       |
| `hello`   | Display a personalized greeting to the current user.          |

---

## Pipe Support

The shell supports piping between commands, such as:

```bash
ls | grep shell
```

---

## Files

- **`shell.c`**: The main source code for the shell.

---

## Authors

- **Arushi Vaidya**
- **Aryan Gupta**

---

## License

This project is for educational purposes only. Feel free to use or modify the code for learning and exploration.
