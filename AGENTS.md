# Agent notes

This repo is a published Omarchy theme. `colors.toml` is the single
source of truth: Omarchy regenerates terminal, btop, hyprland, neovim,
vscode, chromium, and shell configs from it via the templates in
`$OMARCHY_PATH/default/themed/`. Do not add generated config files
(`*.lua`, `alacritty.toml`, `foot.ini`, `ghostty.conf`, `kitty.conf`,
`vscode.json`) — `omarchy theme install` strips them from cloned themes.

## Testing changes locally

Copy the repo contents (not the repo itself — a `.git` directory makes
Omarchy treat the theme as cloned and restricted) into the user theme
dir, then re-apply:

```bash
rsync -a --delete --exclude .git ./ ~/.config/omarchy/themes/antique-brass/
omarchy theme set antique-brass
hyprctl configerrors
```

## preview.png

1800x1012 (matches stock themes), produced by staging an empty
workspace with foot+neovim (left), foot+btop (top right), and Nautilus
(bottom right), screenshotting the output with `grim`, and scaling with
`magick -resize 1800x1012!`. Keep personal data out of the shot: run
btop with a config showing only cpu/mem/disks boxes and point Nautilus
at a staged directory, not the real home.
