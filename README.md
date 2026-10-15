# Custom Desktop Image

This template repository is a starting point for creating custom desktop images based on top of the [vanilla-kde/base](https://github.com/Vanilla-KDE/base-image/pkgs/container/base). It contains a basic recipe to get you started.

> [!TIP]
> It is strongly suggested to check the [Vib documentation](https://docs.vanillaos.org/collections/vib) and [Vanilla-OS/custom-image](https://github.com/Vanilla-OS/custom-image/) to know more about the recipe format, structure of modules and the supported fields.

## Changes required

### Vib

- `includes.container/usr/bin/*`: Scripts for setting up terminal configuration for `apx-vso-native`. Varies depending on your terminal.
- `modules/00-remove-unnecessities.yml`: Remove incompatible pre-installed components. Varies depending on your DE.
- `modules/00-vanilla-backgrounds.yml`: Vanilla Backgrounds. The installation path of wallpapers may vary depending on your DE.
- `modules/99-cleanup.yml`: Be sure to check whether your desktop environment directly or indirectly depends on `sudo`.

### Packages

- Basic packages for your desktop environment
- Wallet/Keyring, `gnome-keyring` is suggested
- A Flatpak backend for your application manager
- A VSO Plugin for your application manager used to visually perform system update
- Input methods (Optional)
