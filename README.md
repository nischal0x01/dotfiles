
# My Dotfiles

Welcome to my dotfiles repository! This repository contains the configuration files and settings I use to customize my development environment. By storing these files in a version-controlled repository, I can easily replicate my setup across multiple systems.

---

## Requirements

Before proceeding with the installation, ensure that the following tools are installed on your system:

### **Git**
Git is required to clone the dotfiles repository. If Git is not already installed, you can install it using the following command:
```bash
brew install git
```

### **GNU Stow**
GNU Stow is a symlink farm manager that makes it easier to manage and apply configurations. Install it using the command:
```bash
brew install stow
```

---

## Installation

Follow these steps to set up your dotfiles on your system:

### Step 1: Clone the Repository
First, clone this repository into your `$HOME` directory. You can use the following command:
```bash
git clone git@github.com:nischal0x01/dotfiles.git ~/.dotfiles

```

Change into the cloned repository directory:
```bash
cd dotfiles
```

---

### Step 2: Apply Dotfiles Using GNU Stow
GNU Stow will create symbolic links from the files in this repository to their appropriate locations in your home directory. To do this, simply run:
```bash
stow .
```

This command links all configuration files in the repository to the corresponding directories in your `$HOME`.

---

## Repository Structure

This repository is organized to separate configuration files for each application or tool. Below is an example structure:
```
dotfiles/
├── bash/          # Configuration for Bash shell
├── nvim/          # Neovim configuration
├── git/           # Git configuration files
├── zsh/           # Zsh shell configuration
└── tmux/          # Tmux configuration
```

Each directory contains the configuration files specific to that tool. Using `stow`, you can selectively apply configurations for specific tools if needed. For example:
```bash
stow bash  # Apply only the Bash configurations
stow nvim  # Apply only the Neovim configurations
```

---
