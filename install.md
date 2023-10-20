---
title: Installing Git
subtitle: \"Committing\" to Git Workshop
author: Michael Connor Buchan
date: 2023-10-20
...

## 🪟 Windows

* Download and install [Git for Windows](https://gitforwindows.org)
* Select “Add a Git Bash profile to Windows Terminal”
* Choose your preferred text editor for writing commit messages
    * This can be anything, but you don't need a fancy editor for commit messages, they're just plain text
* Choose to install git-credential-manager
    * This makes authenticating to Github and other code-forges much easier
* Leave all other options at default unless you know what they mean

##  macOS

I've written a script that will automatically install everything you'll need:

* The [Xcode](https://developer.apple.com/support/xcode/) command-line tools
    * This contains git itself
* The [Homebrew](https://brew.sh) package manager
    * This lets us easily install git-credential-manager
* [git-credential-manager](https://github.com/git-ecosystem/git-credential-manager)
    * This makes authenticating to Github and other code-forges much easier

If you'd like to read the script, you can [view it here](https://lowerelements.club/ussc-git/install-macos.sh)

Open a terminal and run the following command to execute it:

```sh
curl -Ss https://lowerelements.club/ussc-git/install-macos.sh | bash
```

Finally, configure some essential git settings:

```sh
git config --global user.name 'Your Name'
git config --global user.email 'your@email.com'
git config --global core.editor "open --wait-apps --new -e"
```

By default, this will use your default text editor (usually Text Edit) as git's editor. See [git config core.editor
commands](https://git-scm.com/book/en/v2/Appendix-C%3A-Git-Commands-Setup-and-Config#ch_core_editor) if you'd like to
choose another editor

## 🐧 Linux

Install the `git` package with you're system's package manager.

### Debian / Ubuntu & Derivitives

```sh
sudo apt install git
```

### Redhat / Fedora & Derivitives

```sh
sudo dnf install git
```

### Arch & Derivitives

```sh
sudo pacman -S git
```

--------

Finally, configure some essential git settings:

```sh
git config --global user.name 'Your Name'
git config --global user.email 'your@email.com'
git config --global core.editor nano
```

By default, this will use nano as git's editor. See [git config core.editor
commands](https://git-scm.com/book/en/v2/Appendix-C%3A-Git-Commands-Setup-and-Config#ch_core_editor) if you'd like to
choose another editor
