# Heavy Duty Deck Panel for Voron Trident (Preview)

> [!CAUTION]
> I put a lot of effort into keeping all dimensions correct, but I haven't tested it in real life **yet** — only against Voron's official STEP file for a 250mm build and my own 350mm 4040 build. Please check the dimensions before ordering.

## Overview

This repository contains a parametric aluminium deck panel cover for the Voron Trident, made by someone who is not a CAD designer — so I apologize in advance for anything you may find in the `.f3d` file. I have seen a few similar projects with solid mounts for Z motors, but none of them appealed to me. This design makes no compromises: just one big, sturdy piece of aluminium.

All `.dxf` files were generated using the default values from the table below. If you need to change them, open the file in Autodesk Fusion, adjust the parameters or edit the `BaseDrawing` sketch.

## Features

- One mounting plate for the Z motors ensures all of them are level and aligned.
- Seals the bottom of the chamber, reducing hot air leakage.
- Two holes near the rear center for PG cable glands, separating high voltage and data cables — left (PG7) for 230V bed power, right (PG11) for thermistors, bed fans, CAN cables, etc.
- Two PG9 holes on the rear corners for motor and chamber thermistor cables. These will fit eight AWG24 cables and four thermistors — enough for an AWD setup, motor and corner chamber temperature sensors. See [images](/image/) for visualisation.

## BOM

Assuming deck thickes of 4 mm and utilising DXFs from the repository.

| Part Name               | 250 mm | 300 mm | 350 mm |
| ----------------------- | ------ | ------ | ------ |
| M5x8 BHCS               | 21     | 24     | 27     |
| M5 Roll in Spring T-Nut | 21     | 24     | 27     |
| PG 7 Cable Gland        | 1      | 1      | 1      |
| PG 9 Cable Gland        | 2      | 2      | 2      |
| PG 11 Cable Gland       | 1      | 1      | 1      |

## Customisng the design

### Public Parameters

| Name | Description | Default Value |
| ---- | ----------- | ------------- |
| corner_brackets_z_length | Extends cut-outs on left and right sides of Z vertical extrusion to accommodate 90° corner brackets | `0 mm` |
| cut_tolerance | How much the external perimeter should be sized down to fit CNC machine tolerance | `0.15 mm` |
| extrusion_horizontal_length | Length of a horizontal side extrusion. `120 mm` for `0 mm` bed size. Every additional `mm` will reflect bed size. For `250 mm` bed size it'll be `120 mm + 250 mm = 370 mm`. | `120 mm + 250 mm` |
| screw_m3_diam | M3 screw hole dimension (must include cut tolerance) | `3.5 mm` |
| screw_m5_diam | M5 screw hole dimension (must include cut tolerance) | `5.5 mm` |
| screw_m5_number_long | How many M5 screw holes should be added on the left, front and right edges. Recommended `5` for `370 mm` `extrusion_horizontal_length` and one for every additional `50 mm`. | `5`/`6`/`7` |
| screw_m5_number_short | How many M5 screw holes should be added on both back edges (left and right). | `3` |

All parameters with an `_` prefix are internal and I don't recommend changing them. I left a few internal variables with different PG Cable Glands sizes which can be used in case of someone would like to modify some hole sizes. All values include small offset.

- `_pgX_drill_hole` - Hole for mounting PG Cable Gland with 0.5 mm offset
- `_pgX_outrer_diam` - Width of the bottom nut with small offset to distance it from extrusion

| Name               | Value   |
| ------------------ | ------- |
| _pg7_drill_hole    | 13 mm   |
| _pg7_outer_diam    | 23 mm   |
| _pg9_drill_hole    | 15.5 mm |
| _pg9_outer_diam    | 27 mm   |
| _pg11_drill_hole   | 19 mm   |
| _pg11_outer_diam   | 30 mm   |
| _pg13_5_drill_hole | 21 mm   |
| _pg13_5_outer_diam | 34 mm   |

## Footnotes

[Kradex PG cable glands](https://www.kradex.com.pl/product/accessories/d%c5%82awnica?lang=en) were used in this project, so please compare the dimensions. [Here is  direct link](https://www.kradex.com.pl/products/1102/D%C5%82awnica_Dimension_table.pdf) to the dimension table.

The files are distributed under Apache 2.0 licence.

In case of any issues or ideas, open an issue ticket please.

## Render

![Render of the deck panel for 250 mm bed size](/image/deck_for_250mm.png)
