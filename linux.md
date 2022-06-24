# Linux

For the first portion of the class, we'll be working exclusively inside of the browser and Node. We'll be installing the following tools.

* Slack
* Git


**TIP:** Use `CTRL+SHIFT+V` to paste into terminal


## GIT

Before we do this process, please make sure you have signed up for an account on [Github](http://www.github.com). We will be installing a version of GIT from home brew and also configuring it.

To install GIT

```text
sudo apt-get install git-all
```

#### Configuring GIT

Using your email credentials for GIT, run these commands with your user and email configured.

```text
git config --global user.name "YOUR-USERNAME"
git config --global user.email "YOUR-EMAIL-ADDRESS"
git config --global push.default simple
git config --global credential.helper cache
```

### Setting up the bash shell

> do you have any other shell configuration files in your home directory? `ls -la ~` If you have something named `.bashrc`, `.bashrc`, `.bash_profile` Take the contents out of this file and put it in the new one we are creating. Then delete the old file.

Create a new shell config file.

```text
touch ~/.bashrc
```

## VSCode

We'll be running **VScode** as our text editor of choice.


If the above does not work, try installing via VScode's website: [https://code.visualstudio.com/download](https://code.visualstudio.com/download) Download the `.deb` file and run it to install.


Hurray!! You have completed the first part of installation. Move on to installfest.md for the next set of installations.
