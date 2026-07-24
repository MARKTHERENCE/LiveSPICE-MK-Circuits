# LiveSPICE-MK-Circuits
![livespice-mk-circuits](https://github.com/user-attachments/assets/b2af7ccc-bb4a-4518-81c5-2767758b60af)

Schematic files drawn for use with [LiveSPICE]( https://github.com/dsharlet/LiveSPICE ), developed by Dillon ([@dsharlet]( https://github.com/dsharlet ).)

## IMPORTANT!
 - The amp models require more than one instance of LiveSPICE for the desired results, separated into preamp and poweramp sections. This is done to prevent heavy CPU usage.
   - **CAUTION:**
     - Even if most of these circuits do not return error messages when tested, too much input gain will result in Simulation Diverged errors, depending on your overdrive/distortion/booster/etc. effector of choice. Amp and pedal circuits that have this issue will be noted in the circuit list with workarounds.
   - The schematic files are no longer optimized. I have [created NAM captures of them instead]( https://www.tone3000.com/83ennui ) at the cost of component-level control over amp/pedal/etc. settings and such.
   - For REAPER users, LiveSPICE will run in parallel, so all instances of LiveSPICE will open the same circuit. To be able to use more than one circuit across multiple instances, do the following workaround:
     - `Add FX ⊳ Right-click on "VST3: LiveSPICE (mono) ⊳ Run as... ⊳ Dedicated process` 
 - Some of the circuits may be "preamp only" sections available due to the following reasons:
   - The referenced schematic does not include the diagram for the power amp section.
   - The power amp section is solid state-based.
 - May not be a regular occurence, but circuits that use dual (or more) SP3T/SP4T/SP5T switches will not work in the VST version. To compensate, they are their own separate switch controls. Please match the switch positions accordingly.

**_If any of these are the case, please refer to the schematic file for further details and instructions._**

# List of Circuits
Circuits of various guitar/bass amps and FX pedals. This list may expand over time.

 - ## Pedals & Effectors
   - AMT SS-11A and SS-11B Studio Preamps 
   - Andromeda Natural Overdrive
   - B.K. Butler Tube Driver ('79-80 "Garage" edition & bajaman's "Bias pot" mod)
     - 12AX7, 12AT7, and 12AU7 tube variations
   - BOSS BD-2 Blues Driver
     - ***Very experimental!!*** *It is a heavy circuit to simulate in real-time.*
       - *This is due to the discrete op-omp topology used for the gain stages. An alternative version of this circuit with ideal op-amp components is provided.*
   - BOSS BD-2 Blues Driver (emy's Op-Amp Variant)
     - *Noticeably less compressed due to the use of ideal op-amp components at the first opamp stage and peak filter at the output stage as trade-off for CPU usage.*
   - BOSS Distortion DS-1
   - BOSS HM-2 Heavy Metal
   - Carlsbro Suzz
   - Dallas Rangemaster Treble Booster
   - Dan Armstrong Blue Clipper
   - Dan Armstrong Green Ringer
   - Dan Armstrong Purple Peaker
   - Dan Armstrong Red Ranger
     - Grouped SP3T switches are buggy in the VST version of LiveSPICE. Match both switches when selecting which mode for intended result.
   - Dan Armstrong Yellow Humper
   - Ibanez Jemini Distortion
   - Ibanez Tube Screamer TS-10
   - MXR Distortion III
   - Nobels ODS-1 Overdrive
   - UMI Buzz Tone
   - Xotic EP Booster

 - ## Guitar & Bass Amplifiers
   - Alamo Fury 2566
   - Ampeg VH140-C
   - B-52 AT100
   - Bogner Ecstasy "83K Mod"
     - Essentially the 101B circuit with some of the following additions/changes:
       - KT88 power tubes
       - Deep switch for the Clean channel, taken from the Bogner Alchemist
       - Additional Crunch channel (Clean channel with an extra tube stage, taken from the Bogner Triple Giant)
       - Mid Shift for the Red and Blue channels, taken from the Bogner Alchemist
       - Presence control is exclusive to the Red and Blue channels, similar to the 104 model
       - Depth is an approximation of the Excursion controls from the 101A/B models
   - Bogner/Hafler Triple Giant preamp
   - Carlsbro Stingray Lead 65/100
   - Carvin VL300 Legacy 3
   - Ceriatone Marshall Plexi Super Lead "Dookie Mod"
   - Crate Stealth GT50-H
   - Diezel VH4*
     - _These are alleged, as VH4's are known to vary extensively. These circuits are bits and pieces that I could pick up from the sources mentioned in the schematic files._
   - Fender Machete
   - Fender Metalhead MH-500
   - Fender Roc Pro 1000
   - "Fortin Cali Mod" (assumed to be incorrect)
   - Gibson Super Goldtone GA Series
   - HH V/S Musician
   - Hiwatt DR103
   - Hiwatt DR201
   - Ibanez Thermion TN120
   - Kitty Hawk Quattro preamp
   - Lab Series L5
   - Laney AOR Series II
   - Laney Klipp 60 & 100
   - Laney LV300
   - Legend Rock 'n Roll 50
   - Line 6/Bogner Alchemist
   - Marshall "Jose Master Volume" mod (by Fusedbrain)
     - _Derived from 1987x._
   - Marshall 4140 Club & Country
   - Marshall 6100 30th Anniversary
   - Marshall JCM600
   - Marshall JCM900 2100
   - Marshall Lead 12
   - Marshall MA100
   - Marshall Silver Jubilee 2550/2555
   - Marshall SL5
   - Marshall Valvestate 8100
   - MESA/Boogie Mark I
   - MESA/Boogie Nomad 100
   - MESA/Boogie Stiletto Stage II Deuce
   - Orange Rockerverb 50
   - Orange Thunderverb 50
   - Park 1210 Rock Head
     - Poweramp section is work-in-progress.
   - Paul P's "Bodie" Bogen CHB-35A amp conversion
   - Peavey Decade preamp section
   - Randall BMF
   - Randall RGT100
   - Roland DAC15
   - Selmer Treble 'n Bass 50w MKII
   - Sunn Model T
   - Trainwreck Liverpool
   - Tube Works MosValve RT-2100
   - Vox AC30C2
   - Vox UL730
   - WEM Dominator 1965
     - Requires matching poweramp circuit for intended behavior and sound.
     - Number of iterations for the poweramp circuit at 16 _minimum_.
   - WEM Dominator Mk III
     - Requires matching poweramp circuit for intended behavior and sound.
     - Number of iterations for the poweramp circuit at 16 _minimum_.
---
 - ### Removed
   - Dan Armstrong Orange Squeezer
     - LiveSPICE does not seem to support circuits that consist of compression and other forms of amplitude modulation.
   - Marshall "Martin Golub/Dookie Mod" (by Misery Party / julio)
     - _Derived from JCM800 2203 / JMP Superlead 100w._
     - As per julio's request, it is no longer available for download. Please contact him on Instagram (@walkingcontrad1ction) if you want to see the schematic.
   - Pignose 7-100
     - Put on hold as I am unfamiliar with transformer components for the circuit to work as intended.

## Special Thanks
 - [Emil Rohbe]( https://www.youtube.com/@Rohbemusic ) for showcasing LiveSPICE a few years back.
 - [Ed S]( https://www.youtube.com/@eds4754/ ) for some of his demos of relatively obscure amps as inspiration.
 - [Misery Party]( https://www.youtube.com/@miseryparty3726 ) / julio ([@walkingcontrad1ction]( https://www.instagram.com/walkingcontrad1ction/ ) on Instagram) for his accurate schematic of the Martin Golub/Dookie mod.
 - [@sdleffler]( https://github.com/sdleffler ) for providing the schematics for the Orange Thunderverb 50w.

## Sound Demos
 - [Boss BD-2 Blues Driver (emy's Op-Amp Variant)]( https://youtu.be/5Iytw2b1FHE ) by me.
 - [Lab Series L5]( https://youtu.be/xhopjWutTFM ) by me.
 - [1 hr. and 14 min. high gain shootout]( https://www.youtube.com/watch?v=8n2cJ84vBjc ) by [@cmd_f5]( https://www.youtube.com/@cmd_f5 )
 - [Fender Metalhead MH-500]( https://youtu.be/JuXZqc2LVPo ) by me.
 - [Martin Golub's "Green Day Dookie" Marshall mod]( https://youtu.be/Woa6odWk67s ) by me.
 - [Peavey Decade]( https://youtu.be/CR4IU-_BRPQ ) by me.
 - [Tube Works MosValve RT-2100]( https://youtu.be/AjsVQ49L4hQ ) by me.
