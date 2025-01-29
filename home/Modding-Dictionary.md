---
title: Modding Concepts
description: 
published: true
date: 2025-01-29T21:17:31.426Z
tags: 
editor: markdown
dateCreated: 2025-01-23T20:09:58.646Z
---

---

> If you have any questions related to modding, join the [Battalion Wars discord server](https://discord.gg/aPvrTsDARJ)  and we'll be happy to help with anything you might be stuck on.
{.is-info}

---

# General concepts

<details>
<summary>What’s a ".out" file?</summary>
  
Battalion Wars 1 and 2 utilize the **.out** file that defines the geographical data for each level, including the terrain the player interacts with and specifies ground textures. Objects that are not part of the walkable ground are defined separately in the **Level.xml** file.
  
While the file format remains undocumented, it is consistent across both games, as **.out** files from one game function seamlessly in the other—aside from issues with missing textures.
  
<br>  
  
| Battalion Wars 1 | Battalion Wars 2 |
| --- | --- |
| ![screenshot_2025-01-23_200715.png](/screenshot_2025-01-23_200715.png) | ![screenshot_2025-01-23_200249.png](/screenshot_2025-01-23_200249.png) |

</details>

<details>
<summary>What’s a ".pfd" file?</summary>

Battalion Wars 1 utilizes the **.pf2**, though no documentation currently exists for this file. Any information it would be much appreciated.
  
<br>
  
| Battalion Wars 1 |
| --- |
| ![screenshot_2025-01-23_200818.png](/screenshot_2025-01-23_200818.png) |

</details>

<details>
<summary>What’s a ".pf2" file?</summary>
  
Battalion Wars 2 utilizes the **.pf2** file that appears to define level boundaries, facilitate pathfinding, and potentially assist in calculations related to map zones.
  
For more detailed information, check out the [PF2 Documentation](/en/home/Modding-Dictionary/pf2) page to learn more.

<br>
  
| Battalion Wars 2 |
| --- |
| ![screenshot_2025-01-23_200840.png](/screenshot_2025-01-23_200840.png) |
  
</details>

<details>
<summary>What’s a ".res" file?</summary>
  
Battalion Wars 1 and 2 utilize resource files with the **.res** extension to store various assets for each level including models, textures, sounds, animations, effects, and scripts.

Each level has its own dedicated resource file. By default, levels cannot access assets that are not contained within their respective **.res** file.

<br>  
  
| Battalion Wars 1 | Battalion Wars 2 |
| --- | --- |
| ![screenshot_2025-01-23_170837.png](/screenshot_2025-01-23_170837.png) | ![screenshot_2025-01-23_170811.png](/screenshot_2025-01-23_170811.png) |
  
</details>

<details>
<summary>What’s a "Level.xml" file?</summary>
  
Battalion Wars 1 and 2 utilize a **level.xml** for each level that contain all the objects within that level including scenery, units, unit classes, cameras, etc.

<br>  
  
| Battalion Wars 1 | Battalion Wars 2 |
| --- | --- |
| ![screenshot_2025-01-23_193720.png](/screenshot_2025-01-23_193720.png) | ![screenshot_2025-01-23_193656.png](/screenshot_2025-01-23_193656.png) |

</details>

<details>
<summary>What’s a "preload.xml" file?</summary>
  
Battalion Wars 1 and 2 utilize a **preload.xml** for each level that defines general information about the level including its music, certain damage modifiers, memory values, etc.

<br>  
  
| Battalion Wars 1 | Battalion Wars 2 |
| --- | --- |
| ![screenshot_2025-01-23_195629.png](/screenshot_2025-01-23_195629.png) | ![screenshot_2025-01-23_195609.png](/screenshot_2025-01-23_195609.png) |
  
<br>  

---  
  
> **_Damage Armour Bonus object_:** 
Note that **mAlliedDamage/ArmourBonus** and **mEnemyDamage/ArmourBonus** are always set to 1.000000 in all fields in every level in both games. 
{.is-info} 
 
---  
  
In Battalion Wars 1, every level except Tomb of the Unknown Soldiers: ID **1100012909** (TotUS has this table available but uses table ID **2138055993** (below) instead)

<br>  

| Every level except TotUS | | Value |
| --- | --- | --- | 
| mPlayerDamageBonus | = | 1.500000 |
| mPlayerArmourBonus | = | 0.600000 |
| mPlayerRaceDamageBonus | = | 1.200000 |  
| mPlayerRaceArmourBonus | = | 0.700000 |

<br> 
  
| Tomb of the Unknown Soldiers | | Value |
| --- | --- | --- | 
| mPlayerDamageBonus | = | 1.000000 |
| mPlayerArmourBonus | = | 1.000000 |
| mPlayerRaceDamageBonus | = | 1.000000 |  
| mPlayerRaceArmourBonus | = | 1.000000 |  

These define how much damage units either controlled directly by the player **(mPlayerDamage/ArmourBonus)**, commanded by the player **(mPlayerRaceDamage/ArmourBonus)**, assisting the player **(mAlliedDamage/ArmourBonus)**, or opposed by any combination of the other 3 **(mEnemyDamage/ArmourBonus)** deal/take.

---  
  
> In the vanilla games, all of the multipliers for the **Allied** and **Enemy** factions are set to **1.000000**, which is neutral effect. In vanilla **BW2**, these generally decrease over the course of the campaign, making it harder and harder to destroy units or survive attacks as the game goes on.
{.is-info}
  
</details>

<details>
<summary>What’s a ".lua" file?</summary>
  
A **.lua** file is a script written in the Lua programming language, often used for game scripting and configuration. It has a **.lua** extension and is commonly embedded into applications for controlling logic and behaviors.

<br>  
  
| Battalion Wars 1 | Battalion Wars 2 |
| --- | --- |
| ![screenshot_2025-01-23_220407.png](/screenshot_2025-01-23_220407.png) | ![screenshot_2025-01-23_220346.png](/screenshot_2025-01-23_220346.png) |
  
</details>

<details>
<summary>What’s a ".str" file?</summary>
  
Battalion Wars 1 and 2 utilize a **.str** that store **English, French, German, Italian, Japanese, Spanish** and in **Battalion wars 2, British English** text strings used in the game, with each string identified by a unique number.
  
These numbers allow the game engine to reference specific text for dialogues, menus, mission briefings, Unit names, or system messages efficiently.

<br>  
  
| Battalion Wars 1 | Battalion Wars 2 |
| --- | --- |
| ![screenshot_2025-01-23_205827.png](/screenshot_2025-01-23_205827.png) | ![screenshot_2025-01-23_205858.png](/screenshot_2025-01-23_205858.png) |
  
</details>

# [Infantry-XML-Information-and-details](/en/home/Modding-Dictionary/Infantry-XML-Information-and-details)

# Ground vehicle XML Section and detail

- cGroundVehicle
- cGroundVehicleBase
- mUnitInstanceFlags
- mPassenger
- mRevivable

# Air vehicle XML Section and detail

- cAirVehicle
- sAirVehicleBase
- mUnitInstanceFlags
- mPassenger
- mRevivable

# Water vehicle XML Section and detail

- cWaterVehicle
- cWaterVehicleBase
- mUnitInstanceFlags
- mPassenger
- mRevivable

# Model XML Sections and detail

- mpModel
- mpTreadTrackModelLeft
- mpTreadTrackModelRight


# Unit Scripts Sections and detail

- mpScript














---

> Back to [Battalion Wars Home Page](/en/home)
{.is-info}