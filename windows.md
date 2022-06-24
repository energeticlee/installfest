# Windows

For the first portion of the class, we'll be working exclusively inside of the browser. We'll be installing the following tools.

* Slack
* Git
* WSL
* VS Code

If you already have some tools and software installed that are similar to below, it will be more conveient for you to switch over than it will be for you to try to go ahead with your current versions.

## Installation Notes for Windows 10

A 64-bit version of Windows 10 is absolutely needed here as we will be using the Windows Subsystem for Linux \(WSL\) extensively. You can check whether your version of Windows 10 is a 64-bit one by going to `Settings -> System -> About` and looking under the `System type` field.

## Installing the Windows Subsystem for Linux \(WSL\)

[https://docs.microsoft.com/en-us/windows/wsl/install-win10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

* Press the Windows key and search for `Windows features` and select `Turn Windows features on and off`.
* Scroll down and find `Windows Subsystem for Linux` and make sure it's checked, then press OK. Restart the system when prompted to.
* Next, go to the Windows store and search for `Ubuntu` and install it.
* Launch Ubuntu from the start menu. Enter your Linux username and password, and make a note of it \(they are needed later\). Under no circumstances should you leave these blank or cancel the process, as this will run your Linux installation as a root user which causes permission warnings later on and also poses a significant security risk to your system.
  * _Do not forget your Linux password. It is needed for admin operations in the WSL environment._
* _Note: Right-clicking on the WSL window pastes whatever is in your clipboard. This can save you some time when running the longer commands here._

## Symlinking a Windows workspace folder into your WSL home

* **Warning**: Your WSL files are stored in a separate file system managed by WSL with a different, stricter and more fine-grained permission system than Windows. You should _never_ edit any WSL files from Windows itself, as there is a non-trivial risk of corrupting your entire WSL installation. However, editing Windows files from WSL is perfectly fine. Thus, we can integrate the two systems \(WSL and Windows\) by making sure that your working folders live in Windows and are conveniently accessible from WSL.
* Create a `projects` folder from your Windows user account home directory. For example, go to `C:\Users` in Explorer and go into the folder corresponding to your user name. Create a folder named `projects` here. For example, if your home directory is `C:\Users\Bobby Tan`, create the directory `C:\Users\Bobby Tan\projects`. All projects should be created in this folder so that you can safely browse or edit the files from both WSL and Windows.
* Next, symlink it by opening a WSL window and running the following commands in order
  * `cd ~`
  * `ln -s /mnt/c/Users/Bobby\ Tan/projects ./projects`
* From now on, you will be able to access the projects folder in your WSL installation as if it were a directory in it.

## Git

Run the following commands in order in a WSL terminal.

* `sudo apt install git`
* `git config --global credential.helper cache` This will cache your git credentials for a short time after you enter it.
* If you wish to extend the amount of time for which your git credentials are cached, run `nano ~/.gitconfig` and edit the line `helper = cache` to `helper = cache --timeout=86400`. The number after `--timeout=` refers to the cache duration in seconds, so the previous line would cache your credentials for 1 day.

~~https://git-scm.com/download/win~~

## VS Code
We'll be running Visual Studio Code (*not Visual Studio*), as the text editor of choice.

[Download VS code](https://code.visualstudio.com/docs/setup/windows)

Follow Installation instructions only.

Hurray!! You have completed the first part of installation. Move on to installfest.md for the next set of installations.