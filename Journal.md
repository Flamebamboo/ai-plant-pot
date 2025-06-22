---
title: "PixPlanter"
author: "Flamebamboo"
description: "smart planter with cute expressions! it has soil reading, surrounding temperature, motion, ambient light sensors that displays on a OLED screen! "
created_at: "2025-06-20"
---

# June 20th: Gettin started with research

The first thing was asking a nerd friend who could give me some pointers how to get started on this project. This is my first custom project and I literally have no experience with electronics except making a MacroPad with a guide at hand. So the first thing I asked him was what parts I will be needing and he told me to do some research first on what features I will be needing for the planter. I moved on looking at some other commercial smart planter and this one is really cool called Ivy, it has temperature, soil moisture, ambient light, water level, touch and vibration?!? sensors. But as a noob I decided to keep it simple and cheap. so after some brainstorming I’m going with temperature, soil moisture, light, and motion sensors.

The parts that I’ve looked into are:

- [XIAO ESP32 S3](https://www.aliexpress.com/item/1005007084388623.html)
- [OLED RGB display](https://www.aliexpress.com/item/1005004794240558.html)
- [LIPO Battery 3.7V 2000mAH 103450](https://www.aliexpress.com/item/3256808031709894.html)
- [SHT30 Temperature And Humidity Sensor](https://www.adafruit.com/product/5064)
- [Adafruit STEMMA Soil Sensor - I2C Capacitive Moisture Sensor - JST PH 2mm](https://www.adafruit.com/product/4026)
- [Adafruit BH1750 Light Sensor - STEMMA QT / Qwiic](https://www.adafruit.com/product/4681)

**Estimated Costs (USD):**

- XIAO ESP32 S3: $6.90
- OLED RGB display: $10.10
- LIPO Battery 3.7V 1500mAH 103048: $4.70
- SHT30 Temperature And Humidity Sensor: $8.95
- Adafruit STEMMA Soil Sensor: $7.50
- Adafruit BH1750 Light Sensor: $4.50

My project roadmap ->
![Roadmap](img/notion.png)

I also made some prototype sketches here.
![Prototype Sketch 1](img/features.jpeg)
![Prototype Sketch 2](img/features2.jpeg)
**Total time spent: 5.5h**

# June 21th: Understanding more about the parts + design schematics

I just found out that to charge the battery effectively it will require a battery charger module called TP4056. TP4056 has two different variations with protection IC and without protection. Without protection IC it only protects overcharge, with protection IC it protects overdischarge and over current protection.

I imported the OPL libary for my XIAO ESP32 S3 into KICad and I also added some other pins and batttery module and started wiring for it.. Except I have no clue how to do this....

After some research I found out that the battery can directly connect to XIAO ESP32 from the -BAT and +BAT. I intend to change the ESP32 S3 to C6 since I need an MCU that supports Thread which then allows me to integrate with IOS nicely.

- XIAO ESP32 S3 -> XIAO ESP32 C6 (Thread support )
- LIPO Battery 3.7V 1500mAH 103048 -> LIPO Battery 3.7V 2000mAH (longer battery life)
- SHT30 Temperature And Humidity Sensor -> SHT40 Temperature And Humidity Sensor (apparently better and $2 cheaper)

I have no idea if this is correct or what... 😞
![schematic_1](img/schematic_1.png)

**Total time spent: 3.5h**

# June 22th: Applying footprints

Oh boy... This one was SUPER SUPER confusing for me. I made some changes for the parts to places more "trusted" with well documented parts instead of going to AliExp, the parts like 1.5 inch OLED from waveshare raises the prices abit (hope its okay for Hack Club) because as a beginner who barely have any electronics knowledge I dont understand what schematics symbols to add, what in the world is footprints, and what these parts footprints is. I read the docs aswell as back and fourth chatting with co pilot to assist me making sure that I assigned the correct footprint for each parts.

I hope this is correct ;-;
[footprints](img/footprints.png)

me chatting with copilot for an hour? xD
[chatcopilot](img/chatcopilot.png)
**Total time spent: 2h**
