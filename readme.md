
# Custom-card "Light Group"
This is a custom-card to give a count of how many lights in a group are on as well as provide controls for each individual light in the group.

![Light Group](images/example-a.png)
![Light Group with color light](images/example-b.png)

## Credits
Author: PartemImperium - 2022  
Version: 1.0.1

## Changelog
<details>
  <summary>1.0.1</summary>
  Fix issue with a blank space in the controls on larger screen sizes.
</details>
<details>
  <summary>1.0.0</summary>
  Initial release
</details>

## Requirements
This card needs the following to function correctly:

<table>
<tr>
<th>Component / card</th>
<th>required</th>
<th>Note</th>
</tr>
<tr>
<td><a href="https://github.com/thomasloven/lovelace-auto-entities">auto-entities</a></td>
<td>x</td>
<td>Used to create the individual light controls for each light in the group.</td>
</table>

## Usage

### Color On/Forced with slider on individual controls
<pre><code class="language-yaml" style="border: 0">
- type: custom:button-card
  template:
    - "card_light_group_count"
  entity: light.dining_room_lights
  variables:
    ulm_card_light_enable_slider: true
    ulm_card_light_enable_color: true
    ulm_card_light_force_background_color: true
</code></pre>

### Color On/Forced with slider all controls
<pre><code class="language-yaml" style="border: 0">
- type: custom:button-card
  template:
    - "card_light_group_count"
  entity: light.dining_room_lights
  variables:
    ulm_card_light_enable_slider: true
    ulm_card_light_enable_color: true
    ulm_card_light_force_background_color: true
    ulm_custom_card_group_light_enable_slider: true
</code></pre>

## Variables
Variables are passed into the individual light controls (and the group light control). As such any variable for the [native minimalist light control](https://ui-lovelace-minimalist.github.io/UI/usage/cards/card_light/#variables) can be passed to affect the controls. However the "ulm_card_light_enable_slider" variable is overriden to the value of "ulm_custom_card_group_light_enable_slider" on the group control.

<table>
<tr>
<th>Variable</th>
<th>Example</th>
<th>Default Value</th>
<th>Required/ Optional</th>
<th>Explanation</th>
</tr>
<tr>
<td>ulm_custom_card_group_light_enable_slider</td>
<td>true</td>
<td>false</td>
<td>optional</td>
<td>Controls if the group light control should have the slider control. </td>
</tr>
</table>
