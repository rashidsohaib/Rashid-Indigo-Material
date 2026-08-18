# Rashid Indigo Material

A clean, Material Design–inspired **light** theme for Thunderbird in indigo and soft blue tones.

![Theme](bird_PO.png)

## Features

- Light, airy UI (`#FFFFFF` / `#F5F5F5` / `#E8EAF6`) across the main window, folder pane, message list, and calendar
- Indigo accent palette (`#3949AB`, `#283593`, `#1A237E`) for highlights, selection, and hover states
- Themed spaces toolbar (left sidebar) with distinct active/inactive button states
- Styled calendar views: month grid, today/weekend highlighting, task and agenda backgrounds
- Custom message pane styling, including a themed default/initial message background image
- Full icon set included for toolbar, folder, and action icons
- Built using Thunderbird's `theme_experiment` API for deeper styling beyond the standard `theme.colors` surface (folder pane counts, message list header, calendar internals, etc.)

## Compatibility

| | |
|---|---|
| Thunderbird version | 115.0 – 141.* |
| Manifest version | 2 |
| Theme type | `theme_experiment` (static + experimental CSS variables) |
| Color scheme | Light |

## Installation

1. Download the latest `.xpi` file from the [Releases](../../releases) page (or clone this repo and zip the contents).
2. In Thunderbird, go to **Menu → Add-ons and Themes** (or `Ctrl+Shift+A`).
3. Click the gear icon (⚙) and choose **Install Add-on From File...**
4. Select `Rashid-Indigo-Material.xpi`.
5. Enable the theme from the **Themes** tab.

## Building from source

```bash
# From the repository root
zip -r Rashid-Indigo-Material.xpi manifest.json style.css *.png Icons/
```

## Project structure

```
.
├── manifest.json     # Theme manifest & theme_experiment color/property mappings
├── style.css          # Experimental CSS variable stylesheet
├── cheese64.png        # Theme icon
├── bird_PO.png          # Initial/default message pane image
└── Icons/                # Icon set used by the theme
```

## Customization

Colors are defined in two places in `manifest.json`:

- `theme.colors` – standard Thunderbird theme API colors
- `theme_experiment.colors` (mapped to CSS custom properties) – extended styling consumed by `style.css`, covering things like folder pane counts, calendar backgrounds, and message list styling

To create your own variant, fork this repo and adjust the hex values in `manifest.json`, then update `style.css` if you add or rename any CSS variables.

## Related themes

- [Rashid Charcoal Material](../Rashid-Charcoal-Material) – the dark counterpart to this theme

## Author

**Rashid Sohaib**

## License

MIT
