---
title: Project Harbinger+Air
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
- MH-60R Seahawk Weapons & Tactics Instructor
- Mostly based from San Diego, C7F + C5F deployments
- Currently at Carrier Air Wing EIGHT in NAS Oceana

### In the right place at the right time


# Project Harbinger+Air

Use machine learning to classify acoustic contact in the spectrogram (*gram*) from an SSQ-53 series DIFAR buoy.

![Example Gram Data](waterfall.png)

## Needle in a Haystack

$$SE = SL-RD-NL+DI-PL$$

There are lots of things that make sound in the water other than submarines.

Finding and discriminating subsurface contact from other sources is hard.

Doing so, while managing 4 other sensors is harder.

**Let my sensors monitor themselves when I am not.**



# So, where's the data?

## What happens after a flight

### It gets deleted

Once any immediate debrief or VI is complete, re-format the cards.

### Except ESM... sometimes

Previously the only sensor data collection effort in the MH-60R fleet.^[I am not counting maintenance data/IMDS in this.]

Multiple steps for the aircrew:

  - Run a program to parse ESM data
  - Find output in obscure folder
  - Rename output according to specific format
  - Upload output to IntelDocs

# Well that's not great {.unlisted .unnumbered}

## Every Byte, Every Flight

### Minimize aircrew actions and decisions.
Save everything, build batch processing on the backside.

Build future value for other sensors, e.g. ISAR, FLIR, etc...

### There are lots of bytes
- ~20 GB/flight-hour^[Depends highly on what sensors are being used and recorded. Ranges from 10 to 30 GB/flight-hour.]
- ~240 GB/flight-day (12-hour fly day)
- ~36 TB/2-bird detachment (150 fly days)
- ~60 TB/CVN element (20-hour fly day, 150 fly days)

### Not enough storage
We needed a better simple storage solution.

## Alone with a Snowball

Harbinger+Air uses AWS Secret Commercial Cloud Services.

AWS Snowball Edge migrates up to 80TB into AWS S3. 

Security Manager: "What the *$%! is this?" 
![WTF](wtf.png){height=30%}
![Snowball](snowball.png){height=30%}

<!-- 
Arrives unclassified via UPS

Departs classified via prepaid UPS^[DoD Manual 5200.01 Enclosure 4 paragraph 10d]
-->

## Data Pipeline: The fleet side

![Data Flow](data-flow.png)

## Cronus, the harvester

Tool that:

- Automates the snowball setup
- Minimizes aircrew decisions
- Minimizes aircrew post-flight actions

Its really just a fancy copy/paste operation right now.

Initial version built in 3 weeks. Iterated with users over 4 HARPs throughout 2020 and 2021.

Usage checklist is a single kneeboard sized page.

# Where is the project now?

## Status of Harbinger+Air fleet collections
- Data collection process used on **14** operational deployments and numerous HARP classes.
- Large 10TB hard drives for on-ship cache. Dump to Snowball upon return.
- Testing initial algorithm later this year on P-8A Mighty Orion.
- Roadmap to MH-60R integration is unknown.

# What we learned

- Understand the user workflow
- Minimize what the user needs to learn
- Shipping SECRET material is easier than you might think.
- Long-term snowball rental can be expensive.^[The first 10 days are free. Intended as dump and ship back.]
- Snowballs can fail.
- Labelling is hard. 
- Details:
  - ARPDD discriminator data is huge. Nothing uses this data yet.

## Future Work

- Batch parser so we can automate