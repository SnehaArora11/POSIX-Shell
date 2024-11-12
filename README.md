# Interactive POSIX Shell

This repository contains the implementation of an interactive POSIX-compatible shell. The project showcases process management, input parsing, and system-level functionality with various built-in commands and features.

## Features

- **Command Execution**: Executes both built-in and external commands.
- **Piping and Redirection**: Supports pipes (`|`) and I/O redirection (`<`, `>`).
- **Job Control**: Handles foreground and background processes (`&`).
- **History Management**: Maintains a command history (up to 20 commands) across sessions.
- **Signal Handling**: Processes interrupts like `Ctrl+C`, `Ctrl+Z`, and `Ctrl+D`.

## File Descriptions

- **`headers.h`**: Contains all include files, function definitions, and extern variables.
- **`main.cpp`**: Driver code that decides which methods to call.
- **`prompt.cpp`**: Displays the shell prompt.
- **`parse_input.cpp`**: Parses and tokenizes the user input.
- **`cmd_handler.cpp`**: Decides which command to call based on parsed input.
- **`background.cpp`**: Forks and runs processes in the background.
- **`cd.cpp`**: Implements the `cd` command for changing directories.
- **`ls.cpp`**: Implements the `ls` command to list directory contents.
- **`pinfo.cpp`**: Displays process information.
- **`pipe.cpp`**: Manages and executes commands with pipes.
- **`pwd.cpp`**: Implements the `pwd` command to display the current working directory.
- **`redirection.cpp`**: Handles input and output redirection.
- **`search.cpp`**: Recursively searches for a file in the current directory.
- **`sig_handler.cpp`**: Manages signals like `Ctrl+Z`, `Ctrl+C`, and `Ctrl+D`.
- **`makefile`**: Configuration file to compile all `.cpp` files.
- **`history.cpp`**: Implements the `history` command, storing up to 20 commands across sessions in a file.

## Execution

Run the following commands in a terminal (Linux) to compile and execute the shell:

```bash
make
./a.out
```

## Assumptions

- Pipes (`|`) and I/O redirection operators (`<`, `>`) are preceded and succeeded by spaces.
- The user runs the executable (`a.out`) from the directory where it is located.

## Examples

### Running Commands
```bash
> ls -la
> echo "Welcome to the interactive shell"
```

### Background Processes
```bash
> sleep 10 &
```

### Piping and Redirection
```bash
> cat file.txt | grep "keyword"
> ls > output.txt
```

### History Command
```bash
> history
```

### Searching Files
```bash
> search myfile.txt
```

## Project Structure

```
.
├── src/                # Source code files
├── include/            # Header files
├── makefile            # Build system configuration
└── README.md           # Documentation
```

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.
