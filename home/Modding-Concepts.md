---
title: Modding Concepts
description: 
published: true
date: 2025-01-30T06:25:14.486Z
tags: 
editor: markdown
dateCreated: 2025-01-23T20:09:58.646Z
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
| ![screenshot_2025-01-23_200715.png](/screenshot_2025-01-23_200715.png)  | ![screenshot_2025-01-23_200249.png](/screenshot_2025-01-23_200249.png) |

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
  
For more detailed information, check out the [PF2 Documentation](/en/home/Modding-Concepts/pf2) page to learn more.

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

# [Infantry-XML-Information-and-details](/en/home/Modding-Concepts/Infantry-XML-Information-and-details) 

![s_grunt01.dxt1.4108.0.255.2.93.-1.png](/s_grunt01.dxt1.4108.0.255.2.93.-1.png)![s_antiarm01.dxt1.4108.0.255.2.64.-1.png](/s_antiarm01.dxt1.4108.0.255.2.64.-1.png)![s_hose01.dxt1.4108.0.255.2.72.-1.png](/s_hose01.dxt1.4108.0.255.2.72.-1.png)![s_antiair01.dxt1.4108.0.255.2.66.-1.png](/s_antiair01.dxt1.4108.0.255.2.66.-1.png)![s_parabolic01.dxt1.4108.0.255.2.78.-1.png](/s_parabolic01.dxt1.4108.0.255.2.78.-1.png)![s_hmg01.dxt1.4108.0.255.2.62.-1.png](/s_hmg01.dxt1.4108.0.255.2.62.-1.png)

![wf_grunt01.png](/wf_grunt01.png)![wf_antiarm01.dxt1.4108.0.255.2.54.-1.png](/wf_antiarm01.dxt1.4108.0.255.2.54.-1.png)![wf_hose01.dxt1.4108.0.255.2.60.-1.png](/wf_hose01.dxt1.4108.0.255.2.60.-1.png)![wf_antiair01.dxt1.4108.0.255.2.59.-1.png](/wf_antiair01.dxt1.4108.0.255.2.59.-1.png)![wf_parabolic01.dxt1.4108.0.255.2.82.-1.png](/wf_parabolic01.dxt1.4108.0.255.2.82.-1.png)![wf_hmg01.dxt1.4108.0.255.2.53.-1.png](/wf_hmg01.dxt1.4108.0.255.2.53.-1.png)

![icon_anglogrunt.dxt1.4108.0.255.2.69.-1.png](/icon_anglogrunt.dxt1.4108.0.255.2.69.-1.png)![ai_antiarm01.dxt1.4108.0.255.2.73.-1.png](/ai_antiarm01.dxt1.4108.0.255.2.73.-1.png)![ai_hose01.dxt1.4108.0.255.2.69.-1.png](/ai_hose01.dxt1.4108.0.255.2.69.-1.png)![ai_antiair01.dxt1.4108.0.255.2.68.-1.png](/ai_antiair01.dxt1.4108.0.255.2.68.-1.png)![ai_parabolic01.dxt1.4108.0.255.2.65.-1.png](/ai_parabolic01.dxt1.4108.0.255.2.65.-1.png)![ai_hmg01.dxt1.4108.0.255.2.77.-1.png](/ai_hmg01.dxt1.4108.0.255.2.77.-1.png)

![u_grunt01.dxt1.4108.0.255.2.64.-1.png](/u_grunt01.dxt1.4108.0.255.2.64.-1.png)![u_antiarm01.dxt1.4108.0.255.2.65.-1.png](/u_antiarm01.dxt1.4108.0.255.2.65.-1.png)![u_hose01.dxt1.4108.0.255.2.69.-1.png](/u_hose01.dxt1.4108.0.255.2.69.-1.png)![u_antiair01.dxt1.4108.0.255.2.72.-1.png](/u_antiair01.dxt1.4108.0.255.2.72.-1.png)![u_parabolic01.dxt1.4108.0.255.2.75.-1.png](/u_parabolic01.dxt1.4108.0.255.2.75.-1.png)![u_hmg01.dxt1.4108.0.255.2.74.-1.png](/u_hmg01.dxt1.4108.0.255.2.74.-1.png)

![t_grunt01.dxt1.4108.0.255.2.69.-1.png](/t_grunt01.dxt1.4108.0.255.2.69.-1.png)![t_antiarm01.dxt1.4108.0.255.2.60.-1.png](/t_antiarm01.dxt1.4108.0.255.2.60.-1.png)![t_hose01.dxt1.4108.0.255.2.53.-1.png](/t_hose01.dxt1.4108.0.255.2.53.-1.png)![t_antiair01.dxt1.4108.0.255.2.57.-1.png](/t_antiair01.dxt1.4108.0.255.2.57.-1.png)![t_parabolic01.dxt1.4108.0.255.2.57.-1.png](/t_parabolic01.dxt1.4108.0.255.2.57.-1.png)![t_hmg01.dxt1.4108.0.255.2.58.-1.png](/t_hmg01.dxt1.4108.0.255.2.58.-1.png)

![x_grunt01.dxt1.4108.0.255.2.61.-1.png](/x_grunt01.dxt1.4108.0.255.2.61.-1.png)![x_antiarm01.dxt1.4108.0.255.2.56.-1.png](/x_antiarm01.dxt1.4108.0.255.2.56.-1.png)![x_hose01.dxt1.4108.0.255.2.55.-1.png](/x_hose01.dxt1.4108.0.255.2.55.-1.png)![x_antiair01.dxt1.4108.0.255.2.59.-1.png](/x_antiair01.dxt1.4108.0.255.2.59.-1.png)![x_parabolic01.dxt1.4108.0.255.2.63.-1.png](/x_parabolic01.dxt1.4108.0.255.2.63.-1.png)![x_hmg01.dxt1.4108.0.255.2.60.-1.png](/x_hmg01.dxt1.4108.0.255.2.60.-1.png)

# Ground vehicle XML Section and detail

![s_reco01.dxt1.4108.0.255.2.95.-1.png](/s_reco01.dxt1.4108.0.255.2.95.-1.png)![s_ltnk01.dxt1.4108.0.255.2.17.-1.png](/s_ltnk01.dxt1.4108.0.255.2.17.-1.png)![s_htnk01.dxt1.4108.0.255.2.20.-1.png](/s_htnk01.dxt1.4108.0.255.2.20.-1.png)![s_aa01.dxt1.4108.0.255.2.36.-1.png](/s_aa01.dxt1.4108.0.255.2.36.-1.png)![s_art01.dxt1.4108.0.255.2.17.-1.png](/s_art01.dxt1.4108.0.255.2.17.-1.png)

![wf_reco01.dxt1.4108.0.255.2.20.-1.png](/wf_reco01.dxt1.4108.0.255.2.20.-1.png)![wf_ltnk01.dxt1.4108.0.255.2.21.-1.png](/wf_ltnk01.dxt1.4108.0.255.2.21.-1.png)![wf_htnk01.p8.4108.0.255.2.21.-1.png](/wf_htnk01.p8.4108.0.255.2.21.-1.png)![wf_bsta01.dxt1.4108.0.255.2.22.-1.png](/wf_bsta01.dxt1.4108.0.255.2.22.-1.png)![wf_aa01.dxt1.4108.0.255.2.19.-1.png](/wf_aa01.dxt1.4108.0.255.2.19.-1.png)![wf_art01.dxt1.4108.0.255.2.21.-1.png](/wf_art01.dxt1.4108.0.255.2.21.-1.png)

![ai_ltnk01.dxt1.4108.0.255.2.39.-1.png](/ai_ltnk01.dxt1.4108.0.255.2.39.-1.png)![ai_htnk01.dxt1.4108.0.255.2.36.-1.png](/ai_htnk01.dxt1.4108.0.255.2.36.-1.png)![ai_art01.dxt1.4108.0.255.2.27.-1.png](/ai_art01.dxt1.4108.0.255.2.27.-1.png)

![u_htnk01.dxt1.4108.0.255.2.28.-1.png](/u_htnk01.dxt1.4108.0.255.2.28.-1.png)![u_bsta01.dxt1.4108.0.255.2.27.-1.png](/u_bsta01.dxt1.4108.0.255.2.27.-1.png)![u_art01.dxt1.4108.0.255.2.25.-1.png](/u_art01.dxt1.4108.0.255.2.25.-1.png)

![t_reco01.dxt1.4108.0.255.2.19.-1.png](/t_reco01.dxt1.4108.0.255.2.19.-1.png)![t_ltnk01.dxt1.4108.0.255.2.20.-1.png](/t_ltnk01.dxt1.4108.0.255.2.20.-1.png)![t_htnk01.dxt1.4108.0.255.2.21.-1.png](/t_htnk01.dxt1.4108.0.255.2.21.-1.png)![t_bsta01.dxt1.4108.0.255.2.19.-1.png](/t_bsta01.dxt1.4108.0.255.2.19.-1.png)![t_aa01.dxt1.4108.0.255.2.23.-1.png](/t_aa01.dxt1.4108.0.255.2.23.-1.png)![t_art01.dxt1.4108.0.255.2.21.-1.png](/t_art01.dxt1.4108.0.255.2.21.-1.png)

![x_ltra01.dxt1.4108.0.255.2.32.-1.png](/x_ltra01.dxt1.4108.0.255.2.32.-1.png)![x_ltnk01.dxt1.4108.0.255.2.22.-1.png](/x_ltnk01.dxt1.4108.0.255.2.22.-1.png)![x_htnk01.dxt1.4108.0.255.2.24.-1.png](/x_htnk01.dxt1.4108.0.255.2.24.-1.png)![x_bsta01.dxt1.4108.0.255.2.30.-1.png](/x_bsta01.dxt1.4108.0.255.2.30.-1.png)![x_aa01.dxt1.4108.0.255.2.20.-1.png](/x_aa01.dxt1.4108.0.255.2.20.-1.png)![x_art01.dxt1.4108.0.255.2.76.-1.png](/x_art01.dxt1.4108.0.255.2.76.-1.png)

# Air vehicle XML Section and detail

![s_gshp01.dxt1.4108.0.255.2.15.-1.png](/s_gshp01.dxt1.4108.0.255.2.15.-1.png)![s_ftr01.dxt1.4108.0.255.2.24.-1.png](/s_ftr01.dxt1.4108.0.255.2.24.-1.png)![s_tpt01.dxt1.4108.0.255.2.18.-1.png](/s_tpt01.dxt1.4108.0.255.2.18.-1.png)

![wf_gshp01.dxt1.4108.0.255.2.19.-1.png](/wf_gshp01.dxt1.4108.0.255.2.19.-1.png)![wf_ftr01.dxt1.4108.0.255.2.20.-1.png](/wf_ftr01.dxt1.4108.0.255.2.20.-1.png)![wf_bomber01.dxt1.4108.0.255.2.18.-1.png](/wf_bomber01.dxt1.4108.0.255.2.18.-1.png)![wf_srato01.dxt1.4108.0.255.2.19.-1.png](/wf_srato01.dxt1.4108.0.255.2.19.-1.png)![wf_tpt01.dxt1.4108.0.255.2.22.-1.png](/wf_tpt01.dxt1.4108.0.255.2.22.-1.png)

![ai_ftr01.dxt1.4108.0.255.2.39.-1.png](/ai_ftr01.dxt1.4108.0.255.2.39.-1.png)![ai_bomber01.dxt1.4108.0.255.2.32.-1.png](/ai_bomber01.dxt1.4108.0.255.2.32.-1.png)![ai_tpt01.dxt1.4108.0.255.2.34.-1.png](/ai_tpt01.dxt1.4108.0.255.2.34.-1.png)

![u_gshp01.dxt1.4108.0.255.2.37.-1.png](/u_gshp01.dxt1.4108.0.255.2.37.-1.png)![u_ftr01.dxt1.4108.0.255.2.24.-1.png](/u_ftr01.dxt1.4108.0.255.2.24.-1.png)![u_bomber01.dxt1.4108.0.255.2.24.-1.png](/u_bomber01.dxt1.4108.0.255.2.24.-1.png)

![t_gshp01.dxt1.4108.0.255.2.20.-1.png](/t_gshp01.dxt1.4108.0.255.2.20.-1.png)![t_ftr01.dxt1.4108.0.255.2.31.-1.png](/t_ftr01.dxt1.4108.0.255.2.31.-1.png)![t_bomber01.dxt1.4108.0.255.2.21.-1.png](/t_bomber01.dxt1.4108.0.255.2.21.-1.png)![t_srato01.dxt1.4108.0.255.2.41.-1.png](/t_srato01.dxt1.4108.0.255.2.41.-1.png)![t_tpt01.dxt1.4108.0.255.2.20.-1.png](/t_tpt01.dxt1.4108.0.255.2.20.-1.png)

![x_gshp01.dxt1.4108.0.255.2.21.-1.png](/x_gshp01.dxt1.4108.0.255.2.21.-1.png)![x_ftr01.dxt1.4108.0.255.2.19.-1.png](/x_ftr01.dxt1.4108.0.255.2.19.-1.png)![x_bomber01.dxt1.4108.0.255.2.22.-1.png](/x_bomber01.dxt1.4108.0.255.2.22.-1.png)![x_srato01.dxt1.4108.0.255.2.21.-1.png](/x_srato01.dxt1.4108.0.255.2.21.-1.png)![x_tpt01.dxt1.4108.0.255.2.20.-1.png](/x_tpt01.dxt1.4108.0.255.2.20.-1.png)

# Water vehicle XML Section and detail

![s_frigate01.dxt1.4108.0.255.2.21.-1.png](/s_frigate01.dxt1.4108.0.255.2.21.-1.png)![s_bshp01.dxt1.4108.0.255.2.18.-1.png](/s_bshp01.dxt1.4108.0.255.2.18.-1.png)![s_dnought01.dxt1.4108.0.255.2.29.-1.png](/s_dnought01.dxt1.4108.0.255.2.29.-1.png)![s_sub01.dxt1.4108.0.255.2.12.-1.png](/s_sub01.dxt1.4108.0.255.2.12.-1.png)![s_lcraft01.dxt1.4108.0.255.2.12.-1.png](/s_lcraft01.dxt1.4108.0.255.2.12.-1.png)

![wf_frigate01.dxt1.4108.0.255.2.19.-1.png](/wf_frigate01.dxt1.4108.0.255.2.19.-1.png)![wf_bship01.dxt1.4108.0.255.2.19.-1.png](/wf_bship01.dxt1.4108.0.255.2.19.-1.png)![wf_dnought01.dxt1.4108.0.255.2.22.-1.png](/wf_dnought01.dxt1.4108.0.255.2.22.-1.png)![wf_sub01.dxt1.4108.0.255.2.23.-1.png](/wf_sub01.dxt1.4108.0.255.2.23.-1.png)![wf_lcraft01.dxt1.4108.0.255.2.16.-1.png](/wf_lcraft01.dxt1.4108.0.255.2.16.-1.png)

![ai_frigate01.dxt1.4108.0.255.2.30.-1.png](/ai_frigate01.dxt1.4108.0.255.2.30.-1.png)![ai_bship01.dxt1.4108.0.255.2.38.-1.png](/ai_bship01.dxt1.4108.0.255.2.38.-1.png)![ai_sub01.dxt1.4108.0.255.2.35.-1.png](/ai_sub01.dxt1.4108.0.255.2.35.-1.png)![ai_lcraft01.dxt1.4108.0.255.2.30.-1.png](/ai_lcraft01.dxt1.4108.0.255.2.30.-1.png)

![t_frigate01.dxt1.4108.0.255.2.19.-1.png](/t_frigate01.dxt1.4108.0.255.2.19.-1.png)![t_bship01.dxt1.4108.0.255.2.19.-1.png](/t_bship01.dxt1.4108.0.255.2.19.-1.png)![t_dnought01.dxt1.4108.0.255.2.15.-1.png](/t_dnought01.dxt1.4108.0.255.2.15.-1.png)![t_sub01.dxt1.4108.0.255.2.15.-1.png](/t_sub01.dxt1.4108.0.255.2.15.-1.png)

![x_frigate01.dxt1.4108.0.255.2.18.-1.png](/x_frigate01.dxt1.4108.0.255.2.18.-1.png)![x_bship01.dxt1.4108.0.255.2.17.-1.png](/x_bship01.dxt1.4108.0.255.2.17.-1.png)![x_dnought01.dxt1.4108.0.255.2.19.-1.png](/x_dnought01.dxt1.4108.0.255.2.19.-1.png)![x_sub01.dxt1.4108.0.255.2.20.-1.png](/x_sub01.dxt1.4108.0.255.2.20.-1.png)

# Unit Scripts Sections and detail

- mpScript














