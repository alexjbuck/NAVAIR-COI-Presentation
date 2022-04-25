---
title: Harbinger+Air
subtitle: What I've learned
author:
- Alexander "Jarvis" Buck
theme:
- default
date:
- April 28, 2022
toc: true
toc-title: the overview


---

# Who am I?

### Just some pilot

- LCDR Alex "Jarvis" Buck
- USNA '11, MIT '13
- MH-60R pilot, Seahawk Weapons & Tactics Instructor
- Mostly based from San Diego, C7F + C5F deployments
- Currently at Carrier Air Wing EIGHT in NAS Oceana

### The right place at the right time

- HSM Weapons School Pacific & Project Maven
- No extensive data collection process in the fleet
  - ESM data is the one exception

# Project Harbinger+Air

Use machine learning to classify acoustic contact in the spectrogram (*gram*) from an SSQ-53 series DIFAR buoy.
![gram](waterfall.png){height=2in}

# Where's the data?

## Prior Art: ESM Data Extract

- The only sensor data collection process in the MH-60R fleet.
- Manually intensive for the user. Recent updates vastly improved process to this:
  - Run a program to parse ESM data
  - Find output in obscure folder
  - Rename output according to specific format
  - Upload output to IntelDocs

# That's not great {.unlisted .unnumbered}

## Alone with a Snowball
- Security Manager: "What the *$%! is this?" ![WTF](wtf.png){height=1in}![Snowball](snowball.png){height=1in}
- HARP students: "You want me to do what?"
- Iterate over 4 HARPs throughout 2020 and 2021

## 

# What it is now

## Status of Harbinger+Air fleet collections
- Data collection process used on **14** operational deployments and numerous HARP classes.
- Large 10TB hard drives for on-ship cache. Dump to Snowball upon return.

# What we learned

- Understand the user workflow
- Minimize what the user needs to learn
