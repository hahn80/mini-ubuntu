# Additional packages to set up a clean ubuntu from scratch (minimal server)

## Shell and desktop

```sh
sudo apt install gdm3 gnome-shell gnome-terminal gnome-session
```

## Needed packages:

```sh
sudo apt install network-manager-gnome network-manager-openvpn-gnome network-manager-pptp-gnome network-manager-l2tp-gnome gnome-bluetooth gkbd-capplet switcheroo-control bolt iio-sensor-proxy chrome-gnome-shell gnome-keyring gnome-themes-extra adwaita-qt gnome-control-center gnome-online-accounts gnome-color-manager gnome-user-share gnome-remote-desktop gnome-tweaks seahorse nautilus gnome-calendar gnome-clocks gnome-weather bash-completion gnome-shell-extensions gnome-shell-extension-tool network-manager gnome-menus adwaita-icon-theme-full
```

## Application indicator for gnome:

```sh
sudo apt install gnome-shell-extension-appindicator
```

## Multimedia packages:

```sh
sudo apt install gnome-screenshot gnome-sound-recorder ubuntu-restricted-extras rhythmbox
```

**Notice:** If the login screen missing the cursor icon, it means that you are missing `adwaita-icon-theme-full`.


