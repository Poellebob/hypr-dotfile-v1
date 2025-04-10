# Dependenses 
## Arch
### Deps
`sudo pacman -Syu hyprland hyprlock hypridle rofi-wayland kitty otf-commit-mono-nerd`

`yay -S ags-hyprpanel-git pyprland`
### Cosmetic
`yay -S rose-pine-hyprcursor`

`yay -S breezex-cursor-theme`
### Switch to wpa_supplicant (if on IWD)
This is because hyprpanel dussent support *IWD*
```bash
sudo systemctl stop iwd
sudo systemctl disable iwd

sudo pacman -S wpa_supplicant
sudo systemctl enable --now wpa_supplicant

sudo systemctl restart NetworkManager
```
### For extra wifi settings install `nm-connection-editor`
`sudo pacman -Sy nm-connection-editor`

# Installation
```bash
git clone https://github.com/Poellebob/hypr-dotfile-v1.git
cd hypr-dotfile-v1
cp -r * ~/.config/
```
