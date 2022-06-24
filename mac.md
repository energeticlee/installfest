# Mac OSX - 1

For the first portion of the class, we'll be working exclusively inside of the browser. We'll be installing the following tools.

- Slack
- Homebrew
- Git
- Node
- VS Code

If you already have some tools and software installed that are similar to below, it will be more conveient for you to switch over than it will be for you to try to go ahead with your current versions.

## Hidden Files

With a finder window open, set your finder to display hidden unix files by default:

```text
cmd + shift + .
```

## For M1 Macbooks users ONLY

Open up terminal, and paste the following command to install Rosetta 2. Rosetta is a translation process that allows users to run apps that contain x86_64 instructions on Apple silicon. So it's basically to allow you to use apps that are not yet supported by the new mac processors.

```text
softwareupdate --install-rosetta
```

This will launch the rosetta installer and you’ll have to agree to a license agreement, which I’m sure you’ll read completely and thoroughly as we all do every time we install anything on every device.

Now, close the terminal and do as follow:

- Right click your terminal app from Finder
- Select "Get Info"
- Enable "Open using Rosetta"

## Homebrew

Homebrew is a package manager that we will use to install various command line tools in our class.

Open up terminal, and paste the following command to install Homebrew. You might be prompted to install XCode Command Line Tools during the install process.

```text
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

You may be prompted to installed XCode command line tools. When prompted, click and install through that, and you're homebrew installation will continue. You can also install XCode command line tools by running `xcode-select --install` in your terminal.

After the installation process, run the command `brew doctor`. If any warnings or errors are displayed, we will need to resolve them before proceeding with the rest of the install fest.

## Xcode

Speaking of Xcode, install Xcode through the App Store. [Link here](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)

## GIT

Before we do this process, please make sure you have signed up for an account on [Github](http://www.github.com). We will be installing a version of GIT from home brew and also configuring it.

To install GIT

```text
brew install git
```

## Node

To install Nodejs

```text
brew install node
```

#### Configuring GIT

Using your email credentials for GIT, run these commands with your user and email configured.

```text
git config --global user.name "YOUR-USERNAME"
git config --global user.email "YOUR-EMAIL-ADDRESS"
git config --global push.default simple
git config --global credential.helper osxkeychain
```

## VS Code

We'll be running Visual Studio Code (_not Visual Studio_), as the text editor of choice.

[Download VS Code](https://code.visualstudio.com/docs/setup/mac)

Follow Installation instructions and set up Launching from command line.

Hurray!! You have completed the first part of installation. Move on to installfest.md for the next set of installations.
