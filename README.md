# Dimmer Blueprint
Home assistant blueprint for controlling a dimmer

### Description

This blueprint allows you to control light brightness using a dimmer switch. It supports selecting lights from a dropdown input and adjusting their brightness based on dimmer steps.
Some dimmers will need custom logic for the changing the brightness percentage. Currently it triggers on step size change, checks for the action is up or down and adds or subtracts that from, the current brightness.

###  Inputs
- Dimmer Toggle Device: Device that triggers the light selection (button press action).
- Dimmer Step Sensor: On dimmer change (step size)
- Light Selector Input: Input select dropdown helper entity containing light entity IDs. (dropdown)
    
### Setup
- Create an input_select entity with the IDs of the lights you want to control.
- Configure the blueprint with the appropriate devices and entities.

### Automation Details

- Single Click: Cycles through the lights in the dropdown and toggles the selected light.
- Dimming: Adjusts the brightness of the selected light based on the dimmer step size.

### Usage

- Select the dimmer toggle device and step sensor.
- Choose the light selector input and set the dimmer step size.
- Save and activate the automation.

This blueprint simplifies managing multiple lights with a dimmer switch, providing easy configuration and smooth control.
