# Vibrant (Dark) Clear Theme
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

   Can be hard to see - see card alterations below

> Feel free to leave any feedback [here](https://github.com/myleskeeffe/clear-theme-dark/issues).

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

   This was made to work with my solar system - so the color_threshold and other will likely be off (and there's probably a better way to do one solid colour like this, I originally had multiple colours in it - but reverted to one and was too lazy to search for the better way).
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
