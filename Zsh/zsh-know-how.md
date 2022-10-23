# ZSH Setup



## Installation

```bash
sudo apt update && \
sudo apt install -y zsh && \
chsh -s $(which zsh) $(whoami)
```



## Customization

**[Oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) installation**

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```



**Fonts setting**

1. ```bash
   git clone https://github.com/deepdev1/Linux-Fonts.git ~/.fonts/
   ```

2. ```bash
   sudo apt install -y gnome-tweaks
   ```

3. Open Tweaks utility => Fonts => Select "MesloLGS NF Regular" font



**[Powerlevel10k theme](https://github.com/romkatv/powerlevel10k)**

1. ```bash
   git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
   ```

2. Update `.zshrc`

   ```bash
   ZSH_THEME="powerlevel10k/powerlevel10k"
   ```

3. Restart terminal session, or run `p10k configure`



**[Zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)**

1. ```bash
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
   ```

2.  Update `.zshrc`

   ```bash
   plugins=(git zsh-autosuggestions)
   ```

3. Restart terminal session, and start typing recent commands



