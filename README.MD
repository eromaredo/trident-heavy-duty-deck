# Heavy Duty Deck Panel for Voron Trident (Preview)

> [!CAUTION]
> I put a lot of effort into keeping all dimensions correct, but I haven't tested it in real life (yet) - only against Voron's official STEP file for a 250mm build and my own 4040 350mm. Please check the dimensions before ordering.

## Overview

This repository contains a parametric aluminium deck panel cover for the Voron Trident, made by someone who is not a CAD designer — so I apologize in advance for anything you may find in the `.f3d` file. I have seen a few similar projects with solid mounts for Z motors, but none of them appealed to me. This design makes no compromises: just one big, sturdy piece of aluminium. I tried to keep it compatible with the stock VT, and it mostly is. There are two holes for PG cable glands to separate data cables from the 230V bed power cable, and to provide extra room for additional wiring.

All `.dxf` files were generated using the default values from the table below. If you need to change them, open the file in Autodesk Fusion, edit the `BaseDrawing` sketch, and adjust the parameters.

## Features

- One mounting plate for the Z motors ensures all of them are level and aligned.
- Seals the bottom of the chamber, reducing hot air leakage.
- Two holes for PG cable glands to separate high voltage and data cables — left (PG7) for 230V bed power, right (PG13.5) for motors, thermistors, etc.

## BOM

Assuming deck thickes of 4 mm and utilising DXFs from the repository.

| Part Name               | 250 mm | 300 mm | 350 mm |
| ----------------------- | ------ | ------ | ------ |
| M5x8 BHCS               | 19     | 24     | 27     |
| M5 Roll in Spring T-Nut | 19     | 24     | 27     |
| PG 7 Cable Gland        | 1      | 1      | 1      |
| PG 13.5 Cable Gland     | 1      | 1      | 1      |

## Customisng the design

### Public Parameters

All parameters with an `_` prefix are internal and I don't recommend changing them.

| Name | Description | Default Value |
| ---- | ----------- | ------------- |
| corner_brackets_z_length | Extends cut-outs on left and right sides of Z vertical extrusion to accommodate 90° corner brackets | `0 mm` |
| cut_tolerance | How much the external perimeter should be sized down to fit CNC machine tolerance | `0.15 mm` |
| extrusion_horizontal_length | Length of a horizontal side extrusion. `120 mm` for `0 mm` bed size. Every additional `mm` will reflect bed size. For `250 mm` bed size it'll be `120 mm + 250 mm = 370 mm`. | `120 mm + 250 mm` |
| screw_m3_diam | M3 screw hole dimension (must include cut tolerance) | `3.5 mm` |
| screw_m5_diam | M5 screw hole dimension (must include cut tolerance) | `5.5 mm` |
| screw_m5_number_long | How many M5 screw holes should be added on the left, front and right edges. Recommended `5` for `370 mm` `extrusion_horizontal_length` and one for every additional `50 mm`. | `5`/`6`/`7` |
| screw_m5_number_short | How many M5 screw holes should be added on both back edges (left and right). `2` for `370 mm` `extrusion_horizontal_length`, `3` for `430mm` and `470 mm`. | `2`/`3` |

## To Do List

- Look for AWD options (holes on the front)
- Add additional holes on rear right and left corners for motors and chamger thermistors

## Footnotes

In case of any issues or ideas, open an issue ticket please. The files are distributed under Apache 2.0 licence.

## Render

![Render of deck panel for 250 mm bed size](/image/deck_for_250mm.png)
