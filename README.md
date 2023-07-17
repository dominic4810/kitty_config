# Terminal configuration

This repo contains my config files for my terminal setup.
I use the `kitty` terminal emulator.

## External tools

### 1. ranger
Ranger is a file manager in the terminal.

Installation:

```bash
pip install ranger-fm
ranger --copy-config=rc
ranger --copy-config=rifle
```

To enable image previews, the following lines have to be changed in the `rc.conf` file.

```
 73 set preview_images true
119 set preview_images_method kitty
```

To open text files in neovim, change the following line in the `rifle.conf` file

```
 88 mime ^text,  label editor = nvim -- "$@"
```

### 2. timg
timg allows images and videos to be viewed in the terminal, even over ssh.

Installation:

```bash
sudo apt install timg
```

### 3. kitty\_grab
Identical to copy mode in iterm2. Use `ctrl`+`shift`+`c` to enter copy mode.
It should already be installed directly in this repo as a submodule.


### 4. matplotlib-backend-kitty
Plot matplotlib plots directly in the terminal.

Installation:
```bash
pip install matplotlib-backend-kitty
```

Usage:
```python
import matplotlib
matplotlib.use('module://matplotlib-backend-kitty')
```
