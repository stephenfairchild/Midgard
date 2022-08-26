# Midgard

The Middle Earth. A home for all of my development system state.

This package installs:
i3, nvim, tmux, dotfiles, Lastpass.

Then it loads my secret keys out of Lastpass and installs them in the correct locations.

## Troubleshooting

Problem: Trying to `sudo pacman -Syu` gives some errors messages about outdated PGP signatures

```
error: <package>: signature from "Someone <mail.of.someone>" is marginal trust
:: File /var/cache/pacman/pkg/<package_name_version>_x86_64.pkg.tar.zst is corrupted (invalid or corrupted package (PGP signature)).
Do you want to delete it? [Y/n] 
```
Solution:
- First update the mirror list by moving some mirrors around to see if this fixes the problem.
- Try Updating the keyring
```
sudo pacman -Sy archlinux-keyring && sudo pacman -Su
```
