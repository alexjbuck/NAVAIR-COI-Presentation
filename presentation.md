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

LCDR Alex "Jarvis" Buck

- USNA '11, MIT '13
- MH-60R pilot, Seahawk Weapons & Tactics Instructor
- Mostly based from San Diego, C7F + C5F deployments
- Currently at Carrier Air Wing EIGHT in NAS Oceana

### In the right place at the right time

- HSM Weapons School Pacific & Project Maven
- HSM-49.2 & Artem Sherbinin

# Project Harbinger+Air

Use machine learning to classify acoustic contact in the spectrogram (*gram*) from an SSQ-53 series DIFAR buoy.
![gram](waterfall.png){height=2in}

# Where's the data?

## What happens after a flight

### It gets deleted

Once any immediate debrief is complete, re-format the cards.

### Except ESM... sometimes

The only sensor data collection process in the MH-60R fleet.

Multiple steps for the user:

  - Run a program to parse ESM data
  - Find output in obscure folder
  - Rename output according to specific format
  - Upload output to IntelDocs

# Well that's not great {.unlisted .unnumbered}

# What would we like? {.unlisted .unnumbered}

## Every Byte, Every Flight

- ~20 GB/flight-hour
- ~240 GB/flight-day (12-hour fly day)
- ~36 TB/2-bird detachment (150 fly days)
- ~60 TB/CVN element (20-hour fly day, 150 fly days)

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
- Labelling is hard. 
- Details:
  - ARPDD discriminator data is huge. Nothing uses this data yet.
