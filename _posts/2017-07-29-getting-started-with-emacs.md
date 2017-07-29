---
layout: post
title: Getting started with spacemacs
author: Aria
---

[Spacemacs](http://spacemacs.org) is a pre-made configuration for GNU editor Emacs. It combines the superior editing of vim and the extensibility of emacs into one thing,as well as premade configs for many languages.

Installing Emacs
===================

Depending on your operating system, installing emacs should be quite effortless. On arch linux it's as simple as
```shell
sudo pacman -S emacs
```

Once installed, it'll look pretty terrible.
![]({{site.url}}/assets/getting-started-with-spacemacs/screenshot1.png)
So let's close out of that with C-x C-c and install spacemacs. If we go to [their website](http://spacemacs.org), you can see that the install string is to run
```shell
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
```
Then start emacs again, and you'll be greeted with something that looks like this.
![]({{site.url}}/assets/getting-started-with-spacemacs/screenshot2.png)
Hit enter a few times and wait for the packages to install. 
