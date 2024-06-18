# Dimmer Blueprint
Home assistant blueprint for controlling a dimmer

### Description

This blueprint allows you to control light brightness using a dimmer switch. It supports selecting lights from a dropdown input and adjusting their brightness based on dimmer steps.
Some dimmers will need custom logic for the changing the brightness percentage. Currently it triggers on step size change, checks for the action is up or down and adds or subtracts that from, the current brightness.
I would have like to do this in one blueprint but combining the automations seemed to make thing much more unclear.

## Dimmer Brightness Adjustment Blueprint

### Description
This blueprint adjusts the brightness of a selected light based on the dimmer step size.

### Inputs
- **Dimmer Step Sensor**: Sensor for dimmer step size.
- **Light Selector Input**: Input select entity containing light entity IDs.

### Setup
1. Create an `input_select` entity with the IDs of the lights you want to control.
2. Configure the blueprint with the appropriate sensor and input select entity.

### Automation Details
- **Dimming**: Adjusts the brightness of the selected light based on the dimmer step size.

### Usage
1. Select the dimmer step sensor.
2. Choose the light selector input.
3. Save and activate the automation.

This blueprint provides smooth dimming control for lights based on a dimmer step sensor.


## Dimmer Single Click Control Blueprint

### Description
This blueprint cycles through lights and toggles the selected light on a single click.

### Inputs
- **Click Device**: Device that triggers the light selection (toggle action).
- **Light Selector Input**: Input select entity containing light entity IDs.

### Setup
1. Create an `input_select` entity with the IDs of the lights you want to control.
2. Configure the blueprint with the appropriate click device and input select entity.

### Automation Details
- **Single Click**: Cycles through the lights in the dropdown and toggles the selected light.

### Usage
1. Select the click device.
2. Choose the light selector input.
3. Save and activate the automation.

This blueprint simplifies managing multiple lights with a single click, providing easy configuration and smooth control.