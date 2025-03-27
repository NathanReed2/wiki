---
title: PF2 Documentation
description: detailed .pf2 information
published: true
date: 2025-03-27T04:42:48.220Z
tags: 
editor: markdown
dateCreated: 2025-01-27T05:24:23.353Z
---

> If you have any questions related to modding, join the [Battalion Wars discord server](https://discord.gg/aPvrTsDARJ)  and we'll be happy to help with anything you might be stuck on.
{.is-info}

---

# PF2 File Detailed
The Pf2 file, at its core, is an image file consisting of six images. Each image stores data in 6-byte intervals, with each set of 6 bytes representing an individual pixel across all six images. These pixels correspond to specific X and Z coordinates on the in-game 2048x2048 map. Each 6-byte set represents a 4x4 block in the game world.

The first 0x180000 bytes of the file define a **512x512 tile map**, with **6 bytes per tile**. Each byte represents specific attributes or functionality for the corresponding tile:

## Tile Data Structure
1. **First Byte**  
   - **Description**: Matches the `MapZones` object XML attribute `ZONETYPE_NOGOAREA`, with some small exceptions.  
   - **Notes**:  
     - Some areas, like a ravine in 5.4, are exceptions, likely due to specific functionalities (e.g., aircraft-related behavior).  
     - Some XML objects include attributes like `ignore_nogo`.

2. **Second Byte**  
   - **Description**: Matches `MapZones` with the XML attribute `ZONETYPE_FORD`.  
   - **Notes**: Used to identify river crossings.

3. **Third Byte**  
   - **Description**: Represents level boundaries.  
   - **Behavior**:  
     - Changing the value to `0xF0` removes the boundary, allowing players to move into the tile.  
     - Matches XML-defined level boundaries exactly.

4. **Fourth Byte**  
   - **Description**: Possibly unused.  
   - **Notes**: No observed differences across levels.

5. **Fifth Byte**  
   - **Description**: Likely represents ground unit pathfinding.  

6. **Sixth Byte**  
   - **Description**: Likely represents water vehicle pathfinding.

## Purpose
The calculations for these map zones are pre-processed in this file for faster performance. However, to enable events (e.g., scripting specific to a zone), the `MapZones` objects are still included in the levels. These objects provide unique IDs to associate with events or scripting triggers.

--- 

> Back to [Modding-Concepts](/home/Modding-Concepts)
{.is-info}

> Back to [Battalion Wars Home Page](/en/home)
{.is-info}