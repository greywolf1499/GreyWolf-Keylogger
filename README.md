# GreyWolf Keylogger

GreyWolf is a C-based keylogger for Linux systems. It can capture keystrokes and send them to a file or a remote server. It also includes an exploit server to receive keystrokes from a target machine. This project was developed as part of a System Programming course.

## Features

- Keystroke logging to a local file.
- Keystroke logging to a remote server.
- Exploit server to receive keystrokes from a target.
- Dynamic keyboard device detection.
- Handles special keys like Shift, Ctrl, Alt, etc.
- Signal handling for graceful shutdown.

## How to Compile and Run

The project uses a `makefile` for easy compilation.

To compile, run the `make` command in the project directory:
```bash
make
```

This will create an executable file named `GreyWolf`.

To run the keylogger, execute the following command with superuser privileges:
```bash
sudo ./GreyWolf
```

## Usage

When you run `GreyWolf`, you will be presented with a menu with the following options:

1.  **File**: Log keystrokes to a file. You will be prompted to enter the file path.
2.  **Network**: Log keystrokes to a remote server. You will be prompted to enter the server's IP address.
3.  **Start Exploit Server**: Start a server to listen for incoming connections from a target machine running the keylogger.

## Project Structure

- `GreyWolf.c`: The main file containing the user interface and logic for choosing the output target.
- `keylogger_core.c`: The core keylogging functionality. It captures keystrokes from the keyboard device.
- `keylogger_core.h`: Header file for `keylogger_core.c`.
- `network_setup.c`: Functions for setting up network connections (client and server).
- `network_setup.h`: Header file for `network_setup.c`.
- `makefile`: For compiling the project.
- `README.md`: This file.

## Dependencies

- A C compiler (like GCC).
- `make` utility.
- Linux-based operating system.

## License

This project is unlicensed.
