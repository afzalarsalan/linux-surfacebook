# linux-surfacebook
A kernel which strives to be semi-practical for daily use on the Surface Book, no matter the cost (stability included)

## Pacman Repository

Due to a large amount of requests, I've created a pacman repo for those who don't want to build the Linux kernel on a dual core laptop

First you need to run

```
sudo pacman-key --recv-keys 606B8F67F4DAEEE2CD7FD986DF84850438168E49
sudo pacman-key --lsign-key 606B8F67F4DAEEE2CD7FD986DF84850438168E49
```
which will download my signing key from your assigned GPG keyserver and have your system sign it, showing that you trust packages signed by my machine

You will then need to add these lines to your `/etc/pacman.conf` right about `[testing]`.

```
[linux-surfacebook]
SigLevel = Required
Server = https://github.com/afzalarsalan/linux-surfacebook/releases/download/current/
```
It should look similar to below

```
# New lines start here
[linux-surfacebook]
SigLevel = Required
Server = https://github.com/afzalarsalan/linux-surfacebook/releases/download/current/

#[testing]
#Include = /etc/pacman.d/mirrorlist
```

After that, if you already have the packages installed then pacman will update them whenever I update or if you have yet to install them, simply run `pacman -S linux-surfacebook`

Header and Docs are included in the repository for those who need them. 
