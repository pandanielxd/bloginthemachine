---
title: Overland Travel for Tools
excerpt: Combat can be complicated! In this article, we talk about Initiative, finishing off explaining why being first is better than being last.
date: 2024-10-23
last_modified_at: 2024-10-23
permalink: /overland-travel-for-tools/
categories: WWN
tags: Theory Tool
header:
  image: /assets/images/road.webp
---
With the release of the [***Worlds without Number*** System Reference Document](https://www.drivethrurpg.com/en/product/473939/worlds-without-number-system-reference-document), the world was forever changed. Well, maybe I shouldn't go that far, but overland travel was modified to be capped at three miles per hour, which means roads no longer allow people to travel at running speeds for ten hours a day.

Today, we'll quickly go over the Overland Travel rules, and finish up with a tool to calculate the speed of a party, and with that the time needed to traverse a distance. It isn't rocket science, but might be useful for some people nonetheless.
## The Ins and Outs
As I have mentioned, a party can generally travel ten hours a day. The other time is used for rest, making camp, and other activities. The System Reference Document (SRD) mentions the speed for a variety of different terrain types and modifiers, which will also be mentioned a bit later here.

The speeds mentioned assume a party is going from A to B without spending any time scouting areas, or investigating surroundings. It also doesn't matter if you walk, go by cart, or similar.

For a day of travel or a night of camping outdoors, the GM can roll a die for a wandering encounter check. If they roll a 1, some situation arises that requires the PCs attention. If they meet creatures, opposed Wis/Notice checks can be rolled to determine who sees who first. If the PCs win, they can likely find cover before being spotted.

Finally, if the PCs are travelling on their lonesome without some well-stocked travel wagon, the overland exploration rules detail the difficulty and supplies needed.
## Calculate Speed
<div class="terrain-calculator">
  <form id="terrain-form">
    <fieldset>
      <legend><strong>Terrain Type</strong></legend>
      <label>
        Plains or savannas (3 mph)
        <input type="radio" name="terrain" value="3" checked required>
      </label><br>
      <label>
        Light forest or desert (2 mph)
        <input type="radio" name="terrain" value="2">
      </label><br>
      <label>
        Dense forest or rugged hills (1.5 mph)
        <input type="radio" name="terrain" value="1.5">
      </label><br>
      <label>
        Swamp or marsh (1 mph)
        <input type="radio" name="terrain" value="1">
      </label><br>
      <label>
        Mountains or dire wastelands (0.5 mph)
        <input type="radio" name="terrain" value="0.5">
      </label>
    </fieldset>
    <fieldset>
      <legend><strong>Modifiers</strong></legend>
      <label>
        Road through the terrain (x2)*
        <input type="checkbox" name="modifier" value="2">
      </label><br>
      <label>
        Foul weather, mud, or heavy rain (x0.5)
        <input type="checkbox" name="modifier" value="0.5">
      </label><br>
      <label>
        Deep snow on the ground (x0.1)
        <input type="checkbox" name="modifier" value="0.1">
      </label>
    </fieldset>
	<p>* Good roads cannot increase the party’s marching speed above three miles per hour</p>
    <button type="button" onclick="calculateSpeed()">Calculate Speed</button>
  </form>
  Calculated Speed: <strong><span id="speed">3.00</span> mph</strong>
</div>

## Calculate Travel Time
<div class="hex-calculator">
  <form id="hex-form">
    <fieldset>
      <legend><strong>Hex Travel Information</strong></legend>
      <label>
        Miles per Hex:
        <input type="number" id="miles-per-hex" value="6" placeholder="6" required>
      </label><br>
      <label>
        Number of Hexes:
        <input type="number" id="number-of-hexes" value="1" placeholder="1" required>
      </label><br>
    </fieldset>
    <button type="button" onclick="calculateHexTime()">Calculate Time</button>
  </form>
  Total Travel Time: <strong><span id="travel-time">2.00</span> hours</strong>
</div>