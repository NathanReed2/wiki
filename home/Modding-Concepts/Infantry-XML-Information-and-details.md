---
title: Infantry XML Information and details
description: 
published: true
date: 2025-09-13T09:02:39.884Z
tags: 
editor: markdown
dateCreated: 2025-01-26T22:57:13.447Z
---

> If you have any questions related to modding, join the [Battalion Wars discord server](https://discord.gg/aPvrTsDARJ)  and we'll be happy to help with anything you might be stuck on.
{.is-info}

---

# cTroop

The **cTroop** object defines an infantry unit's behavior, attributes, and position within the game world, etc.
 
## mName

- The name or identifier for the troop **(can be left empty)**.
   
![screenshot_2025-01-26_141410.png](/screenshot_2025-01-26_141410.png)

## mBase  

- This is a core component used to define the base properties of a specific troop.
  
![screenshot_2025-01-26_141604.png](/screenshot_2025-01-26_141604.png)

## spawnMatrix
  
- A 4x4 transformation matrix.
  
![screenshot_2025-01-26_141703.png](/screenshot_2025-01-26_141703.png)

## State

- The troop’s current AI state (e.g., **AI_STATE_NORMAL**). 
  
![screenshot_2025-01-26_142043.png](/screenshot_2025-01-26_142043.png)
  
## mAttackStyle

- Defines how the troop engages in combat (e.g., **ATTACKSTYLE_FROM_DEFENSIVE_AREA**). 
  
![screenshot_2025-01-26_142056.png](/screenshot_2025-01-26_142056.png)
  
## mMoveStyle 
  
- Determines how the troop moves (e.g., **MOVESTYLE_ATTACK_ON_SIGHT**).  
  
![screenshot_2025-01-26_142106.png](/screenshot_2025-01-26_142106.png)

## mStartWaypoint

- Specifies the starting waypoint for troop movement (if applicable). 
  
![screenshot_2025-01-26_142121.png](/screenshot_2025-01-26_142121.png)
 
##  mPlaceOnPlatform
  
- Indicates if the troop should be placed on a platform (**eTrue** or **eFalse**).  
  
![screenshot_2025-01-26_142132.png](/screenshot_2025-01-26_142132.png)

## mUnitInstanceFlags

- There a multiple flags for the unit behaviors.
  
![screenshot_2025-01-26_150709.png](/screenshot_2025-01-26_150709.png)

Here are some of the flags we know of so far.  
   
| mUnitInstanceFlags |  | elements |
| --- | --- | --- |
| AIUNIT_INITIALLY_DONT_IDLE_TURN | = | 1 |
| AIUNIT_NEVER_IDLE_TURN | = | 2 |
| AIUNIT_INACTIVE | = | 4 |
| AIUNIT_NOT_SCORED | = | 8 |
| AIUNIT_NOT_COMMANDABLE | = | 16 |
| AIUNIT_CAN_IGNORE_BOUNDARY | = | 32 |
| AIUNIT_STARTS_AS_POW | = | 64 |

## mVehicleOccupant

- Specifies if the troop starts in a vehicle. (**eTrue** or **eFalse**)
  
![screenshot_2025-01-26_142724.png](/screenshot_2025-01-26_142724.png)

## mRevivable

- Determines if the troop can be revived after being defeated. (**eTrue** or **eFalse**)
  
![screenshot_2025-01-26_142733.png](/screenshot_2025-01-26_142733.png)

## mDontRegisterBirth

- If **eTrue**, it's possible it prevents the troop’s creation from being logged or registered. (**eTrue** or **eFalse**)  
  
![screenshot_2025-01-26_142744.png](/screenshot_2025-01-26_142744.png)
 
## mEnemyTargetableOnly
 
- Restricts the troop to being targeted only by enemies. (**eTrue** or **eFalse**) 
  
![screenshot_2025-01-26_142750.png](/screenshot_2025-01-26_142750.png)

## mpScript

- Links to a custom game script that can influence the troop's behavior.  
  
![screenshot_2025-01-26_143026.png](/screenshot_2025-01-26_143026.png)

## Mat

- This seems to be the main 4x4 matrix that determines the troop's initial position and orientation in the game world.

![screenshot_2025-01-26_141948.png](/screenshot_2025-01-26_141948.png)

## miWorldObjFlags

- Flags related to the troop's interaction with the world.  
  
![screenshot_2025-01-26_143109.png](/screenshot_2025-01-26_143109.png)

## SystemFlags

- Internal system-specific flags for the troop.  
  
![screenshot_2025-01-26_143120.png](/screenshot_2025-01-26_143120.png)

---

> In summary, the `cTroop` object is the blueprint for each infantry unit, defining its behavior, spawn location, AI settings, and interaction with the game world. Each attribute and pointer allows for precise customization of how a unit behaves in the game.  
{.is-info}

---

# sTroopBase   

The **mBase** points to the **sTroopBase** data, which provides shared attributes like stats or behaviors for this type of troop. 

- This is a core component used to define the base properties of a specific troop. It acts as a pointer reference **(mBase)** in the object configuration to a predefined blueprint that determines the attributes of the troop. 
  
- These attributes might include its type **(e.g., Rifle Grunt, Bazooka Vet, etc.)**, base stats, animations, and behaviors. The **mBase** field references an **sTroopBase** entity using a unique and random **ID** in this case the **ID** is **2138049763**. This ID points to the data that defines what kind of troop this is, which includes parameters like health, movement speed, weapon type, and other base characteristics. 

---

> Essentially, the `sTroopBase` is the foundational **"blueprint"** that ensures troops of the same type share consistent behaviors and abilities. 
{.is-info}









