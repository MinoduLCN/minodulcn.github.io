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

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; flex-wrap: wrap;">

  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29.png"/>
  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29Inside.jpg"/>
  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29open.jpg"/>
  <img src="../assets/images/0B_Parametric_Box_AxialFan_AirFlowVent_v29_2.jpg"/>

</div>


# Assembly guide – Minodu Local Network

## 3D Printing Guide

### Materials
- ABS or PETG filament
- TPU for flexible and sealing components

### 3D Files
#### Protection Box 3d Files
*ABS or at least PETG for outdoor setup*
 - [01x Base](../assets/3dFiles/Base_x01.stl)
 - [01x Top](../assets/3dFiles/Top_x01.stl) if you can Print Mulitcolor use This [Top_x01-MultiColor.stl](../assets/3dFiles/Top_x01-MultiColor.stl)
 - [02x Hinge](../assets/3dFiles/Hinge_x02.stl)
 - [02x Latch](../assets/3dFiles/Latch_x02.stl)
 - [02x Latch clip](../assets/3dFiles/Clip_x02.stl)

 *Flexible parts (TPU)*
 - [02x TPU Cable outlet cap](../assets/3dFiles/TPU_CableOutletCap_x02.stl)
 - [01x TPU RPi5 ports dust cap](../assets/3dFiles/TPU_RPi5PortDustCaps_x01.stl)

#### Stevenson Screen Files
  - [01x Stevenson screen sensor plate](../assets/3dFiles/StevensonScreen_RC01_Sensor_Plate)
  - [01x Stevenson screen top](../assets/3dFiles/StevensonScreen_RC01_Top.stl)
  - [01x Stevenson screen sensor plate holder](../assets/3dFiles/StevensonScreen_RC01_Midlle_SensorPlate_Holder.stl)
  - [06x Stevenson screen Midlle](../assets/3dFiles/StevensonScreen_RC01_Midlle_X06)
  - [01x Stevenson screen base](../assets/3dFiles/StevensonScreen_RC01_Base.stl)
  - [01x Stevenson screen bottom cover](../assets/3dFiles/StevensonScreen_RC01_Botom.stl)
 

 

### Slicer Setup
3D printers only understand G-code language (**geometric code)**; So what we need to do is to convert the *STL* files into G CODE. 

Recommended tool: I personally use [OrcaSlicer](https://www.orcaslicer.com/) but they all work the same.
Tool tutorial: Watch [this quick video](https://www.youtube.com/watch?v=KWfKkeOSpmw) to get you started if you are new to 3D printing with OrcaSlicer.

Here is The Orca slicer projectfile withh all the parts
    - [Minodu_Box.3mf](../assets/3dFiles/Minodu_Box.3mf)

## Protection Box
This guide explains how to assemble the 3D-printed protection box for the Minodu Local Network. The enclosure is designed to house a Raspberry Pi 5, the Tele-Agriculture Board, a 12V-to-5V DC-DC power converter, sensor cables, and can be mounted on a pole for outdoor installations with a Stevenson screen.

Assembly video
<iframe
  src="https://youtu.be/kqEWPuSYfUo"
  style="width:100%; height:480px;"
></iframe>

### Required Components

#### 3D Printed Parts

- Top cover
- Bottom enclosure
- 2 × Hinges
- 2 × Latches
- TPU dust cap

#### Electronics

- Raspberry Pi 5
- Raspberry Pi Active Cooler
- Tele-Agriculture Board
- 12 V → 5 V DC-DC Converter
- 30 × 30 × 10 mm cooling fan

#### Hardware

- 04x M2.5 heat-set inserts
- 04x M2.5 × 20 mm standoffs
- 04x M2.5 × 6 mm screws
- 06x M3 × 30 mm hex socket head screws
- 06x M3 hex nuts
- 02x M6 heat-set inserts
- 02x M6 × 14 mm countersunk screw

### Step by step assembly
#### Step 1 – Install Raspberry Pi Inserts

Turn the top cover upside down.
Insert the M2.5 heat-set inserts into the designated mounting holes using a soldering iron or heat-set insert tool.
Ensure every insert sits perfectly flush with the plastic surface.
*Allow the inserts to cool before continuing.*

![Step 01](../assets/images/00.0.png "Step 01")
![Step 02](../assets/images/00.1.jpg "Step 02")

#### Step 2 – Mount the Raspberry Pi
Position the Raspberry Pi 5 (with its cooling fan already installed) over the inserts.
![Step 03](../assets/images/01.0.png "Step 03")


Install the 20 mm M2.5 standoffs and secure the Raspberry Pi.
![Step 0X](../assets/images/02.0.jpg "Step 0X")
![Step 0X](../assets/images/02.1.jpg "Step 0X")

Verify that the board is firmly mounted.
![Step 0X](../assets/images/02.2.jpg "Step 0X")


#### Step 3 – Install the Tele-Agriculture Board

Place the Tele-Agriculture Board on top of the standoffs.
![Step 0X](../assets/images/03.0.jpg "Step 0X")

Secure it using M2.5 × 6 mm screws.
![Step 0X](../assets/images/04.0.jpg "Step 0X")
Install the fourth screw located beneath the display.
Check that nothing moves or is loose.

![Step 04](../assets/images/04.1.png "Step 0X")

#### Step 4 – Assemble the Latches

For each latch:

Insert one M3 hex nut.
Align the latch.
Insert one M3 × 30 mm screw.
Tighten until secure.
![Step 0X](../assets/images/05.0.png "Step 0X")

Repeat for the second latch.

![Step 0X](../assets/images/05.1.jpg "Step 0X")

![Step 0X](../assets/images/05.2.jpg "Step 0X")


#### Step 5 – Assemble the Hinges

Using the same hardware:

Insert the M3 nut.
Align the hinge.
Insert the M3 × 30 mm screw.
Tighten.
![Step 0X](../assets/images/06.0.jpg "Step 0X")

Repeat for the second hinge.

Ensure both hinges rotate freely.

![Step 0X](../assets/images/06.1.jpg "Step 0X")

#### Step 6 – Install the DC Converter Insert

Install the M6 heat-set insert for the DC-DC converter into the bottom enclosure.
![Step 0X](../assets/images/07.0.jpg "Step 0X")

Make sure it is completely flush with the plastic.

![Step 0X](../assets/images/07.1.jpg "Step 0X")

#### Step 7 – Install the Cooling Fan

![Step 0X](../assets/images/08.1.jpg "Step 0X")

Insert the 30 × 30 × 10 mm cooling fan into its ventilation opening.

Ensure:
The cable exits toward the wiring opening.
Airflow is directed from inside the enclosure to the outside.
Push the fan fully into position.
If necessary, secure it with a very small amount of glue.

![Step 0X](../assets/images/08.2.png "Step 0X")

Important: Ensure the fan blades rotate freely. If the blades touch the enclosure, If they rub against the enclosure, it can be jammed, overheat and be fried.

#### Step 8 – Install the DC-DC Converter

Position the 12V-to-5V converter inside the enclosure.

![Step 0X](../assets/images/09.0.jpg "Step 0X")

Align the mounting holes with the insert.

![Step 0X](../assets/images/09.1.jpg "Step 0X")

Secure it using the M6 × 14 mm countersunk screw.

![Step 0X](../assets/images/09.2.jpg "Step 0X")

Ensure the wiring faces the cable exit.

![Step 0X](../assets/images/09.3.jpg "Step 0X")

#### Step 9 – Join Both Halves

Align the hinge side first.

Insert the hinge screws, nuts and, tighten.

![Step 0X](../assets/images/10.0.jpg "Step 0X")
![Step 0X](../assets/images/10.1.png "Step 0X")

Then align the latch side and secure it.

Verify that:

- The enclosure opens smoothly.
- The enclosure closes correctly.

#### Step 10 – Install the Latch Clips

Insert the two printed latch clips into the lower enclosure.
Push them fully into place until flush.
Close the enclosure and verify that the latches lock securely.

![Step 0X](../assets/images/09.40.jpg "Step 0X")
![Step 0X](../assets/images/09.41.jpg "Step 0X")

#### Step 11 – Final Assembly

Install:
- TPU dust cap
- Wi-Fi antenna
- Sensor cables
Install the dust cap around the cables to maintain dust protection. Route all cables through the cable openings.

![Step 0X](../assets/images/xx.jpg "Step 0X")

The enclosure is now ready to be mounted on a pole together with the Stevenson screen for outdoor deployment.


## Stevenson Screen : Sensors
- Stevenson Screen for environmental sensors that need to be protected but still measure temperature, humidity, etc.
- Weather Meter connection
### Required Components
3D Printed Parts




##
