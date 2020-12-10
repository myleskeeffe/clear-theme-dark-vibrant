# Vibrant (Dark) Clear Theme
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)
[![GitHub last commit](https://img.shields.io/github/last-commit/myleskeeffe/clear-theme-dark-vibrant)](https://github.com/myleskeeffe/clear-theme-dark-vibrant)

This is a theme for [Home Assistant](https://www.home-assistant.io/). You can install it [manually](#installation) or via [HACS](https://hacs.xyz/).

## Screenshot
![clear-dark-vibrant](https://user-images.githubusercontent.com/11828103/101709740-01543500-3acb-11eb-9793-178241f5733b.png)

## Installation

1. Copy the folder `themes` into your home-assistant folder
2. Add this under the section `frontend` in your `config.yaml`:
    ```
    frontend:
      themes: !include_dir_merge_named themes
    ```
3. Restart Home Assistant
4. Enable the theme in your user profile (bottom left in Home Assistant)

## Known issues
* [Vacuum Card](https://github.com/denysdovhan/vacuum-card)
** Can be hard to see - see card alterations below

> Feel free to leave any feedback [here](https://github.com/naofireblade/clear-theme-dark/issues).

## Card Alterations
(Ideas/Fixes to help cards match theme)
* Vacuum Card - Use with CardMod
```
style: |
  :host {
    --primary-color: var(--card-background-color);
  }
```
* Mini Graph Card
```
color_thresholds:
  - color: '#25B798'
    value: 1500
entities:
  - <Your Sensor>
hours_to_show: 24
name: <Your Stats>
points_per_hour: 2
type: 'custom:mini-graph-card'
show:
  fill: fade
  labels: false
```


## Attributions
- Background Image based on an image from [visme](https://visme.co/blog/simple-backgrounds/)
