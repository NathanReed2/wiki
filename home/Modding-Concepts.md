---
title: Modding Concepts
description: 
published: true
date: 2025-09-11T18:06:59.170Z
tags: modding, modding documentation
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
  
Battalion Wars 1 and 2 utilize resource files with the **.res** extension to store various assets for each level including models, textures, sounds, animations, effects, and scripts. Each level has its own dedicated resource file. By default, levels cannot access assets that are not contained within their respective **.res** file.
  
For more detailed information, check out the [Res-File-Detailed-Documentation](/home/Modding-Concepts/Res-File-Detailed-Documentation) page to learn more.

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

# [Infantry XML Information and Details](/en/home/Modding-Concepts/Infantry-XML-Information-and-details) 

![Solar Empire Grunt](/s_grunt01.dxt1.4108.0.255.2.93.-1.png "Solar Empire - Grunt (Rifle Infantry)")![Solar Empire Anti-Armor](/s_antiarm01.dxt1.4108.0.255.2.64.-1.png "Solar Empire - Anti-Armor Trooper")![Solar Empire Flame Veteran](/s_hose01.dxt1.4108.0.255.2.72.-1.png "Solar Empire - Flame Veteran")![Solar Empire Anti-Air](/s_antiair01.dxt1.4108.0.255.2.66.-1.png "Solar Empire - Anti-Air Veteran")![Solar Empire Assault Veteran](/s_parabolic01.dxt1.4108.0.255.2.78.-1.png "Solar Empire - Assault Veteran")![Solar Empire Heavy Machine Gunner](/s_hmg01.dxt1.4108.0.255.2.62.-1.png "Solar Empire - Heavy Machine Gunner")

![Western Frontier Grunt](/wf_grunt01.png "Western Frontier - Grunt (Rifle Infantry)")![Western Frontier Anti-Armor](/wf_antiarm01.dxt1.4108.0.255.2.54.-1.png "Western Frontier - Anti-Armor Trooper")![Western Frontier Flame Veteran](/wf_hose01.dxt1.4108.0.255.2.60.-1.png "Western Frontier - Flame Veteran")![Western Frontier Anti-Air](/wf_antiair01.dxt1.4108.0.255.2.59.-1.png "Western Frontier - Anti-Air Veteran")![Western Frontier Assault Veteran](/wf_parabolic01.dxt1.4108.0.255.2.82.-1.png "Western Frontier - Assault Veteran")![Western Frontier Heavy Machine Gunner](/wf_hmg01.dxt1.4108.0.255.2.53.-1.png "Western Frontier - Heavy Machine Gunner")

![Anglo Isles Grunt](/icon_anglogrunt.dxt1.4108.0.255.2.69.-1.png "Anglo Isles - Grunt (Rifle Infantry)")![Anglo Isles Anti-Armor](/ai_antiarm01.dxt1.4108.0.255.2.73.-1.png "Anglo Isles - Anti-Armor Trooper")![Anglo Isles Flame Veteran](/ai_hose01.dxt1.4108.0.255.2.69.-1.png "Anglo Isles - Flame Veteran")![Anglo Isles Anti-Air](/ai_antiair01.dxt1.4108.0.255.2.68.-1.png "Anglo Isles - Anti-Air Veteran")![Anglo Isles Assault Veteran](/ai_parabolic01.dxt1.4108.0.255.2.65.-1.png "Anglo Isles - Assault Veteran")![Anglo Isles Heavy Machine Gunner](/ai_hmg01.dxt1.4108.0.255.2.77.-1.png "Anglo Isles - Heavy Machine Gunner")

![Underworld Grunt](/u_grunt01.dxt1.4108.0.255.2.64.-1.png "Underworld - Grunt (Rifle Infantry)")![Underworld Anti-Armor](/u_antiarm01.dxt1.4108.0.255.2.65.-1.png "Underworld - Anti-Armor Trooper")![Underworld Flame Veteran](/u_hose01.dxt1.4108.0.255.2.69.-1.png "Underworld - Flame Veteran")![Underworld Anti-Air](/u_antiair01.dxt1.4108.0.255.2.72.-1.png "Underworld - Anti-Air Veteran")![Underworld Assault Veteran](/u_parabolic01.dxt1.4108.0.255.2.75.-1.png "Underworld - Assault Veteran")![Underworld Heavy Machine Gunner](/u_hmg01.dxt1.4108.0.255.2.74.-1.png "Underworld - Heavy Machine Gunner")

![Tundran Territories Grunt](/t_grunt01.dxt1.4108.0.255.2.69.-1.png "Tundran Territories - Grunt (Rifle Infantry)")![Tundran Territories Anti-Armor](/t_antiarm01.dxt1.4108.0.255.2.60.-1.png "Tundran Territories - Anti-Armor Trooper")![Tundran Territories Flame Veteran](/t_hose01.dxt1.4108.0.255.2.53.-1.png "Tundran Territories - Flame Veteran")![Tundran Territories Anti-Air](/t_antiair01.dxt1.4108.0.255.2.57.-1.png "Tundran Territories - Anti-Air Veteran")![Tundran Territories Assault Veteran](/t_parabolic01.dxt1.4108.0.255.2.57.-1.png "Tundran Territories - Assault Veteran")![Tundran Territories Heavy Machine Gunner](/t_hmg01.dxt1.4108.0.255.2.58.-1.png "Tundran Territories - Heavy Machine Gunner")

![Xylvania Grunt](/x_grunt01.dxt1.4108.0.255.2.61.-1.png "Xylvania - Grunt (Rifle Infantry)")![Xylvania Anti-Armor](/x_antiarm01.dxt1.4108.0.255.2.56.-1.png "Xylvania - Anti-Armor Trooper")![Xylvania Flame Veteran](/x_hose01.dxt1.4108.0.255.2.55.-1.png "Xylvania - Flame Veteran")![Xylvania Anti-Air](/x_antiair01.dxt1.4108.0.255.2.59.-1.png "Xylvania - Anti-Air Veteran")![Xylvania Assault Veteran](/x_parabolic01.dxt1.4108.0.255.2.63.-1.png "Xylvania - Assault Veteran")![Xylvania Heavy Machine Gunner](/x_hmg01.dxt1.4108.0.255.2.60.-1.png "Xylvania - Heavy Machine Gunner")

# [Ground Vehicle XML Section and Details](/home/Modding-Concepts/Ground-Vehicle-XML-Section-and-Details)

![Solar Empire Recon](/s_reco01.dxt1.4108.0.255.2.95.-1.png "Solar Empire - Recon Vehicle")![Solar Empire Light Tank](/s_ltnk01.dxt1.4108.0.255.2.17.-1.png "Solar Empire - Light Tank")![Solar Empire Heavy Tank](/s_htnk01.dxt1.4108.0.255.2.20.-1.png "Solar Empire - Heavy Tank")![Solar Empire Anti-Air](/s_aa01.dxt1.4108.0.255.2.36.-1.png "Solar Empire - Anti-Air Vehicle")![Solar Empire Artillery](/s_art01.dxt1.4108.0.255.2.17.-1.png "Solar Empire - Artillery")

![Western Frontier Recon](/wf_reco01.dxt1.4108.0.255.2.20.-1.png "Western Frontier - Recon Vehicle")![Western Frontier Heavy Recon](/wf_heavy_recon.png "Western Frontier - Heavy Recon")![Western Frontier APC](/wf_apc2.png "Western Frontier - Armored Personnel Carrier")![Western Frontier Light Tank](/wf_ltnk01.dxt1.4108.0.255.2.21.-1.png "Western Frontier - Light Tank")![Western Frontier Heavy Tank](/wf_htnk01.p8.4108.0.255.2.21.-1.png "Western Frontier - Heavy Tank")![Western Frontier Battlestation](/wf_bsta01.dxt1.4108.0.255.2.22.-1.png "Western Frontier - Battlestation")![Western Frontier Anti-Air](/wf_aa01.dxt1.4108.0.255.2.19.-1.png "Western Frontier - Anti-Air Vehicle")![Western Frontier Artillery](/wf_art01.dxt1.4108.0.255.2.21.-1.png "Western Frontier - Artillery")

![Anglo Isles Light Tank](/ai_ltnk01.dxt1.4108.0.255.2.39.-1.png "Anglo Isles - Light Tank")![Anglo Isles Heavy Tank](/ai_htnk01.dxt1.4108.0.255.2.36.-1.png "Anglo Isles - Heavy Tank")![Anglo Isles Artillery](/ai_art01.dxt1.4108.0.255.2.27.-1.png "Anglo Isles - Artillery")

![Underworld Heavy Tank](/u_htnk01.dxt1.4108.0.255.2.28.-1.png "Underworld - Heavy Tank")![Underworld Battlestation](/u_bsta01.dxt1.4108.0.255.2.27.-1.png "Underworld - Battlestation")![Underworld Artillery](/u_art01.dxt1.4108.0.255.2.25.-1.png "Underworld - Artillery")

![Tundran Territories Recon](/t_reco01.dxt1.4108.0.255.2.19.-1.png "Tundran Territories - Recon Vehicle")![Tundran Territories Light Tank](/t_ltnk01.dxt1.4108.0.255.2.20.-1.png "Tundran Territories - Light Tank")![Tundran Territories Heavy Tank](/t_htnk01.dxt1.4108.0.255.2.21.-1.png "Tundran Territories - Heavy Tank")![Tundran Territories Battlestation](/t_bsta01.dxt1.4108.0.255.2.19.-1.png "Tundran Territories - Battlestation")![Tundran Territories Anti-Air](/t_aa01.dxt1.4108.0.255.2.23.-1.png "Tundran Territories - Anti-Air Vehicle")![Tundran Territories Artillery](/t_art01.dxt1.4108.0.255.2.21.-1.png "Tundran Territories - Artillery")

![Xylvania Light Transport](/x_ltra01.dxt1.4108.0.255.2.32.-1.png "Xylvania - Light Transport")![Xylvania Light Tank](/x_ltnk01.dxt1.4108.0.255.2.22.-1.png "Xylvania - Light Tank")![Xylvania Heavy Tank](/x_htnk01.dxt1.4108.0.255.2.24.-1.png "Xylvania - Heavy Tank")![Xylvania Battlestation](/x_bsta01.dxt1.4108.0.255.2.30.-1.png "Xylvania - Battlestation")![Xylvania Anti-Air](/x_aa01.dxt1.4108.0.255.2.20.-1.png "Xylvania - Anti-Air Vehicle")![Xylvania Artillery](/x_art01.dxt1.4108.0.255.2.76.-1.png "Xylvania - Artillery")

# [Air Vehicle XML Section and Details](/home/Modding-Concepts/Air-vehicle-XML-Section-and-Details)

![Solar Empire Gunship](/s_gshp01.dxt1.4108.0.255.2.15.-1.png "Solar Empire - Gunship")![Solar Empire Fighter](/s_ftr01.dxt1.4108.0.255.2.24.-1.png "Solar Empire - Fighter")![Solar Empire Transport](/s_tpt01.dxt1.4108.0.255.2.18.-1.png "Solar Empire - Transport")

![Western Frontier Gunship](/wf_gshp01.dxt1.4108.0.255.2.19.-1.png "Western Frontier - Gunship")![Western Frontier Fighter](/wf_ftr01.dxt1.4108.0.255.2.20.-1.png "Western Frontier - Fighter")![Western Frontier Bomber](/wf_bomber01.dxt1.4108.0.255.2.18.-1.png "Western Frontier - Bomber")![Western Frontier Strato Destroyer](/wf_srato01.dxt1.4108.0.255.2.19.-1.png "Western Frontier - Strato Destroyer")![Western Frontier Transport](/wf_tpt01.dxt1.4108.0.255.2.22.-1.png "Western Frontier - Transport")

![Anglo Isles Fighter](/ai_ftr01.dxt1.4108.0.255.2.39.-1.png "Anglo Isles - Fighter")![Anglo Isles Bomber](/ai_bomber01.dxt1.4108.0.255.2.32.-1.png "Anglo Isles - Bomber")![Anglo Isles Transport](/ai_tpt01.dxt1.4108.0.255.2.34.-1.png "Anglo Isles - Transport")

![Underworld Gunship](/u_gshp01.dxt1.4108.0.255.2.37.-1.png "Underworld - Gunship")![Underworld Fighter](/u_ftr01.dxt1.4108.0.255.2.24.-1.png "Underworld - Fighter")![Underworld Bomber](/u_bomber01.dxt1.4108.0.255.2.24.-1.png "Underworld - Bomber")

![Tundran Territories Gunship](/t_gshp01.dxt1.4108.0.255.2.20.-1.png "Tundran Territories - Gunship")![Tundran Territories Fighter](/t_ftr01.dxt1.4108.0.255.2.31.-1.png "Tundran Territories - Fighter")![Tundran Territories Bomber](/t_bomber01.dxt1.4108.0.255.2.21.-1.png "Tundran Territories - Bomber")![Tundran Territories Strato Destroyer](/t_srato01.dxt1.4108.0.255.2.41.-1.png "Tundran Territories - Strato Destroyer")![Tundran Territories Transport](/t_tpt01.dxt1.4108.0.255.2.20.-1.png "Tundran Territories - Transport")

![Xylvania Gunship](/x_gshp01.dxt1.4108.0.255.2.21.-1.png "Xylvania - Gunship")![Xylvania Fighter](/x_ftr01.dxt1.4108.0.255.2.19.-1.png "Xylvania - Fighter")![Xylvania Bomber](/x_bomber01.dxt1.4108.0.255.2.22.-1.png "Xylvania - Bomber")![Xylvania Strato Destroyer](/x_srato01.dxt1.4108.0.255.2.21.-1.png "Xylvania - Strato Destroyer")![Xylvania Transport](/x_tpt01.dxt1.4108.0.255.2.20.-1.png "Xylvania - Transport")

# [Water Vehicle XML Section and Details](/home/Modding-Concepts/Water-Vehicle-XML-Section-and-Details)

![Solar Empire Frigate](/s_frigate01.dxt1.4108.0.255.2.21.-1.png "Solar Empire - Frigate")![Solar Empire Battleship](/s_bshp01.dxt1.4108.0.255.2.18.-1.png "Solar Empire - Battleship")![Solar Empire Dreadnought](/s_dnought01.dxt1.4108.0.255.2.29.-1.png "Solar Empire - Dreadnought")![Solar Empire Submarine](/s_sub01.dxt1.4108.0.255.2.12.-1.png "Solar Empire - Submarine")![Solar Empire Landing Craft](/s_lcraft01.dxt1.4108.0.255.2.12.-1.png "Solar Empire - Landing Craft")

![Western Frontier Frigate](/wf_frigate01.dxt1.4108.0.255.2.19.-1.png "Western Frontier - Frigate")![Western Frontier Battleship](/wf_bship01.dxt1.4108.0.255.2.19.-1.png "Western Frontier - Battleship")![Western Frontier Dreadnought](/wf_dnought01.dxt1.4108.0.255.2.22.-1.png "Western Frontier - Dreadnought")![Western Frontier Submarine](/wf_sub01.dxt1.4108.0.255.2.23.-1.png "Western Frontier - Submarine")![Western Frontier Landing Craft](/wf_lcraft01.dxt1.4108.0.255.2.16.-1.png "Western Frontier - Landing Craft")

![Anglo Isles Frigate](/ai_frigate01.dxt1.4108.0.255.2.30.-1.png "Anglo Isles - Frigate")![Anglo Isles Battleship](/ai_bship01.dxt1.4108.0.255.2.38.-1.png "Anglo Isles - Battleship")![Anglo Isles Submarine](/ai_sub01.dxt1.4108.0.255.2.35.-1.png "Anglo Isles - Submarine")![Anglo Isles Landing Craft](/ai_lcraft01.dxt1.4108.0.255.2.30.-1.png "Anglo Isles - Landing Craft")

![Tundran Territories Frigate](/t_frigate01.dxt1.4108.0.255.2.19.-1.png "Tundran Territories - Frigate")![Tundran Territories Battleship](/t_bship01.dxt1.4108.0.255.2.19.-1.png "Tundran Territories - Battleship")![Tundran Territories Dreadnought](/t_dnought01.dxt1.4108.0.255.2.15.-1.png "Tundran Territories - Dreadnought")![Tundran Territories Submarine](/t_sub01.dxt1.4108.0.255.2.15.-1.png "Tundran Territories - Submarine")

![Xylvania Frigate](/x_frigate01.dxt1.4108.0.255.2.18.-1.png "Xylvania - Frigate")![Xylvania Battleship](/x_bship01.dxt1.4108.0.255.2.17.-1.png "Xylvania - Battleship")![Xylvania Dreadnought](/x_dnought01.dxt1.4108.0.255.2.19.-1.png "Xylvania - Dreadnought")![Xylvania Submarine](/x_sub01.dxt1.4108.0.255.2.20.-1.png "Xylvania - Submarine")


# Unit Scripts Sections and detail

- mpScript














