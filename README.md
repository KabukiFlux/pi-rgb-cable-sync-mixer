# RGBpi cable sync mixer

Small PCB mod to mix the sync in the RGBpi cable to solve sync issues

## Table of contents

- [Why](#why)
- [Description](#description)
- [Schematics](#schematics)
- [Install](#install)
- [Pics and final result](#pics-and-final-result)

## Why?

In order to eliminate/mitigate the sync issues on the cable we can do several options,
one is to use the common XOR mixer as usual, this other approach reduces the BOM
and enables the PCB to fit in the scart cable connector without any problem.


As you can see on this screenshot the original cable without modding induces a lot of 
DC bias on the sync causing some issues on some TVs, arcade monitors and so: 

![RGBpi original cable waveform](assets/rgbpi_original_waveform.jpg)

With this mod we remove the DC offset not mixing into a full CSync signal but at least
we enable it to be used on more systems, of course the best approach is always the active sync
mixer with some gates but with this mod we restore at least the basic functionality.

![RGBpi modded cable waveform](assets/rgbpi_modded_waveform.jpg)

Yes, the vertical period is not as good as with an active mixer but at least it removes the sync
issues on most devices with a very small BOM.

### OSSC comparison

Without modding:

![OSSC without modding](assets/ossc_original_cable_no_sync.jpg)

Modded cable:

![OSSC modded cable](assets/ossc_modded_cable_ok_sync.jpg)



## Description

This is intended to be a very small PCB to be included inside the scart connector on the rgbpi cable.

![Sync mixer PCB](assets/pcb.jpg)

It is valid for all the rgbpi cable versions, we will see on the installation procedure V1 and V2 cables.

In the BOM directory there's an interactive BOM with all the required components.

In the gerbers directory we have the gerbers to manufacture the boards.

In the KiCAD folder we can find the KiCAD project itself.

## Schematics

![Schematics](assets/schematics.jpg)

![PCB footprint](assets/pcb_diagram.jpg)

You can find here as well as the KiCAD files inside the KiCAD folder.


## Install

1- Send to manufacture the GERBER board to JLCPCB or other PCB manufacturer.

2- Get the components required, you can see here the Bill Of Materials [BOM](bom/ibom.html)

3- Solder the components.

4- Follow the procedure depending on your cable version.

### Detect your cable version

This is what we will call V1, follow the V1 install procedure:

![Cable V1](assets/cable_v1.jpg)

This is what we will call V2, follow the V2 install procedure:

![Cable V2](assets/cable_v2.jpg)

### V1 cable install

If your cable is V1 then:

* Check the wires for the installation

![v1 wires](assets/v1_01_wires.jpg)

* Check the soldering positions

![v1 soldering positions](assets/v1_02_solder_pos.jpg)

* Solder as shown (the big white cable is not required by this mod)

![v1 solder](assets/v1_03_solder.jpg)

### V2 cable install

If your cable is V2 then:

* Check the wires for the installation

![v2 wires](assets/v2_01_wires.jpg)

* Check the soldering positions

![v2 soldering positions](assets/v2_02_solder_pos.jpg)

* Place as shown

![v2 placing](assets/v2_03_placing.jpg)

* Solder the scart part (you can use for GND the 3rd pin from the bottom, it is better)

![v2 solder scart part](assets/v2_04_solder_scart.jpg)

* Solder the cable hsync and vsync wires

![v2 solder sync wires](assets/v2_05_solder_cables.jpg)



### Pics and final result

V1:

![V1 close](assets/v1_04_closed.jpg)

V2

![V2 close](assets/v2_06_closed.jpg)

That's it.



I'm not responsible
============
And yes, read below, no responsibility taken on bad use.

Special thanks to Retroark [here on X](https://twitter.com/retroark) 


DISCLAIMER (See Licensing)
==========================
See LICENSE fo more information.
