
# Custom-card "Light Group"
This is a custom-card to give a count of how many lights in a group are on as well as provide controls for each individual light in the group.

![Light Group](images/example-a.png)
![Light Group with color light](images/example-b.png)

## Credits
Author: PartemImperium - 2022  
Version: 1.0.0  

## Changelog
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

<pre><code class="language-yaml" style="border: 0">
- type: custom:button-card
  template:
    - "card_light_group_count"
  entity: light.dining_room_lights
</code></pre>

<!-- Currently dont use any variables. I plan on eventually passing the vars from lights down but dont currently
## Variables
<table>
<tr>
<th>Variable</th>
<th>Example</th>
<th>Required</th>
<th>Explanation</th>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</table> -->
