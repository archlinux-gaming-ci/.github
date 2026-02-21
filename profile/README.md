# Arch Linux Gaming CI Repository

This repository provides automated CI builds for gaming-related Arch Linux packages (Git versions).

The packages are built automatically via GitHub Actions and hosted on GitHub Pages.

## Installation

To add this repository to your system, follow these steps:

### 1. Import and Trust the Repository PGP Key

```bash
curl -sS https://raw.githubusercontent.com/archlinux-gaming-ci/.github/refs/heads/main/repo-public.key | sudo pacman-key --add -
sudo pacman-key --lsign-key DBF8337047E5683F
```

### 2. Add to pacman.conf

Edit your `/etc/pacman.conf` file:

```bash
sudo nano /etc/pacman.conf
```

Add the following lines to the end of the file.

```
[archlinux-gaming-ci]
SigLevel = Required
Server = https://archlinux-gaming-ci.github.io/x86_64
```

### 3. Update Database

Sync your pacman database to pick up the new repository:

```bash
sudo pacman -Sy
```
