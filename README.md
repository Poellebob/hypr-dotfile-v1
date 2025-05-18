![image](https://github.com/user-attachments/assets/b6a5f2bb-609c-49a2-b681-3a4fe2a4cb0c)

# Dependenses 
## Arch
### Deps
```bash
sudo pacman -Syu --needed wireplumber libgtop bluez bluez-utils btop networkmanager dart-sass wl-clipboard brightnessctl swww python upower pacman-contrib power-profiles-daemon gvfs cliphist hyprland hyprlock hypridle rofi-wayland kitty ttf-jetbrains-mono-nerd qt6-wayland qt5-wayland qt5ct grim slurp swappy
```
I recommend also doing `yay -Syu #--noconfirm`
```bash
yay -S pyprland qt6ct-kde
```

**ags-hyprpanel**
***My fork***
My fork makes it posseble to customize all the shourtcuts in the Dashbord.
```bash
sudo pacman -Sy --needed wireplumber libgtop bluez bluez-utils btop networkmanager dart-sass wl-clipboard brightnessctl swww python upower pacman-contrib power-profiles-daemon gvfs wf-recorder meson npm nodejs ninja
```
```bash
yay -Sy --needed aylurs-gtk-shell-git grimblast-git hyprpicker matugen-bin python-gpustat hyprsunset-git #--noconfirm
```
```bash
git clone https://github.com/Poellebob/HyprPanel.git
cd HyprPanel
npm install
meson setup build
meson compile -C build
meson install -C build
```
***Official aur package***
```bash 
yay -S ags-hyprpanel-git
```

### Cosmetic
**Cursors**
```bash
yay -S rose-pine-hyprcursor rose-pine-cursor
```
### Switch to wpa_supplicant (if on IWD)
This is because hyprpanel does not support *IWD* (will still work with KDE and Gnome)
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
### For extra wifi settings
```bash
sudo pacman -Sy nm-connection-editor
```
# Installation
```bash
git clone https://github.com/Poellebob/hypr-dotfile-v1.git
cd hypr-dotfile-v1
cp -r * ~/.config/
```
# Config
## Wallpaper 
```bash
swww img <path/to/wall>
```
This sets the wallpaper permenetly.

You can of course change it by doing the same command.
