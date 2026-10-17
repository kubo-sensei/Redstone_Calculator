# Circuit Diagrams

Logic schematics for each module of the VoxelCalc redstone calculator. Click a title to open its diagram.

In the redstone build, an OR gate is dust lines merging, a NOT gate is a redstone torch, and a delay is a repeater.

---

### [1. Decimal to BCD Converter](decimal_to_bcd_encoder_matrix.png)

Turns a key press (D0 to D9) into a 4-bit BCD code plus a strobe signal. Each output bit is an OR of the digit lines that have that bit set.

### [2. Decimal to 7-Segment Matrix](decimal_to_7segment_matrix.png)

Wires each digit line straight to the segments (a to g) it must light. Each dot is a tap onto that segment's OR line.

### [3. 5-Digit Shift Register System](shift_register_5x_system.png)

Keypad, encoder, pulse shortener, five registers, decoders and displays. Each new digit pushes the older ones one display to the left.

### [4. Accumulator Block Diagram](accumulator_block_diagram.png)

Builds the number as you type using `new ACC = old ACC x 10 + digit`. The `x10` is done as `x8 + x2` with bit shifts and two adders.

### [5. Full Adder Cell](full_adder_cell_gates.png)

The one-bit adder (2 XOR, 2 AND, 1 OR) repeated for every bit of the accumulator's adders, with carry rippling bit to bit.

### [6. Pulse Shortener](pulse_shortener_schematic_timing.png)

Turns a held key press into one short pulse using `OUT = IN AND NOT(IN delayed)`, so the circuit loads only once per press.
