# 555-based latches (0001)

## Description

The circuit contains of three latches: astable, monostable and bistable. Each of them is build around a separate 555
integrated circuit with configured parameters.

<img src="images/schematic.png" alt="Schematics" style="width:600px;"/>

The astable latch is built around integrated circuit U1. Potentiometers RV1 and RV2, together with resistors R1 and R2
and capacitor C1 regulate the frequency and duty cycle of the `ASTBL_OUT` output signal. The frequency range is
1Hz-1kHz. The `ASTBL_OUT` signal is provided to screw connector J2. The state of `ASTBL_OUT` signal is visualised with
D1 LED.

The bistable latch is build around integrated circuit U2. Pushing SW1 button triggers high output state of `BSTBL_OUT`
signal. Pushing SW2 button triggers low output state of `BSTBL_OUT` signal. The `BSTBL_OUT` signal is provided to screw
connector J3. The state of `BSTBL_OUT` signal is visualised with D2 LED.

The monostable latch is build around integrated circuit U3. Potentiometer RV3, together with resistor R6 and capacitor
C4 regulate the pulse duration of the `MSTBL_OUT` output signal. The pulse is triggered by pushing SW3 button. The pulse
duration range is 25ms-25s. The `MSTBL_OUT` signal is provided to screw connector J4. The state of `MSTBL_OUT` signal is
visualised with D3 LED.

The maximum output current of each output signal is ~15mA (input voltage/1000).

## Assembly

The circuit should be assembled on a single-sided, THT printed circuit board.

<img src="images/pcb.png" alt="PCB layout" style="width:600px;"/>

## Running

The device should be powered with 5-15VDC provided to J1 `DC_IN` (center-positive DC jack 2.1/5.5).

After providing the voltage all output signals should be available (observe LED visualisations).

## Bill of Materials

| Reference            | Qty | Value     |
|----------------------|-----|-----------|
| C1                   | 1   | 470nF     |
| C2,C3,C5             | 3   | 10nF      |
| C4                   | 1   | 22uF      |
| D1                   | 1   | RED       |
| D2                   | 1   | GREEN     |
| D3                   | 1   | YELLOW    |
| J1                   | 1   | DC_IN     |
| J2                   | 1   | ASTBL_OUT |
| J3                   | 1   | BSTBL_OUT |
| J4                   | 1   | MSTBL_OUT |
| R1,R2,R6,R7,R8,R9    | 6   | 1k        |
| R3,R4,R5,R10,R11,R12 | 6   | 10k       |
| RV1,RV2,RV3          | 3   | 1M        |
| SW1,SW2,SW3          | 3   | SW_Push   |
| U1,U2,U3             | 3   | NE555P    |

## References

- [555 Timer Tutorial](https://www.build-electronic-circuits.com/555-timer/)
- [555 Timer Calculator](https://www.build-electronic-circuits.com/circuit-calculator-conversion/555-timer-calculator/)
- [KiCad Schematic Editor documentation](https://docs.kicad.org/9.0/en/eeschema/eeschema.html)
- [KiCad YouTube tutorial 1](https://youtube.com/playlist?list=PL3bNyZYHcRSUhUXUt51W6nKvxx2ORvUQB&si=8JaQM5K1sOJ2W4WG)
- [KiCad YouTube tutorial 2](https://youtube.com/playlist?list=PLEBQazB0HUyQ5YJSdCBb79orXaR3Uk5vm&si=labIkKh_z3xuK7w0)
- [KiCad YouTube tutorial 3](https://www.youtube.com/playlist?list=PLUOaI24LpvQPls1Ru_qECJrENwzD7XImd)
- Preparing PCBs using thermal transfer (Youtube, in Polish):
    - [1](https://www.youtube.com/watch?v=IV76AiosMgo)
    - [2](https://www.youtube.com/watch?v=NjvKmZZtHUM)
    - [3](https://www.youtube.com/watch?v=1L4GrPDR9TE) - great effect
    - [4](https://www.youtube.com/watch?v=EEXGR3g5FFA) - interesting way of positioning chalk paper 

## PCB preparation

During this project different techniques of preparing printed circuit boards were compared and tested, including:

- Cleaning the surface
  - cleaning milk
  - sandpaper (1000)
  - IPA
  - Nitro
  - cleaning milk + IPA
  - sandpaper + IPA
- Paths printouts
  - chalk paper [TODO: parameters] *
  - transparent film [TODO: patameters]
  - Paper from magazine 
- Transferring paths
  - Ironing on the board, from the top, 2.5 dots temperature
  - Ironing on the reverted iron, 2.5 dots temperature, after sticking chalk paper with capton tape  
  - Ironing on the reverted iron, 2.5 dots temperature, placing chalk paper quickly on the hot copper  
  - Ironing on the reverted iron, 2.5 dots temperature, after sticking tonner first
  - Ironing on the reverted iron, 3 dots temperature, after sticking tonner first with 2.5 dots *
- Removing chalk paper
  - In the water (toothbrush at the end)
  - In the water
  - In the warm water with few drops of dish soap (toothbrush at the end)
  - In the warm water with few drops of dish soap
  - In the cold water with washing powder (toothbrush at the end)
  - In the cold water with washing powder
  - vinegar 
- Fixing broken paths
  - marker
  - corrector
- Preparing chemistry
  - NaS to 50 C in a bottle, half a bag to 1.5L
- Etching
  - FeCl
  - NaS (B327) (laying on the top)
  - NaS (B327) (drawning and moving)
  - NaS (B327) (drawning and moving, with boiled water around)
  - NaS (B327) (hanging from the top)
  - NaS (B327) (hanging from the top, with boiled water around)
- Removing tonner
  - Nitro
  - sandpaper 
- Copper protection
  - Solder mask Mechanik
  - Solder mask [TODO: name] *
  - Tine
  - colophony in nitro
  - Nothing
- Solder mask removal
  - Film stencil *
  - scraping
- Drills 
  - Mounting points before etching, rest after tinning 
  - Before etching *
  - Before tining
  - After tinning
- Silk screen
  - Ironed from film under solder mask
  - Ironed from film on the solder mask
  - Ironed from chalk paper under solder mask
- Protecting from oxidising
  - drawning in methylated spirits (denaturat) *
  - nothing
  - colophony in nitro

## Photo-relation

Circuits were tested before assembly. Testing astable latch:

<img src="images/photorelation/01_lab.jpg" alt="Testing lab" style="width:300px;"/>

555 integrated circuit in the bread board:

<img src="images/photorelation/02_555_board.jpg" alt="555 in bread board" style="width:300px;"/>

Minimal astable latch configuration resistance measurement:

<img src="images/photorelation/03_astable_r_min.jpg" alt="Min astable resistance" style="width:300px;"/>

Maximal astable latch configuration resistance measurement:

<img src="images/photorelation/04_astable_r_max.jpg" alt="Max astable resistance" style="width:300px;"/>

Astable latch testing circuit ready:

<img src="images/photorelation/05_astable_ready.jpg" alt="Astable testing circuit ready" style="width:300px;"/>

Last astable latch continuity testing before providing power:

<img src="images/photorelation/06_astable_continuity.jpg" alt="Continuity test" style="width:300px;"/>

Astable latch maximal frequency measurement:

<img src="images/photorelation/07_astable_f_max.jpg" alt="Max astable frequency" style="width:300px;"/>

Astable latch minimal frequency measurement:

<img src="images/photorelation/08_astable_f_min.jpg" alt="Min astable frequency" style="width:300px;"/>

Astable latch maximal current measurement:

<img src="images/photorelation/09_astable_i_max.jpg" alt="Max astable current" style="width:300px;"/>

Bistable latch testing:

<img src="images/photorelation/10_bistable_test.jpg" alt="Testing bistable latch" style="width:300px;"/>

Monostable latch testing:

<img src="images/photorelation/11_monostable_test.jpg" alt="Testing monostable latch" style="width:300px;"/>
