# 555-based latches (0001)

## Description

The circuit contains of three latches: astable, monostable and bistable. Each of them is build around a separate 555
integrated circuit with configured parameters.

The device is powered with 5-15V. The voltage is provided to screw connector J1 `DC_IN`, pin 1 is +, pin 2 is -.
The maximum output current of each output signal is ~15mA (depending on the power voltage) [TODO: measure].

The astable latch is built around integrated circuit U1. Potentiometers RV1 and RV2, together with resistors R1 and R2
and capacitor C1 regulate the frequency and duty cycle of the `ASTBL_OUT` output signal. The frequency range is
1Hz-1kHz. The `ASTBL_OUT` signal is provided to screw connector J2. The state of `ASTBL_OUT` signal is visualised with
D1 LED.

The bistable latch is build around integrated circuit U2. Pushing SW1 button triggers high output state of `BSTBL_OUT`
signal. Pushing SW2 button triggers low output state of `BSTBL_OUT` signal. The `BSTBL_OUT` signal is provided to screw
connector J3 [TODO: replace]. The state of `BSTBL_OUT` signal is visualised with D2 LED.

The monostable latch is build around integrated circuit U3. Potentiometer RV3, together with resistor R6 and capacitor
C4 regulate the pulse duration of the `MSTBL_OUT` output signal. The pulse is triggered by pushing SW3 button. The pulse
duration range is 25ms-25s. The `MSTBL_OUT` signal is provided to screw connector J4 [TODO: replace]. The state of
`MSTBL_OUT` signal is visualised with D3 LED.

## Schematic

<img src="images/img.png" alt="Schematics" style="width:300px;"/>

## PCB

## Bill of Materials

## Outcomes

The goal of this project is to compare different techniques of preparing printed circuit boards. The tested techniques
are:
- Cleaning the surface
  - [TODO: list]
- Paths printouts
  - chalk paper [TODO: parameters]
  - transparent film [TODO: patameters]
- Transferring paths
  - [TODO: list]
- Etching
  - [TODO: list]
- Copper protection
  - Solder mask Mechanik
  - Solder mask [TODO: name]
  - Tine

## References

- [555 Timer Tutorial](https://www.build-electronic-circuits.com/555-timer/)
- [555 Timer Calculator](https://www.build-electronic-circuits.com/circuit-calculator-conversion/555-timer-calculator/)
- [KiCad Schematic Editor documentation](https://docs.kicad.org/9.0/en/eeschema/eeschema.html)

