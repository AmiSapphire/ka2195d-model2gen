# ka2195d-model2gen

## Introduction
Project that aims to fix the Model 2 Sega Genesis's composite video clock that uses the console's crystal oscillator instead of using an external one.

This repo contains the schematic, PCBs, and Gerber files for the Composite Video clock fix for Model 2 Sega Genesis consoles: revision VA0, VA1, and VA1.8 boards that contain the infamous Samsung KA2195D NTSC video encoder. The Gerber files can be used for other PCB fabs.

Notes:
* These are KiCad 6 files, so KiCad 5 and earlier will not work with these.
* This does not fix the RGB jailbars, as it is a somewhat different (yet related) issue.
* This particular PCB uses Imperial 1206 size SMD components.
* Removal of the original 10K resistor on R61 on the console's board is **_required_**.
* R61_L is +2.5V as VREF, connecting to SBCR.
* R61_R is GND, connecting to C24, then KA2195 pin 6.

--

## Details
This [twitter thread (through nitter.net)](https://nitter.net/AmiSapphire/status/1496249012688756744) is the original instruction-like thread (with video examples as well). In short:

* you remove R61 from the board
* mount the board to the console's CPU
* have one wire connect to R61's left pad from the R61_L pad
* have one wire connect to R61's right pad from the R61_R pad
* have one wire connect as ground to wherever ground can be, e.g. C4's right pad, C1's left pad

--

## Images
R61 Pad Indicators:

![R61-pad-indicators](https://user-images.githubusercontent.com/103345205/163667306-d909fd19-85b2-42dc-beda-787602c3ff71.png)
![r61_pcb_500px](https://user-images.githubusercontent.com/103345205/163667839-e4dcb0f2-0493-4336-8faf-22b7dd88d765.png)

R61 End Result:

![R61-end-result](https://user-images.githubusercontent.com/103345205/163667312-a2ac3231-c51f-40cc-a7a8-cef1a68949b5.png)

--

## OSH Park order links
Original (test): https://oshpark.com/shared_projects/IpuYYXQL

SMD Hand Solder: https://oshpark.com/shared_projects/toKAOWpJ

Through Hole: https://oshpark.com/shared_projects/uN65Pqal
