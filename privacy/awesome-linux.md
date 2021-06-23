---
id: 20210328220824
created: 2021-01-19
keywords:
  - awesome
  - linux
  - privacy
---

# Awesome Linux

Id argue that most people could use Linux and wouldn't miss any application at all.
Moreover, I think after using Linux for a while, youll miss it when you use windows.

## What is it

"Linux" is the common core of a group of free and open source (FOSS) operating systems, the most widly known ones are Debian, Ubuntu, RedHat and Suse.
These operating systems come in various flavours: the official ones and so called "distributions".
Those distributions are usually customized for a nicer user experience or a specific usecase.

There are also server variants without a graphical user interface which power most of the internet.

## How to use it

### Pick a Distro

If you just need a disposable, safe enviroment and store your data in clouds like cryptpad, GO FOR [TAILS](https://tails.boum.org).

If you want a permanent solution, I'd recommend [popOS](https://pop.system76.com/) because it
- is updated very fast and regularly by the [company behind it](https://system76.com/about), 
- is [documented](https://support.system76.com/#pop) fairly well, 
- has the option for preinstalled nvidia drivers,
- uses the common ".deb" packaging system + has [flathub packages](https://flathub.org/home) in the appcenter out of the box and 
- utilizes a modern, yet easy to use [gnome](https://www.gnome.org) desktop. 

It also makes it very easy to encrypt your disk during the setup. 

### Install it

1. make a bootable USB stick with [rufus](https://rufus.ie/) or [etcher](https://www.balena.io/etcher/)
2. restart your system, boot from your USB stick in UEFI mode
3. test the system, install it if you like

Tips:

- make a backup or keep your data on a seperate drive
- dont install it on the same disk as windows, unless you want to replace windows
- if you have trouble at any point, use google or youtube

## The Terminal

Don't copy paste commands without looking up what they do. Be especially careful if the involve the words/options " / " (as a path), "root", "rm" or "-r". Dont do shit through "sudo -i", you may fuck up shit badly without any safeguards.

## Workarounds

Because of its open nature, some close source libraries or features may not work out of the box. To fix that its usually enough to do a quick search online.

## Extend Gnome

https://extensions.gnome.org/extension/779/clipboard-indicator/

## Awesome Applications

Pop OS comes with the essentials preinstalled, however there are some nice things Id like to highlight. Most of them are installable via the Pop Shop package manager, unless theres a download link

### Commonly Used

Eolie Browser -
Gnome Photos - [Info](https://wiki.gnome.org/Apps/Photos)

Gnome Password Safe is a pretty neat keepass app, personally I always use bitwarden.

### Creative

- **Pitivi** - A Quick and Easy Video editor - [Info](http://www.pitivi.org/)
- **DaVinci Resolve** - Cut, edit, grade and mix anything - [Info & Download](https://www.blackmagicdesign.com/products/davinciresolve/)
- **Krita** - Digital painting - [Info](https://krita.org/)
- **Blender** - 3d / 2d Modelling and Animation - [Info](https://blender.org/)
