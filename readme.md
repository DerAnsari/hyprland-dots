<div align="center">

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Iosevka&size=64&duration=3000&pause=10000&color=78997A&background=282828&center=true&vCenter=true&width=1000&height=150&lines=Sophos'+Hyprland+Rice..)](https://git.io/typing-svg)

*Classic • Simple • Functional*

</div>

---

**THIS IS NOW ARCHIVED AS I HAVE MOVED ONTO NIXOS AND NOCTALIA AND THUS NO LONGER USE IT**

## **Preview**

<img width="1920" height="1080" alt="screenshot-2025-08-23-131506" src="https://github.com/user-attachments/assets/6a6c7ab1-10cc-4140-8c99-ad24c7d2eab7" />

<img width="1920" height="1080" alt="screenshot-2025-08-23-131050" src="https://github.com/user-attachments/assets/4840022e-a493-4f29-a1bf-5ef569b291a1" />

<img width="1920" height="1080" alt="screenshot-2025-08-23-130855" src="https://github.com/user-attachments/assets/b995ab22-a236-4a86-81a4-20dd1fae7605" />
<img width="1920" height="1080" alt="screenshot-2025-08-23-130251" src="https://github.com/user-attachments/assets/375529b4-ee2b-4325-85aa-7bb1e94c49f8" />
<img width="1920" height="1080" alt="screenshot-2025-08-23-130158" src="https://github.com/user-attachments/assets/1ad806f1-a68d-414a-8e15-d8dbdd03c9ba" />

---

## **What's Included**

This rice features a carefully curated collection of tools and configurations:

### **`./system_monitoring`**
- **btop** - Resource monitor with Gruvbox theming
- **cava** - Audio visualizer for aesthetics
- **fastfetch** - Clean system information display

### **`./window_management`** 
- **hypr** - Hyprland compositor configuration
- **waybar** - Status bar with custom modules
- **wlogout** - Logout menu
- **wofi** - Application launcher

### **`./applications`**
- **kitty** - Terminal emulator with Gruvbox colors
- **spicetify** - Themed Spotify client
- **vesktop** - Discord client with custom styling
- **yazi** - File manager with vim-like keybindings
- **zathura** - PDF viewer

### **`./utilities`**
- **swappy** - Screenshot annotation tool
- **zshrc** - Shell configuration with aliases and theming
- **Wallpaper Switcher** - Shell script that changes the wallpaper 

---

## **Installation**

### **Prerequisites**

**Fonts (Required for proper display):**
```bash
# Install Iosevka Nerd Fonts
yay -S ttf-iosevka-nerd ttf-iosevka-nerd-mono

# Alternative: Download from Nerd Fonts releases
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/Iosevka.zip
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/IosevkaMono.zip
unzip Iosevka.zip -d ~/.local/share/fonts/
unzip IosevkaMono.zip -d ~/.local/share/fonts/
fc-cache -fv
```

**System packages:**
```bash
# Essential packages
sudo pacman -S hyprland waybar kitty wofi zsh

# Additional tools
yay -S btop cava fastfetch spicetify-cli vesktop swappy yazi zathura
```

### **Setup**
```bash
# Clone the repository
git clone https://github.com/DerAnsari/hyprland-dotfiles.git
cd hyprland-dotfiles

# Backup existing configs (optional but recommended)
mkdir -p ~/.config/backup
cp -r ~/.config/{hypr,waybar,kitty,wofi,btop,cava,yazi,zathura} ~/.config/backup/ 2>/dev/null

# Create symlinks
ln -sf $(pwd)/hypr ~/.config/
ln -sf $(pwd)/waybar ~/.config/
ln -sf $(pwd)/kitty ~/.config/
ln -sf $(pwd)/wofi ~/.config/
ln -sf $(pwd)/btop ~/.config/
ln -sf $(pwd)/cava ~/.config/
ln -sf $(pwd)/yazi ~/.config/
ln -sf $(pwd)/zathura ~/.config/
ln -sf $(pwd)/spicetify ~/.config/
ln -sf $(pwd)/vesktop ~/.config/
ln -sf $(pwd)/swappy ~/.config/
ln -sf $(pwd)/wlogout ~/.config/

# Link shell configuration
ln -sf $(pwd)/zshrc ~/.zshrc

# Apply Spicetify theme
spicetify config current_theme gruvbox
spicetify apply
```

### **Post-Installation**
```bash
# Reload shell configuration
source ~/.zshrc

# Restart Hyprland or reboot for full effect
```

---

## **TODO**

### **Upcoming Features (when I feel like it)**
- [ ] **Catppuccin Mocha** color palette for all applications
- [ ] Theme switcher script for easy palette changes  
- [ ] Additional wallpaper collection
- [ ] Custom notification daemon configuration

---

<div align="center">

***Made with blood, sweat and tears... took an entire month***

**Special thanks to [ViegPhunt's config](https://github.com/ViegPhunt/Dotfiles/blob/main/README.md) and [binEpilo's config](https://github.com/binEpilo/hyprland-gruvbox-rice-) for being the inspiration behind this rice**

*Feel free to star ⭐ if you found this useful!*

</div>
