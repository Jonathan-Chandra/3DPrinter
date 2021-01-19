# 3D Printer

***Disclaimer:*** I do not own all of the material included in this repository. 
However, all of the materials or files I've used that are included have been 
credited in this README and are some form of open source or publicly viewable 
with no warranty and provided as is. 


***Edit (Jan. 2021):*** Since the purchase of this printer, the Creality Ender 3 has dropped significantly in price for around $200. I would highly consider that over an Anet A8 at this time due to its metal construction and community support.

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
    <li>'Spriya' - High Efficiency Anet A8 Fan Duct: https://www.thingiverse.com/thing:2133328
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
defaults to about 50 mm/s of filament used. At a nozzle diameter of 0.4 mm, 
a radius of 0.2 mm, we have approximately 0.00628 cubic centimeters of PLA 
extruded per second which implies 22.619 cubic centimeters per hour. With a 
density of 1.430 grams per cubic centimeter, we have a extrusion rate of 32.345 
grams per hour. This gives us an extrusion cost of $0.6469 per hour. 

### Total Costs: Less than $0.74/hr 

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

### Summary

As of today, (January 2021), the Anet A8 has lost its competitive edge in my 
personal opinion. With the upgrades I've installed, the printer quickly 
approaches the $200 price. Personally, I would consider the Ender 3 by Creality 
which includes a metal frame, making it more rigid and likely creating a higher 
quality print and a lower failure rate. This is not to say I have 
"buyers remorse". The Anet A8 was a great learning experience and construction 
with low economic risk. However, I wouldn't purchase it again due to what I've 
stated above. Nevertheless, this printer has caused personal interest in FDM 3D 
printers, and in the future, I'll likely build a custom 3D printer with 
personally sourced parts, which will be posted later. 

#### What about print quality?

Well, print quality was *okay*. I think it can suit the needs of some, but not 
many and certainly not 3D printer enthusiasts. In other words, this isn't the 
printer someone should buy as their 2nd printer, or 3rd, etc. Can you get it 
functioning well enough to print figurines or props for cosplay? Yes, especially 
if you plan on sanding and painting your prints, which will hide imperfections. 
Can you get it to print well enough to do gears, bearings, and smaller 
mechanically functioning tools? I doubt it. This printer has issues with 
smaller models. One may argue that I haven't configured the printer well enough 
and this may be true, but I feel that the amount of work and the inconsistent 
results have not made it a viable candidate. In short, you probably will never 
get it to print consistently and as well as, say a Prusa i3, but then again, 
you get what you pay for. 

To a printer enthusiast, the printer quality is probably poor, but there are 
machines that print worse out there, and if you're willing to have patience, 
you can get fair prints. Don't expect it to have good prints right 
after assembly. Especially if you're new to printing, expect to break a part 
here or there. The first time I assembled it, I broke a hot end. Luckily, the 
part was not expensive. Doing so on a name brand hot end would have been 
significantly more. 

#### Buyer Beware!

You need **a lot** of patience and time. Can this turn people away from 3D 
printing? **Absolutely.** If you get easily frustrated, take the extra time to 
budget and save up, and buy a different machine. Not only does it take time to 
build, but it's likely you'll get a lot of failed prints in the beginning. 
Each printer is different and manufacturing of the kit yields inconsistencies 
from product to product. Therefore, there isn't an exact guide on how to 
configure your personal printer. Has this printer turned me away from 3D 
printing? **No.** This being said, I don't plan on using this printer forever, 
and intend to build my own using various sources for design ideas and parts. 
This will also be published on Github on a different repo. 

In the meantime, happy printing!