## Setting up your Git Bash/ZSH terminals on Windows

1. [Download and install the latest Git for Windows](https://git-scm.com/downloads/win)
2. [Download the latest ZSH package](https://packages.msys2.org/packages/zsh?repo=msys&variant=x86_64)
3. Extract the archive’s file into your Git Bash installation directory: `C:\\Program Files\\Git`
4. Open Git Bash and test the ZSH: `$ zsh`
5. Configure ZSH as default command-line shell:
   
   ```py
    # Create/edit the ~/.bashrc file
    $ notepad ~/.bashrc

    # Add the following content
    if [ -t 1 ]; then
      exec zsh
    fi

    # Save the file and close the Git Bash
   ```

6. Installing oh-my-zsh:
   ```py
     sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```

7. Installing Powerlevel10k:
   ```py
     git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
     echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
   ```
