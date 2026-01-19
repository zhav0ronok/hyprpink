# HyprPink
A cute, pink and minimal hyprland configuration, ideal for notetaking and code!

***

## Basic Configuration

While you can copy the [configuration](https://github.com/zhav0ronok/hyprpink/blob/main/hypr/hyprland.conf) ```hyprland.conf``` in the ```hypr``` folder of this repository, I would strongly suggest modifying the default configuration that came with your installation instead, as it will be better suited to your device and (hopefully) fully up-to-date. 

To do this, navigate to ```~/.config/hypr/hyprland.conf``` in your editor of choice (in my case, I will be using nvim).

**Wallpaper**:

I use hyprpaper to display my wallpaper, and my hyprpaper configuration is [here](https://github.com/zhav0ronok/hyprpink/blob/main/hypr/hyprpaper.conf). You will need to install both hyprpaper and download the wallpapers in [this folder](https://github.com/zhav0ronok/hyprpink/tree/main/Wallpapers). Note that this will only work if the ```path``` to your wallpaper is correct (the one in my ```hyprpaper.conf``` uses *my* username and path, which may be different from yours).

If you want your wallpaper to load on startup, rather than the default wallpaper, you can add the line ```exec-once = hyprpaper``` to your ```hyprland.conf```.

**Pink Window Borders**:

To make the borders for your windows pink, set ```col.active_border = rgb(cb2471)``` and ```col.inactive_border = rgb(cb568c)``` 

***

### kitty

To use my terminal configuration for Kitty, install the Iosevka Nerd Font from [https://www.nerdfonts.com](https://www.nerdfonts.com) (or any Nerd Font, really) and ensure it is in the appropriate fonts folder for your system (otherwise it will not work). 

After that, you can copy my [config](https://github.com/zhav0ronok/hyprpink/blob/main/kitty/kitty.conf) to ```~/.config/kitty/kitty.conf```

If you would not like a transparent-blurred terminal, delete the following lines

```
background_opacity 0.8
background_blur 1
```


***

### fastfetch

To install (arch):

```
sudo pacman -S fastfetch
```

Generate basic config:

```
fastfetch --gen-config
```

To use my configuration, open the default config in your editor of choice and replace the default config.jsonc with mine. 

If you want use a different image for your logo than the one I've included, change the ```source": "~/.config/fastfetch/logo/madoka.png"```, line in ```config.jsonc``` to the path for whichever image you would like to use, and tweak the height, width, padding, etc. accordingly. To use the default logo, change ```"type":``` from ```"kitty-direct"``` to ```"auto"``` and ```"source":``` to ```"arch"```.

NOTE: If the icons for the modules do not properly render on your device, select your own suitable icons for widgets [here](https://emojicombos.com).

***

### waybar

To install (arch):

```
sudo pacman -S waybar
```

This includes two files by default, ```config.jsonc``` and ```style.css```. The modules being displayed are selected in the ```config.jsonc``` and styled in ```style.css```.

If you choose to use the default waybar configuration or make your own, be sure to replace the sway with hyprland in the lines in your config that look like

```
"modules-left": ["hyprland/workspaces"],
```

The modules in this configuration are well suited for a laptop, and so you may want to add/remove a few if you are on a desktop.

NOTE: If the icons for the modules do not properly render on your device, select your own suitable icons for widgets [here](https://emojicombos.com).

***

### firefox

I used the Firefox Color extension to create my [theme](https://color.firefox.com/?theme=XQAAAAL9AAAAAAAAAABBKYhm849SCia2CaaEGccwS-xMDPsquGi2Vq1UiOBYIuIUZ2VlXnqFLy_8UvWe56CNXAdfAHGXwgufEnutiaYNBU9Lq1TAwqUIfdpmrKMV6420cbxGARqBgjaA_ISmpT6FXpews5dj3eJR02RYOl1FLA7cQnWnF1pwQw2khU2zOXUZXhPpCbti8w6RK8Q62iYEv__ZspgA)

Aside from that, you can select one of the wallpapers in the [Wallpapers](https://github.com/zhav0ronok/hyprpink/tree/main/Wallpapers) folder as the background image, and remove various elements such as the weather and popup widgets in the settings.

***

### Obsidian

I will be creating a separate repo for this shortly, so that this theme can be added to the browsable list of community themes within Obsidian, but in the meantime, you can copy my files in that folder and follow the Obsidian documentation to reproduce a good result.
