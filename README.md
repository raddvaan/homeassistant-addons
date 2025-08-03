# Samsung Frame TV Art Changer add-on for Home Assistant

![TV with some art on it ](https://i.imgur.com/BunHdwb.jpeg)


## Installation

Install this addon by adding the repository:

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fradddvaan%2Fhomeassistant-addons)


## Configuration Options

1. **IP Address**: Set the IP address of your Samsung The Frame TV.
2. **Google Art**: Enable to use random images from Google Arts and Culture.
3. **Bing Wallpapers**: Enable to use random high-quality wallpapers from Bing.
4. **High Res**: (For Google Art only) Enable to get high-resolution images using dezoomify.


## Example Automation

Here's an example of how to set up an automation to change the image daily at 23:00:

```yaml
description: "Change Samsung Frame TV Art Daily"
mode: single
trigger:
  - platform: time
    at: "23:00:00"
condition: []
action:
  - service: hassio.addon_start
    data:
      addon: local_hass-frametv-artchanger
```

