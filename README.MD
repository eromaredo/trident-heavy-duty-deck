# Heavy Duty Deck Panel for Voron Trident (Preview)

[!CAUTION]
I put a lot of effort into keeping all dimensions correct, but I haven't tested it in real life (yet) - only against Voron's official STEP file for a 250mm build and my own 4040 350mm. Please check the dimensions before ordering.

## Overview

This repository contains a parametric aluminium deck panel cover for the Voron Trident made by someone who's not a CAD Designer, so I'm sorry in advance for what you may find in `.f3d` file. I have seen a couple of different projects with solid mounts for Z motors, but none of them appealed to me. This design makes no compromises - just one big, sturdy piece of aluminium. I tried to keep it compatible with the stock VT, which it mostly is. There are two holes for PG connectors to separate data cables from the 230V bed one, and also just to provide more holes for additional wires.

All `.dxf` files were generated using default values from the table below. If you need to change them, open the ile using Autodesk Fusion, edit `BaseDrawing` sketch and adjust the parameters.

## Parameters

All parameters with an `_` prefix are internal and I don't recommend changing them.

### Public Parameters

| Name | Description | Default Value |
| ---- | ----------- | ------------- |
| corner_brackets_z_length | Extends cut-outs on left and right sides of Z vertical extrusion to accommodate 90° corner brackets | `0 mm` |
| cut_tolerance | How much the external perimeter should be sized down to fit CNC machine tolerance | `0.15 mm` |
| extrusion_horizontal_length | Length of a horizontal side extrusion. `120 mm` for `0 mm` bed size. Every additional `mm` will reflect bed size. For `250 mm` bed size it'll be `120 mm + 250 mm = 370 mm`. | `120 mm + 250 mm` |
| pg_drill_hole | Thread diameter of cable gland. Must include cut tolerance. | `16 mm` |
| pg_outer_diam | PG outer diameter sized to fit the nut against the frame extrusion. Must include some tolerance. | `25 mm` |
| screw_m3_diam | M3 screw hole dimension (must include cut tolerance) | `3.5 mm` |
| screw_m5_diam | M5 screw hole dimension (must include cut tolerance) | `5.5 mm` |
| screw_m5_number_long | How many M5 screw holes should be added on the left, front and right edges. Recommended `5` for `370 mm` `extrusion_horizontal_length` and one for every additional `50 mm`. | `5` |
| screw_m5_number_short | How many M5 screw holes should be added on both back edges (left and right). `2` for `370 mm` `extrusion_horizontal_length` and one for every additional `100 mm`. | `2` |

## To Do List

- No definitive values for PG cable glands (PG9 as default but not tested). Some decisions still need to be made here.
- As a PG cable gland was chosen as the cable passthrough, there is no need for the stock anchor. A custom one must be made, or the stock one can be cut down to use just the cable strain relief part, as there is only one M3 screw for mounting. Alternatively, a fully custom one can be created.

## Footnotes

In case of any issues or ideas, open an issue ticket please. The files are distributed under Apache 2.0 licence.

## Render

![Render of deck panel for 250 mm bed size](/image/deck_for_250mm.png)
