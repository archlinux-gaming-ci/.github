# Arch Linux Gaming CI Repository

This repository provides automated CI builds for gaming-related Arch Linux packages (Git versions).

The packages are built automatically via GitHub Actions and hosted on GitHub Pages.

## Installation

To add this repository to your system, follow these steps:

### 1. Add to pacman.conf

Edit your `/etc/pacman.conf` file:

```bash
sudo nano /etc/pacman.conf
```

Add the following lines to the end of the file.

```
[archlinux-gaming-ci]
SigLevel = Optional TrustAll
Server = https://archlinux-gaming-ci.github.io/x86_64
```

### 2. Update Database

Sync your pacman database to pick up the new repository:

```bash
sudo pacman -Sy
```
