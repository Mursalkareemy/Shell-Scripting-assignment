# Shell-Scripting-assignment
## Overview

This assignment includes two projects with several Bash scripts to automate system setup and user management tasks on an Arch Linux system.

### Project 1: System Setup Scripts

This project consists of scripts to:
1. Create a list of packages for installation.
2. Install specified packages.
3. Create symbolic links for configuration files.

### Project 2: User Creation Script

This project includes a script to automate the creation of a new user with specified options for username, shell, and groups.

---

## Project 1: System Setup Scripts 🚀

### Scripts

| Script            | Description                                                                                         |
|-------------------|-----------------------------------------------------------------------------------------------------|
| `list_packages`   | Creates a file named `packages_list.txt` with a list of packages.                                   |
| `install_packages`| Installs the packages listed in `packages_list.txt`.                                                |
| `create_symlinks` | Creates symbolic links for configuration files in the user's home directory.                        |
| `setup`           | Runs `list_packages`, `install_packages`, and `create_symlinks` in sequence.                        |

### Usage

#### `list_packages`
- **Description**: Generates `packages_list.txt` with a list of packages.
- **Command**:
  ```bash
  ./list_packages


## install_packages

- **Description**: Installs the packages listed in `packages_list.txt`.
- **Command**:
  ```bash
  sudo ./install_packages

## create_symlinks

- **Description**: Creates symbolic links for configuration files in the home directory.
- **Command**:
  ```bash
  ./create_symlinks


## setup

- **Description**: Runs all Project 1 scripts in sequence.
- **Command**:
  ```bash
  sudo ./setup

## Project 2: User Creation Script 👤

### Script

- **`add_user`**: Creates a new user with specified options for username, shell, and additional groups.

### Usage

- **Description**: Adds a new user, sets up their home directory, and assigns them to specified groups.

- **Command**:
  ```bash
  sudo ./add_user -u username -s /bin/bash -g "wheel,audio"

### Options

- `-u`: Specify the username.
- `-s`: Specify the shell (default is `/bin/bash` if not specified).
- `-g`: Specify additional groups (comma-separated, no spaces).

### Example Command

To add a user named `exampleuser` with `/bin/bash` as the shell and `wheel,audio` as groups:

```bash
sudo ./add_user -u exampleuser -s /bin/bash -g "wheel,audio"
