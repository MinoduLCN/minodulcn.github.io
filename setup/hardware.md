---
layout: page
title: Hardware Assembly
---

<iframe
  src="https://a360.co/4q3GGlT"
  style="width:100%; height:720px;"
></iframe>
[Link to Design (Autodesk Fusion 360)](https://a360.co/4q3GGlT): https://a360.co/4q3GGlT

* TOC
{:toc}

<div style="display: flex; gap: 1rem; flex-wrap: wrap;">

  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29.png" style="width: 23%;" />
  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29Inside.jpg" style="width: 23%;" />
  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29open.jpg" style="width: 23%;" />
  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29_2.jpg" style="width: 23%;" />

</div>


## Assembly

<iframe
  src="https://YoutubePlaceHolder"
  style="width:100%; height:480px;"
></iframe>

# Requirements
- Weatherproof: rain-, dust- and windproof
- Openable for maintenance
- Contain RPi 5+ SolarPower Manager board(Type to be confirmed) with The TelaAgriculture board stacked on Top
- Output for the sensors
- Input for the solar panel cables

## Stevenson Screen : Sensors
- Stevenson Screen for environmental sensors that need to be protected but still measure temperature, humidity, etc.
- Weather Meter connection


## Images - Development Process

## 3D Printing 

### Materials
- ABS or PETG filament
- TPU for flexible and sealing components

### Files
*ABS or at least PETG for outdoor setup*
 - [01x Base](../assets/3dFiles/Base_x01.stl)
 - [01x Top](../assets/3dFiles/Top_x01.stl) if you can Print Mulitcolor use This [Top_x01-MultiColor.stl](../assets/3dFiles/Top_x01-MultiColor.stl)
 - [02x Hinge](../assets/3dFiles/Hinge_x02.stl)
 - [02x Latch](../assets/3dFiles/Latch_x02.stl)
 - [02x Latch clip](../assets/3dFiles/Clip_x02.stl)

 *Flexible parts (TPU)*
 - [02x TPU Cable outlet cap](../assets/3dFiles/TPU_CableOutletCap_x02.stl)
 - [01x TPU RPi5 ports dust cap](../assets/3dFiles/TPU_RPi5PortDustCaps_x01.stl)

### Slicer Setup
3D printers only understand G-code language (**geometric code)**; So what we need to do is to convert the *STL* files into G CODE. 

Recommended tool: I personally use [OrcaSlicer](https://www.orcaslicer.com/) but they all work the same.
Tool tutorial: Watch [this quick video](https://www.youtube.com/watch?v=KWfKkeOSpmw) to get you started if you are new to 3D printing with OrcaSlicer.

Here is The Orca slicer projectfile withh all the parts
    - [Minodu_Box.3mf](../assets/3dFiles/Minodu_Box.3mf)

##
