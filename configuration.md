# WIFI

- `iwctl station wlan0 connect "WLAN_NAME"`

# archinstall

## Preparation

- `sudo pacman -Sy`
- `sudo pacman -Sy archlinux-keyring`
- `sudo pacman -Sy archinstall`

## Settings

- Mirrors: United States
- Disk Configuration: Best Practice, Seperate /home
- Bootloader: grub
- Audio: pipewire
- Additional packages: git, curl, wget, neofetch, htop
- Network configuratoin: Network Manager
- Timezone: America/Detroit

(Default for others)

# grub setting

## Before reboot

- `pacman -Sy grub efibootmgr dosfstools mtools`
- `grub-install --target=x86_64-efi --efi-directory=/boot --bootloader-id=GRUB`
- `grub-mkconfig -o /boot/grub/grub.cfg`

## After reboot

- `sudo nano /etc/default/grub` set timeout to 0
- `grub-mkconfig -o /boot/grub/grub.cfg`

# Necessary setups

## yay

- `cd ~/Public`
- `git clone https://aur.archlinux.org/yay.git`
- `cd yay`
- `makepkg -si`

## Fonts

- `sudo pacman -S noto-fonts noto-fonts-cjk noto-fonts-extra noto-fonts-emoji ttf-dejavu ttf-liberation`
- `sudo nano /etc/locale.gen`
- Uncomment `zh_CN.UTF-8 UTF-8`
- `sudo locale-gen`
- `sudo pacman -S nerd-fonts`

# Services

