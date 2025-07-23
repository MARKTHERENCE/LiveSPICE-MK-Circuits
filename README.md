# LiveSPICE-MK-Circuits
![livespice-mk-circuits](https://github.com/user-attachments/assets/b2af7ccc-bb4a-4518-81c5-2767758b60af)

Schematic files drawn for use with [LiveSPICE]( https://github.com/dsharlet/LiveSPICE ), developed by Dillon ([@dsharlet]( https://github.com/dsharlet ).)

## IMPORTANT!
 - The amp models require more than one instance of LiveSPICE for the desired results, separated into preamp and poweramp sections. This is done to prevent heavy CPU usage.
   - **CAUTION:**
     - Even if most of these circuits do not return error messages when tested, too much input gain will result in Simulation Diverged errors, depending on your overdrive/distortion/booster/etc. effector of choice. Amp and pedal circuits that have this issue will be noted in the circuit list with workarounds.
     - Other preamps _need_ to be loud to push their matching poweramp circuit. This will be noted in the circuit list.
   - For real-time usage, the following settings are:
     - Oversampling at 1x.
     - Number of Iterations:
       - 16 _minimum_ for preamps.
       - 32 _minimum_ for overdrive/distortion circuits.
       - Number of Iterations around 1 to 8 for poweramps (generally.) Exceptions will be noted in the circuit list.
         - These are more or less starting points. Your mileage may vary, so do experiement with whichever works best for you sound and performance-wise.
   - For REAPER users, LiveSPICE will run in parallel, so all instances of LiveSPICE will open the same circuit. To be able to use more than one circuit across multiple instances, do the following workaround:
     - `Add FX ⊳ Right-click on "VST3: LiveSPICE (mono) ⊳ Run as... ⊳ Dedicated process` 
 - Some of the circuits may be "preamp only" sections available due to the following reasons:
   - The referenced schematic does not include the diagram for the power amp section.
   - The power amp section is solid state-based.
 - There may be some circuits that are broken down into several parts, due to either unintended behaviors or CPU usage. For convenience, I will note which circuits this workaround applies to.
 - May not be a regular occurence, but circuits that use dual (or more) SP3T/SP4T/SP5T switches will not work in the VST version. To compensate, they are their own separate switch controls. Please match the switch positions accordingly.

**_If any of these are the case, please refer to the schematic file for further details and instructions._**

# List of Circuits
Circuits of various guitar/bass amps and FX pedals. This list may expand over time.

 - ## Pedals & Effectors
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
   - Ibanez Tube Screamer TS-10
   - MXR Distortion III
   - Nobels ODS-1 Overdrive
   - UMI Buzz Tone
   - Xotic EP Booster

 - ## Guitar & Bass Amplifiers
   - Alamo Fury 2566
     - Requires matching poweramp circuit for intended behavior and sound.
     - Number of iterations for the poweramp circuit at 16 _minimum_.
   - Ampeg VH140-C
   - Carlsbro Stingray Lead 65/100
   - Ceriatone Marshall Plexi Super Lead "Dookie Mod"
   - Crate Stealth GT50-H
   - Diezel VH4*
     - _These are alleged, as VH4's are known to vary extensively. These circuits are bits and pieces that I could pick up from the source mentioned in the schematic files._
   - Fender Metalhead MH-500
   - Fender Roc Pro 1000
   - "Fortin Cali Mod" (assumed to be incorrect
   - HH V/S Musician
   - Lab Series L5
   - Laney AOR Series II
   - Laney Klipp 60 & 100
   - Laney LV300
   - Legend Rock 'n Roll 50
   - Marshall "Jose Master Volume" mod (by Fusedbrain)
     - _Derived from 1987x._
   - Marshall "Martin Golub/Dookie Mod" (by Misery Party / julio)
     - _Derived from JCM800 2203 / JMP Superlead 100w._
   - Marshall 4140 Club & Country
   - Marshall 6100 30th Anniversary
   - Marshall JCM600
   - Marshall Silver Jubilee 2550/2555
   - Marshall Valvestate 8100
   - MESA/Boogie Mark I
     - _This circuit seems to be ever-changing as each model may have other features not present from others. I omitted the Graphic EQ/Gain Boost circuits for this one._
     - Should you want the Graphic EQ feature, use an external EQ plug-in (i.e. ReaEQ) to substitute as the Graphic EQ section of the amp. The following frequencies and bandwidth are:
       - 87.61Hz / Q = 1.171 (Low shelf)
       - 371.7Hz / Q = 1.938 (Band)
       - 723.4Hz / Q = 2.128 (Band)
       - 1576Hz / Q = 0.6733 (Band)
       - 4823Hz / Q = 1.000 (High shelf)
         - _Real frequencies and bandwidth are measured by [gugabrandao in the The Boogie Board forums]( https://boogieforum.com/threads/mesa-boogie-graphic-eq-real-frequencies.69355/ )._
   - MESA/Boogie Nomad 100
     - *Graphic EQ frequencies and bandwidth are specified in the Mark I notes.*
   - MESA/Boogie Stiletto Stage II Deuce
   - Park 1210 Rock Head
     - Poweramp section is work-in-progress.
   - Peavey Decade preamp section
   - Roland DAC15
   - Selmer Treble 'n Bass 50w MKII
     - Poweramp section is work-in-progress.
   - Tube Works MosValve RT-2100
   - Vox AC30C2
     - Poweramp section is work-in-progress.
   - Vox UL730
     - Requires matching poweramp circuit for intended behavior and sound.
       - *The poweramp circuit is fed with 25V at the input signal for the intended gain/distortion characteristic of the amp.*
     - Number of iterations for the poweramp circuit at 16 _minimum_.
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
   - Pignose 7-100
     - Put on hold as I am unfamiliar with transformer components for the circuit to work as intended.

## Special Thanks
 - [Emil Rohbe]( https://www.youtube.com/@Rohbemusic ) for showcasing LiveSPICE a few years back.
 - [Ed S]( https://www.youtube.com/@eds4754/ ) for some of his demos of relatively obscure amps as inspiration.
 - [Misery Party]( https://www.youtube.com/@miseryparty3726 ) / julio ([@walkingcontrad1ction]( https://www.instagram.com/walkingcontrad1ction/ ) on Instagram) for his accurate schematic of the Martin Golub/Dookie mod.

## Sound Demos
 - [Boss BD-2 Blues Driver (emy's Op-Amp Variant)]( https://youtu.be/5Iytw2b1FHE ) by me.
 - [Lab Series L5]( https://youtu.be/xhopjWutTFM ) by me.
 - [1 hr. and 14 min. high gain shootout]( https://www.youtube.com/watch?v=8n2cJ84vBjc ) by [@cmd_f5]( https://www.youtube.com/@cmd_f5 )
 - [Fender Metalhead MH-500]( https://youtu.be/JuXZqc2LVPo ) by me.
 - [Martin Golub's "Green Day Dookie" Marshall mod]( https://youtu.be/Woa6odWk67s ) by me.
 - [Peavey Decade]( https://youtu.be/CR4IU-_BRPQ ) by me.
 - [Tube Works MosValve RT-2100]( https://youtu.be/AjsVQ49L4hQ ) by me.
