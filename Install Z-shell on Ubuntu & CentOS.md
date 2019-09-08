# Install Z-shell on Ubuntu & CentOS

All the cool kids are using z-shell instead of bash these days. I won’t go into details here, other than saying:

zsh has much better tab completion behavior than bash
it makes working with git much more pleasant and productive
Here’s what you need to do to install zsh, install [Oh-My-Zsh](https://ohmyz.sh/) (a prepackaged bunch of themes and addons) and get the fonts working on `Ubuntu` & `CentOS`

## 1. Install prerequisite packages

>sudo apt install git-core zsh -y

or
> yum install git curl zsh -y

## 2. Install Oh My Zsh

> sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

## 3. Change your shell to zsh

> chsh -s `which zsh`

## 4. Get the “Powerline” fonts required for a fancy theme

> sudo apt install fonts-powerline

or

[other environment](https://github.com/powerline/fonts) 

## 5. Set up a fancy theme

Open up ~/.zshrc and change ZSH_THEME variable:

> vim ~/.zshrc

then change:

> ZSH_THEME="fino"

## Refrensi

- [Oh-My-Zsh](https://ohmyz.sh/)
