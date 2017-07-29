---
layout: post
title: Getting Started With Spacemacs
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
So let's close out of that with `C-x C-c (Ctrl-x Ctrl-c)` and install spacemacs. If we go to [their website](http://spacemacs.org), you can see that the install string is to run
```shell
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
```
Then start emacs again, and you'll be greeted with something that looks like this.
![]({{site.url}}/assets/getting-started-with-spacemacs/screenshot2.png)
Hit enter a few times and wait for the packages to install. 

![]({{site.url}}/assets/getting-started-with-spacemacs/screenshot3.png)
Once this is done, there's a few things we have to do to get going in ruby. Before that, if you don't know how to navigate around with vim keys, i suggest you take a look at the tutorial by pressing `Spc-h-T` and checking out [The quickstart guide](http://spacemacs.org/doc/QUICK_START.html)

First off, we need to add a few layers. Hit `Spc-f-e-d` to head to your config file and find the line that reads
```elisp
   dotspacemacs-configuration-layers
   '(
     ;; ----------------------------------------------------------------
     ;; Example of useful layers you may want to use right away.
     ;; Uncomment some layer names and press <SPC f e R> (Vim style) or
     ;; <M-m f e R> (Emacs style) to install them.
     ;; ----------------------------------------------------------------
     helm
     ;; auto-completion
     ;; better-defaults
     emacs-lisp
     ;; git
     ;; markdown
     ;; org
     ;; (shell :variables
     ;;        shell-default-height 30
     ;;        shell-default-position 'bottom)
     ;; spell-checking
     ;; syntax-checking
     ;; version-control
     )
```

Edit it like so to add some necessary layers
```diff
   ;; <M-m f e R> (Emacs style) to install them.
   ;; ----------------------------------------------------------------
   helm
-  ;; auto-completion
-  ;; better-defaults
+  auto-completion
+  better-defaults
   emacs-lisp
-  ;; git
+  git
   ;; markdown
   ;; org
-  ;; (shell :variables
-  ;;        shell-default-height 30
-  ;;        shell-default-position 'bottom)
+  ruby
+  ruby-on-rails ;; Skip me if you don't plan on doing rails
+  (shell :variables
+         shell-default-height 30
+         shell-default-position 'bottom)
   ;; spell-checking
-  ;; syntax-checking
+  syntax-checking
   ;; version-control
   )
```
