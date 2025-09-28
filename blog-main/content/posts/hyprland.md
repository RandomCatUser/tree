---
title: 'Firstly Hyprland.'
description: 'Run a window manager.'
pubDate: 2025-08-27
author: 'Dihan Ramanayaka'
tags: [Linux]
---

# 🛠️ Install & Use a GitHub Config for Hyperland

---

## 1. Install Hyperland & Dependencies

First, make sure you already have Hyperland installed:

```bash
yay -S hyprland waybar rofi alacritty thunar network-manager-applet pipewire pavucontrol
```

---

## 2. Find a GitHub Config

Many Linux users share their Hyperland configs. A few good ones:

* [https://github.com/hyprland-community/awesome-hyprland](https://github.com/hyprland-community/awesome-hyprland) → collection of configs
* Example user config: [https://github.com/prasanthrangan/hyprdots](https://github.com/prasanthrangan/hyprdots) (popular Hyprland rice pack)

---

## 3. Backup Your Current Config

Before replacing anything, backup your defaults:

```bash
mv ~/.config/hypr ~/.config/hypr_backup
mv ~/.config/waybar ~/.config/waybar_backup
mv ~/.config/rofi ~/.config/rofi_backup
```

---

## 4. Clone the GitHub Config

Example with **hyprdots**:

```bash
git clone https://github.com/prasanthrangan/hyprdots.git
cd hyprdots
```

Many repos come with an installer script, e.g.:

```bash
./install.sh
```

If not, just copy configs manually:

```bash
cp -r hypr ~/.config/
cp -r waybar ~/.config/
cp -r rofi ~/.config/
```

---

## 5. Autostart Apps

Most configs already set **Waybar, Rofi, Wallpaper, etc.**
If not, check:

```
~/.config/hypr/hyprland.conf
```

Look for lines like:

```ini
exec-once = waybar &
exec-once = nm-applet &
exec-once = swww init && swww img ~/Pictures/wallpapers/wall.jpg
```

---

## 6. Restart Hyperland

* Logout and re-login to Hyperland, or
* Run:

```bash
hyprctl reload
```

---

## 7. Customize

Once installed, you can:

* Edit **Waybar** at `~/.config/waybar/config`
* Edit **Rofi theme** at `~/.config/rofi/config.rasi`
* Change **wallpapers** in the config

---

✅ Now you have a **ready-made Hyperland desktop** with animations, bar, launcher, and a polished look straight from GitHub.

---

