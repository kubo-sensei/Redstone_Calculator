# Schematics

Litematica `.litematic` files for each module of the Redstone Calculator. Load them into your own world to rebuild or reuse a single module.

Each module links to its circuit diagram in [circuit_diagrams/](../circuit_diagrams/).

---

## Files

| Schematic                                                                                                          | What it is                                                | Diagram                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [17_bit_accumulator.litematic](17_bit_accumulator.litematic)                                                       | 17-bit accumulator: `new ACC = old ACC x 10 + digit`      | [Accumulator](../circuit_diagrams/accumulator_block_diagram.png), [Full adder](../circuit_diagrams/full_adder_cell_gates.png) |
| [Decimal_Input_7_seg_with_shift_registor(5x).litematic](Decimal_Input_7_seg_with_shift_registor%285x%29.litematic) | Five-digit shift register driving five 7-segment displays | [Shift register system](../circuit_diagrams/shift_register_5x_system.png)                                                     |
| [Decimal_input_7_segment_display.litematic](Decimal_input_7_segment_display.litematic)                             | Single 7-segment display driven from decimal lines        | [7-segment matrix](../circuit_diagrams/decimal_to_7segment_matrix.png)                                                        |
| [Decimal_input_to_Binary_converter.litematic](Decimal_input_to_Binary_converter.litematic)                         | Keypad digit to 4-bit BCD encoder with strobe             | [BCD encoder](../circuit_diagrams/decimal_to_bcd_encoder_matrix.png)                                                          |
| [Pulse_shortner.litematic](Pulse_shortner.litematic)                                                               | Turns a held key press into one short pulse               | [Pulse shortener](../circuit_diagrams/pulse_shortener_schematic_timing.png)                                                   |

---

## How to Use

1. Install the Litematica mod (Minecraft Java 1.16.5). It is in [mods/](../mods/).
2. Copy the `.litematic` files into the `schematics` folder inside your `.minecraft` directory.
3. In game, press `M` to open the Litematica menu and choose **Load Schematics**.
4. Select a file and load it, then place it where you want to build.
5. Follow the ghost blocks to build the module, or paste it directly if you are in creative mode.

---

## Notes

- Build every module on flat, clear ground with enough space around it. Redstone dust and torches can be affected by neighboring blocks.
- Keep the whole build inside loaded chunks or it will stop mid-calculation.
- Check [PROGRESS.md](../PROGRESS.md) for which modules are finished and tested.
