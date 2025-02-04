---
title: Res File Detailed Documentation
description: In Depth Information on how the RES or Resource File works. 
published: true
date: 2025-02-04T21:10:23.059Z
tags: res file
editor: markdown
dateCreated: 2025-02-04T21:08:09.498Z
---

# BW1 Data Structure

## Sections and Data Entries

### RXET (Section)
- Contains: **Level Name** and **FTBX**  
- **FTBX** (Section)  
  - Contains: **Amount of TXET entries** and the **TXET entries themselves**  
  - **TXET** (Section)  
    - Contains:
      - **Image Name** (corresponds to `cTextureResource` in `_Levels.xml`)
      - **Image Size and Format**
      - **LAP** and **PIM** entries  
    - **PIM** (Data Entry)  
      - Contains: **Image data** (interpreted based on image format in TXET)  
    - **LAP** (Data Entry)  
      - Contains: **Palette data** (only used by textures in **P8** format)  

---

### DNOS (Section)
- Contains: **Level Name**, **HFSB**, **HPSD**, and **DPSD**  
- **HFSB** (Data Entry)  
  - Contains: **Amount of sounds** that follow  
  - *(Sounds come in HPSD, DPSD pairs)*  
- **HPSD** (Data Entry)  
  - Contains: **Sound name** (corresponds to `sSampleResource`)  
- **DPSD** (Data Entry)  
  - Contains: **Sound data**  

---

### Other Data Entries
- **LDOM**  
  - Contains: **Model name** and **Model data**  
  - *(Name corresponds to `cNodeHierarchyResource`)*  
- **MINA**  
  - Contains: **Animation name** and **Animation data**  
  - *(Name corresponds to `cAnimationResource`)*  
- **PRCS**  
  - Contains: **Script name** and **Script data**  
  - *(Name corresponds to `cGameScriptResource`)*  
- **FEQT**  
  - Contains: **Effect name** and **Effect data**  
  - *(Name corresponds to `cTequilaEffectResource`)*  

---

**Note:**  
The exact definitions of the data entries and sections in **BW1** are still a work in progress.
