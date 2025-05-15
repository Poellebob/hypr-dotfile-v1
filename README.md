# Dependenses 
## Arch
### Deps
`sudo pacman -Syu hyprland hyprlock hypridle rofi-wayland kitty otf-commit-mono-nerd swww`

`yay -S ags-hyprpanel-git pyprland`
### Cosmetic
`yay -S rose-pine-hyprcursor`

`yay -S breezex-cursor-theme`
### Switch to wpa_supplicant (if on IWD)
This is because hyprpanel does not support *IWD*
```bash
sudo systemctl stop iwd
sudo systemctl disable iwd

sudo pacman -S wpa_supplicant
sudo systemctl enable --now wpa_supplicant

sudo systemctl restart NetworkManager
```
### Make KDE apps work
```bash
sudo pacman -Sy archlinux-xdg-menu xdg-desktop-portal-hyprland
sudo update-desktop-database
sudo mv /etc/xdg/menus/arch-applications.menu /etc/xdg/menus/applications.menu 
```
### For extra wifi settings install `nm-connection-editor`
`sudo pacman -Sy nm-connection-editor`

### Optional
```bash
 sudo pacman -S --needed wireplumber libgtop bluez bluez-utils btop networkmanager dart-sass wl-clipboard brightnessctl swww python upower pacman-contrib power-profiles-daemon gvfs

yay -S aylurs-gtk-shell
```

# Installation
```bash
git clone https://github.com/Poellebob/hypr-dotfile-v1.git
cd hypr-dotfile-v1
cp -r * ~/.config/
```
# Config
## Wallpaper 
`swww img <path/to/wall>`
This sets the wallpaper permenetly.
You can ofcourse change it by doing the same command
