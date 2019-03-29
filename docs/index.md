# Ooznes OX CNC.

My addons and customisations.

## Wasteboard

M5 nut inserts, spaced 150mm, stagerred so that in the centre of 150x150 square there's a nut.

![Wasteboard](./images/clamps.jpg)

## Limit switches

They are must have!

## Emergency stop

I needed it on a few occasions. 

![eStop button](./images/estop-button.jpg)

<script src="https://embed.github.com/view/3d/muxa/ox-cnc/master/docs/files/eStop-Button-XT60-Insert-all-parts.stl"></script>

- [eStop-Button-XT60-Insert.stl](./files/eStop-Button-XT60-Insert.stl)
- [eStop-Button-XT60-Insert-Nut.stl](./files/eStop-Button-XT60-Insert-Nut.stl)
- [eStop-Button-XT60-Insert-all-parts.stl](./files/eStop-Button-XT60-Insert-all-parts.stl)

## Z-height mod

Swap the bottom two 2040 cross beams and you get 40mm more Z-height!
![Z-height mod](./images/z-height-mod.jpg)

## Dust shoe

![3D printed dust shoe with a brush](./images/dust-shoe-brush-3dp.jpg)

## Z-Probe

Wires connected to `SCL` (`A5`) and `GND`

> So the probe is anything that will take pin A5 to ground when it touches your object. The probe position is relative to machine 0. A typical probe command might be `G38.2 X20 Y15 Z-100` (in mm mode). You should set a slow feed rate , e.g. `F20` (20mm/min). The `G38` will move to X and Y, then Z axis will lower to -100 until the probe makes contact with your object, at which time movement stops. Grbl will report the machine position of the probe touch. 

![xPro pins](./images/xpro-pins.jpg)

> Connect a small capacitance capacitor (e.g. 471) between the probe wires to avoid false triggers

Macro to probe, store location and move to top: `G21 G91 G38.2 F50 Z-10; G10 L20 P1 Z3; G28 G91 Z0`

Important commands: 
* `G28.1` - store current location 
* `G28` - move to remembered location
* `G38.2 F50 Z-5` - move Z -5mm until touched 
* `G92 Z0` - set work coordinate

## Spindle control

1. [Customise Makita spindle](https://www.instructables.com/id/Makita-RT0700C-Detachable-Cable-Mod/)

2. Add relay.

## Vacuum control
## Clamps

![Simple clamps](./images/clamps.jpg)

## Fence

Stops the chips flying on to the Y belts and gears.

## Lights