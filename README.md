# Dimmer Brightness Blueprint

Home Assistant blueprint for controlling a dimmer from zigbee2mqtt

## Description

This blueprint allows you to control light brightness for multiple lights using a dimmer switch. You can select a light from a dropdown input helper and adjust its brightness based on dimmer steps. When pressed and turned it adjusts the brightness of one light element, the Combined Light variable. This way you can turn all the lights on or off. 

---
Currently it is only checked to be working with zigbee2mqtt device [TuYa ERS-10TZBVK-AA](https://www.zigbee2mqtt.io/devices/ERS-10TZBVK-AA.html) (and types seen as). 
** Dont forget to set the dimmer in command mode. ** 
The mqtt event gets checked for payload for brightness_step_up, brightness_step_down, color_temperature_step_up, color_temperature_step_down and toggle. 

### Inputs

- **MQTT Topic**: The MQTT topic to listen to.
- **Input Select Dropdown**: Input select helper entity containing light entity IDs.
- **Combined Light**: The light entity that controls all lights in the dropdown.

### Setup

1. Create an `input_select` entity with the IDs of the lights you want to control.
2. Configure the blueprint with the appropriate MQTT topic, input select entity, and combined light.

### Automation Details

- **Turning the Knob**: Adjusts the brightness of the selected light based on the dimmer step size.
- **Pressing the Button**: Selects a light to dim. The selected light will flash for a second.
- **Turning the Knob and Pressing the Button**: Adjusts the brightness of the combined light variable based on the dimmer step size.