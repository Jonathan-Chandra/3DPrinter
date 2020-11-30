# 3D Printer

***Disclaimer:*** I do not own all of the material included in this repository. 
However, all of the materials or files I've used that are included have been 
credited in this README and are some form of open source or publicly viewable 
with no warranty and provided as is. 
>>>>>>> Stashed changes

## Introduction
This is a repository of all files and notes regarding a 3D printer I assembled.
It contains both information on modifications and firmware files with more to 
come.

**Printer Model:** Anet A8 \
**Print Material:** 1.75 mm PLA

**Settings:** 
<ul>
    <li>200 degrees Celsius hot-end
    <li>60 degrees Celsius Bed lined with 
    blue painter's tape
</ul>

## Why the Anet A8

The Anet A8 is a printer model that is extremely budget friendly at $139 USD at 
the time of creation of this repository (November 2020). It has ample support 
from the community with modifications to increase printing quality and safety. 
It is worth noting though, that safety concerns have been raised by the 
community. At the time of purchase, there was no 3D printer as price 
competitive as the Anet A8. However, presently I would recommend users consider 
looking into the Anet A8 plus, which addresses some of the concerns of the 
quality and safety issues wit hthe Anet A8.

The Anet A8 is a 3D printer *kit* which requires full assembly. From 
start-to-finsh it took me about 4-5 hours of assembly before bed leveling and 
other configurations to create accurate and clean prints. If you're a person 
that enjoys tinkering or learns through physical assembly of objects, then this 
is an ideal kit. If you want a printer that is a *plug and print*, then I would 
not recommend it.

## Known Safety Issues

***Note: This especially applies to older models.***

Anet A8's are well known in the past to be a fire hazard due to a variety of 
deficiencies. It is worth noting that even while spending additional money to 
fix these deficiencies, that the model is still an extremely budget friendly 
printer.

### Underpowered Power Supply Unit

The factory power supply unit is considered to be underpowered for the amount 
of load the printer puts on it. Most people replace it with a compatibly 12V 
30A power supply unit. As of November 2020, they can be found for approximately
$20 USD. 

### Overworked Controller Board and MOSFET

*This is primarily for older models*

The MOSFET's on the Anet A8 are believed to be under-powered. External ones 
that connect to the controller board can be found for $8 USD for two. The 
primary issue is the MOSFET for the hot bed. Some people replace both the 
hot bed and the hot end but it has been debated whether or not this is 
necessary. The new MOSFET's also allow for connection directly to the power 
supply unit. 

### On/Off Switch with Fuse

The factory Anet A8 contains no physical off switch or fuse. One can be 
purchased for about $7 USD. Many PSU shroud plans with an On/Off switch can be 
found on Thingiverse. 

### Thermal Runaway Detection

This is a firmware issue. Thermal runaway detection is a setting such that 
if the thermister somehow gets disloged from the hot end or hot bed, the 
thermometor will be reading a lower temperature than the thermister, causing 
the controller to continuously raise the energy output to the hot end or hot 
bed. A modified version of the firmware will fix this issue as well as allow for 
additional settings and features. 

### Loose Hot Bed Connections

Hot bed connections have been known to come loose. The easiest fix is to solder 
the wires directly to the hot bed itself as opposed to using the hot bed 
connectors that are included. This is a relatively easy fix if you have a 
soldering iron on hand and have soldered before. Otherwise, people have printed 
protection areas to stop any cables or rubbing to improve odds preventing of 
loose wires. Personally, I believe there was no evidence of these issues during 
assembly, but soldered the wires anyways because it was easier to access the 
connection points earlier than later. Connections felt relatively strong though. 

#### Total Costs:
<ul>
    <li> Anet A8: $139
    <li> Upgraded PSU: $20
    <li> MOSFETs: $8
    <li> Power Switch: $7
</ul>

Total: $174 USD

## Octoprint

https://octoprint.org/

Octoprint is installed on a Raspberry Pi 3B that I've already had. Octoprint is 
an operating system that allows prints to be started, stopped, paused, 
monitored, etc. via local network. A camera can be attached to the Pi if desired 
for viewing of actual printer. Octoprint is Open Source.

## Modifications
***These are some modifications I made for increased stability or overall 
printing quality.***
<ol>
    <li>Front Brace: https://www.thingiverse.com/thing:2224643 
</ol>

