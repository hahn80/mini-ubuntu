1. Install ZSH

    `sudo apt install zsh`

2. Set ZSH as Default Shell:

	`chsh -s $(which zsh)`

3. Download Oh My OZH
    ```
	sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
	```

4. Download pk10k theme:
    
    `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
	
5. Add theme to ~/.zshrc file:

	`ZSH_THEME="powerlevel10k/powerlevel10k"`

6. Logout, restart terminal to install pk10k theme interactions.
