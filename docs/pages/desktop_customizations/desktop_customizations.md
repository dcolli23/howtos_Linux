---
title: Desktop Customizations
nav_order: 4
has_children: true
---

# Desktop Customizations

This a list of some of the customizations I make with my Ubuntu installations.

These tweaks require GNOME Tweaks which allows for tweaking of the GNOME desktop experience. You can change a lot through this! This can be a bit strange since you have to configure the settings through your browser but you get used to it quickly.

## Using Fingerprint For Sudo

If you have a laptop with a fingerprint scanner, you can configure your work station to ask for your fingerprint for sudo authentication first. To do this, run:

```
sudo pam-auth-update
```

And select the "Fingerprint authentication" option with <kbd>Spacebar</kbd>. Then use <kbd>Tab</kbd> and <kbd>Spacebar</kbd> to exit. This should work immediately but if it doesn't try to reboot.

## Installation of GNOME Tweaks

I use GNOME Tweaks through Chrome. This can be installed with:

```
$ sudo apt install gnome-shell-extensions chrome-gnome-shell
```

You then install the GNOME Shell Integration extension from the chrome web store at [this link](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep/related).

## Handy GNOME Tweaks

### Workspace Matrix

Allows for 2-dimensional workspace layout.

### Multi Monitors Add-On

This allows for the top bar and workspace preview on mutliple external monitors.

### Shell Tiling

See [Shell Tiling](shell_tiling/shell_tiling) page.

