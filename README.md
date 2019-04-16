![Icon](icon.svg)

[![Latest Version](https://img.shields.io/github/release/rias500/statamic-color-swatches.svg?style=flat-square)](https://github.com/rias500/statamic-color-swatches/releases)
[![Quality Score](https://img.shields.io/scrutinizer/g/rias500/statamic-color-swatches.svg?style=flat-square)](https://scrutinizer-ci.com/g/rias500/statamic-color-swatches)
[![StyleCI](https://styleci.io/repos/117454863/shield)](https://styleci.io/repos/117454863)
[![Total Downloads](https://img.shields.io/packagist/dt/rias/statamic-color-swatches.svg?style=flat-square)](https://packagist.org/packages/rias/statamic-color-swatches)

# Color Swatches plugin for Statamic

Let clients choose from a predefined set of colours.

![Screenshot](./resources/assets/img/color-swatches-screenshot.png)

## Installation

To install the plugin, download the plugin and place it in your `site/addons` folder.

## Color Swatches Overview

Instead of providing a user a full color picker, Color Swatches gives an admin the ability to provide a selection of colors for a user to choose from.

## Using Color Swatches

Add the fieldtype to your fieldset, you can define multiple colors for a swatch by using a YAML array. You can also set a default color by entering the label.

```yaml
sections:
  main:
    display: Main
    fields:
      color:
        type: color_swatches
        colors:
          red: '#E3342F'
          orange: '#F6993F'
          green: '#38C172'
          blue-yellow:
            - '#4299E1'
            - '#ECC94B'
        default: blue
```

## Using Color Swatches

You can access both the label and color in your template.

```twig
{{ color.label }}
{{ color.value }}
{{ color.value[0] }} #If it's more than one color
```

Brought to you by [Rias](https://rias.be)