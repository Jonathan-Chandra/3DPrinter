# 3D Printer

***Disclaimer:*** I do not own all of the material included in this repository. 
However, all of the materials or files I've used that are included have been 
credited in this README and are some form of open source or publicly viewable 
with no warranty and provided as is. 

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

## Cost to Run

### Electricity
With an upgraded power supply unit at 12V 30A, we have 0.36 kW/hr of 
electricity. A high rate of electricity would be $0.25 USD per kW/hr, making the 
cost of operations for electricity $0.09 USD per hour.

### Filament
For the sake of simplicity, we're only going to use PLA filament. As of 
November 2020, PLA filament ranges to as little as $20/kg if you don't care 
about coloring. Of course, some filament quality is better than others. Cura 
defaults to about 50 mm/s of filament used. Based off of PLA density and 
1.75 mm diameter filament, 1 kg of filament is approximately 252.13 meters, with 
a spool weight of about 250 g. We therefore go through about 180 meters of 
filament every hour. Overall, this equates to about $14.28/hr of filament.

Why does this cost look extremely high? Because it is!  $14.28/hr is an upper 
bound of costs. Remember that a printer is not extruding filament 100% of the 
time it is printing. Repositioning takes a significant amount of time on the 
print and furthermore, we can print things with less than 100% infill. 
Therefore, $14.28 is an absolute upper bound of costs. 

### Total Costs: Less than $14.37/hr 

### Is it cost effective?

For personal use, I believe the answer is yes. Printing replacement parts for a 
robotic vacuum or toy will cost cents, whereas buying may cost more due to 
shipping or worse yet, the part is unavailable. Printing will allow you to 
have the part within hours but may require some additional work such as 
creating a model in CAD or sanding and cutting brims, etc. However, there is a 
failure rate of 3D prints, which is especially high when starting. If you manage 
to keep a low failure rate, it may even be a cost effective option for industry.

### Personal Costs

| ***Part***                                                                | ***Cost*** |
|---------------------------------------------------------------------------|------------|
| Anet A8 3D Printer                                                        | $139.00    |
| PSU                                                                       | $20.00     |
| MOSFETs                                                                   | $8.00      |
| Power Switch                                                              | $7.00      |
| Front Brace (Printed for 18 hours with 102g of filament)                  | $3.65      |
| MOSFET mounts (Printed for approximately 40 minutes with 10g of filament) | $0.05      |
| ***Total***                                                               | $177.70    |