# Arch Linux Command Cheat Sheet

## System Management

| Command | Description |
|---------|-------------|
| `uname -a` | Show kernel information |
| `lsb_release -a` | Show distribution info |
| `hostnamectl` | Display host and OS info |
| `uptime` | Show system uptime |
| `neofetch / screenfetch` | Display system info in terminal |

## User Management

| Command | Description |
|---------|-------------|
| `useradd -m -G wheel username` | Add user to sudo group |
| `passwd username` | Set or change user password |
| `usermod -aG group username` | Add user to a group |
| `id username` | Show user ID and groups |
| `groupadd groupname` | Create a new group |

## System Control

| Command | Description |
|---------|-------------|
| `sudo reboot` | Reboot the system |
| `sudo poweroff` | Power off the system |
| `sudo systemctl start service` | Start a systemd service |
| `sudo systemctl stop service` | Stop a systemd service |
| `sudo systemctl enable service` | Enable service at boot |
| `sudo systemctl disable service` | Disable service at boot |
| `sudo systemctl status service` | Check service status |
| `sudo systemctl restart service` | Restart a service |
| `sudo systemctl daemon-reexec` | Reexec systemd |

## Pacman

| Command | Description |
|---------|-------------|
| `sudo pacman -Syu` | Update system |
| `sudo pacman -Syy` | Force refresh package database |
| `sudo pacman -S package` | Install a package |
| `sudo pacman -R package` | Remove a package |
| `sudo pacman -Rs package` | Remove package and deps |
| `sudo pacman -Rns package` | Full remove package |
| `pacman -Ss keyword` | Search packages |
| `pacman -Qs keyword` | Search installed packages |
| `pacman -Si package` | Show package info |
| `pacman -Ql package` | List package files |
| `pacman -Qo /path/to/file` | Find package owning a file |
| `sudo pacman -Sc` | Clean old cache |
| `sudo pacman -Scc` | Clean all cache |
| `sudo pacman -Qdt` | List orphaned packages |
| `sudo pacman -Rns $(pacman -Qdtq)` | Remove orphaned packages |

## Yay

| Command | Description |
|---------|-------------|
| `yay` | Update all packages |
| `yay -Syu` | System update |
| `yay -S package` | Install package |
| `yay -Rns package` | Remove package fully |
| `yay -Ss keyword` | Search for a package |
| `yay -Yc` | Clean orphaned packages |

## Filesystem & Disk

| Command | Description |
|---------|-------------|
| `lsblk` | List block devices |
| `df -h` | Disk usage info |
| `mount / umount` | Mount or unmount devices |
| `fdisk -l` | List partition info |
| `mkfs.ext4 /dev/sdXn` | Format partition as ext4 |

## Networking

| Command | Description |
|---------|-------------|
| `ip a` | Show network interfaces and IPs |
| `ping archlinux.org` | Check internet connectivity |
| `nmcli dev wifi list` | Show WiFi networks |
| `iwctl` | Start interactive iwd WiFi tool |

## Other

| Command | Description |
|---------|-------------|
| `reflector --latest 10 --sort rate --save /etc/pacman.d/mirrorlist` | Update mirrorlist |
| `pacman -Qm` | List AUR packages |
| `pacman -Qn` | List repo packages |
