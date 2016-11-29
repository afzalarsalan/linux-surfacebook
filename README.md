# linux-surfacebook
Arch Linux package to compile the Linux kernel modified for the Surface Book

This is based on the offical Linux kernel package provided by Arch Linux at: https://projects.archlinux.org/svntogit/packages.git/tree/trunk?h=packages/linux.

###Don't expect this to be rock stable, new patches are never rock-stable

##Patches

 - Proper multitouch support for the Surface Book keyboard, allowing two-finger scroll (etc): https://raw.githubusercontent.com/shvr/fedora-surface-pro-3-kernel/master/Add-multitouch-support-for-Microsoft-Type-Cover-3.patch 
 
 - A wifi patch which seems to fix a random kernel crash as a result of the reworked mwifiex driver for late 4.8 & 4.9: https://bugzilla.kernel.org/attachment.cgi?id=245971
 
## Building

You will need to have imported gpg keys for the Linux kernel maintainers:

For Linus Torvalds (the major release key):

	gpg --recv-keys 79BE3E4300411886

For Greg Kroah-Hartman's key (the stable patch release key):

	gpg --recv-keys 38DBBDC86092693E

Then, to build the package, simply run (as usual):

	makepkg
	
## Miscellaneous 
  Try powertop, it's great.
  
  Also use Caffeine or a corresponding applet for your desktop environment because waking up from sleep is a gamble at best.
