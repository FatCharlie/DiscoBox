# Lets build this thing

### The Parts List

#### Were going to skip the laser+crystal phase entirely and just get a photon pair source 

## The Core pieces 

* The Photon source: [spdc810](https://www.thorlabs.com/item/spdc810) , ~ $26k
* The Spatial Light Modulator to twist the light (OAM) and the concentric ring count (radials): Hamamatsu X15213 series LCOS-SLM, ~ ??? (have to get a quote) maybe $15k
* Detection : Excelitas SPCM-AQRH series single-photon counting modules. Confirmed current pricing (DigiKey): standard dark-count tier (<1500 cps) ≈ $3,110/channel; 4-8 depending on starting point. Exact number depends on the final heralding-scheme design - pin that down before ordering, not after. ($12-24k)
* Timing: Swabian Instruments Time Tagger (PicoQuant's TCSPC line is the alternative) - picosecond-resolution multi-channel time tagging, ~$10–15k

## Standard opto-mechanics (catalog items, Thorlabs/Newport-class, prices not itemized here - commodity-level)

- Non-polarizing 50:50 beamsplitter cubes, 810 nm-optimized (for the Bell-state-measurement interference)
- Narrowband bandpass/notch filters to reject 405 nm pump, pass 810 nm
- Half-wave and quarter-wave plates for polarization control/compensation
- Mirrors, kinematic mounts, posts, translation stages
- Optical breadboard sized to the full beam path
- Laser safety: already sourced, see raw/Certified Laser Safety Glasses
