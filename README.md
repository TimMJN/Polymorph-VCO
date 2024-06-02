# Polymorph VCO
 Voltage-controlled oscillator based on SSI2130 VCO-core for Kosmo and Eurorack modular synths. The module design features:
- Main oscillator with various waveforms:
  - Triangle
  - Saw
  - Square/pulse
  - Sine/half-sine
- Suboscillator with 3 different waveforms:
  - Triangle
  - Saw
  - Square
- A voltage-controlled mixer with:
  - 5 channels (triangle, saw, pulse/square, (half) sine and sub)
  - an attenuverter of each channel
  - additional individual outputs for each channel
- Coarse/fine tune and an octave switch
- Exponential FM
- Through-zero linear FM/PM
- Hard and soft sync

View the [schematic](schematic+BOM/Polymorph_VCO.pdf) and [bill of materials](https://htmlpreview.github.io/?https://github.com/TimMJN/Polymorph-VCO/blob/main/schematic%2BBOM/Polymorph_VCO_BOM.html) on this repository.

# Notes and Frequently Asked Questions
## The build

### Calibration
Calibration requires:
- a precision voltage source (e.g. a quantiser, or a keyboard controller with CV-out, like the Arturia Keystep)
- a tuner (app) (or frequency counter, or a really good set of ears)
- a small screwdriver

Start of in the low audible frequency range. Play notes 1 octave apart (CVs 1V apart), and adjust `Exp scale trim` until the output is 1 octave (factor 2 in frequency) apart. Once you're content with the result for 1 octave, move up to playing notes 2 octaves apart, then 3 and 4. During this process don't touch the tune of octave knobs.

Next, move to the high audible frequency range. Play notes 8 octaves apart (CVs 8V apart), and adjust `HF trim` until the output is 8 octaves (factor 256 in frequency) apart. Again, don't touch the tune or octave knobs. The VCO should now track accurately over (at least) an 8-octave range.

Next, calibrate the octave switch. Play a note and, without changing CV or touching the tune knobs, move the octave switch one position. Adjust `Octave trim` until the output is 1 octave apart. Once you're content with the result for 1 octave, move up to 2 positions, then 3 and 4.

Lastly, the `Subtriangle filter trim` can be adjusted. This filter removes some of the high-frequency artefacts from the subtriangle output. Set the suboscillator waveform to triangle, and listen to its output. Adjust the trimmer until any harsh overtones in the lower frequency range are gone, but the suboscillator is still audible in the higher frequency range.

# License
All designs in this repository are released under GPL-3.0 licence. Feel free to use and adapt them to your heart's desire. I only ask to refrain from mass-production and commercialisation of PCBs/modules, as I rely on PCB sales for funding new module designs. If you use (parts of) my designs in your own modules, please credit me on your schematics and PCBs to help users find the original creator. I call upon your good conscience to make fair use of my work shared here.

# Support
If you like the resources I have made available here, and wish to support the development of new modules, feel free to buy me a few components through a small donation. I mainly design modules for fun, but you probably already know it can be a costly endeavour. All small contributions help me, thank you very much!

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/donate?hosted_button_id=FZJELWSAH4UKU)
