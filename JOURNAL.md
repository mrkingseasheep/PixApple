---
title: "PixApple"
author: "Xinyang Wang"
description: "RP2040 Development Board"
created_at: "2025-07-04"
---

# 2025-07-04 - Where to begin (5 hours)

This is a starter project so I can learn how to actually design a keyborad with the RP2040.
So far I've decided on Bluetooth support + battery charging.
I'm tempted to make it waterproof, whatever that means for a development board, so I can stick it in a submarine sometime in the future. Who knows. Maybe.
So far I've done the relatively basic task of setting it up with the power capacitors, pull up resistors and the likes. Only gripe I have right now is reading documentation is a chore.

![Schematic start](img/1.png)

# 2025-07-05 - Adding on functionality (3 hours)

I want CAN. It'll make routing logic/commands/data to and from various parts a lot easier. Only problem is I have no idea what controllers to use. A preliminary search shows that the MCP2515 the CAN controller is a good fit but the transmitter the MCP2551 isn't. MCP2515 can handle +3V3 while MCP2551 needs +5V. So we're ditching MCP2551 for SN65HVD230. Whoever named these needs to be uhhh.... questioned.

Work is slow. So many pages of documentation on documentation. Mainly getting the crystal oscillator and reset pin of all things working. And guess what! My hirearchical sheet was drawn in the wrong grid size because I somehow clicked N by accident. That screws up all the tags and you can't connect to them. Now I have to redraw the sheet. I hate KiCAD sometimes. Why on earth would it let you change grid size if it'll break everything in the schematic??? I'm sleeping now.

![MCP2515 design](img/2.png)
![GRRRRR](img/3.png)
