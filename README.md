# iterm2-ohmyzsh-powerlevel10k-fig

![](https://media.giphy.com/media/HzGqcw6PrSRMRB8wqZ/giphy.gif)

By following the steps below and using the configuration provided in the repo, you will have an iterm2 installation that can be opened in any window. Use the "F6" key to toggle at the end of the installation.

# How to install

## Clone this repo


    git clone https://github.com/gulalicelik/iterm2-ohmyzsh-powerlevel10k-fig.git


## Homebrew

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"


## iTerm2

    brew install --cask iterm2

Or, if you do not have homebrew, [Download](http://www.iterm2.com/downloads.html) and install iTerm2

iTerm2 has better color fidelity than the built in Terminal, so your themes will look better.


# Oh My Zsh

More info here: https://github.com/robbyrussell/oh-my-zsh

## Install with curl

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

## Powerlevel10k


    git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k

Then edit your `~/.zshrc` and set `ZSH_THEME="powerlevel10k/powerlevel10k"`. Once you do so, when you start a new terminal session, the Powerlevel10 configure wizard will be launched to set your prompt, beware, there are many many options!

Powerlevel10k offers a whole lot more and is extremely configurable, best is to [check its project page](https://github.com/romkatv/powerlevel10k#extremely-customizable).

If you want to trigger the configuration wizard immediately, simply run `p10k configure` to discover all options, which are plentiful.

## Fig

    brew install --cask fig

Or, if you do not have homebrew, [Download](https://fig.io/) and install Fig

## Change your .plist file

### from terminal
    cd /Users/{{your-user-name}}/Library/Preferences

    mv com.googlecode.iterm2.plist com.googlecode.iterm2.old.plist    // rename your default .plist file

    cp  {{your-repo-directory}}/iterm2-ohmyzsh-powerlevel10k-fig/com.googlecode.iterm2.plist /Users/{{your-user-name}}/Library/Preferences/


### or manually

     Replace the file named com.googlecode.iterm2.plist in the '/Users/{{your-user-name}}/Library/Preferences' directory with the file in the repo

Everything is ok! You will now be able to use iterm2 as it opens in every window. The default toggle key in this configuration is F6.

## Visual Studio Code config

Installing a patched font will mess up the integrated terminal in VS Code unless you use the proper settings. You'll need to go to settings (CMD + ,) and add or edit the following values:

- for Source Code Pro + Font Awesome: `"terminal.integrated.fontFamily": "'SourceCodePro+Powerline+Awesome Regular'"`. The single quotes are important! Restart VS Code after the config change.
- for Source Code Pro: `"terminal.integrated.fontFamily": "Source Code Pro for Powerline"`
- for Meslo: `"terminal.integrated.fontFamily": "Meslo LG M for Powerline"`
- for other fonts you'll need to check the font name in Font Book. You can right click on them on select "Show in Finder" to get the exact name.

You can also set the fontsize e.g.: `"terminal.integrated.fontSize": 14`