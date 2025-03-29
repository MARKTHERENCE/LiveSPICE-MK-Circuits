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
       - 16 or 32 _minimum_ for preamps and overdrive/distortion circuits.
       - Number of Iterations around 8 _minimum_ for EQ/tonestack and output circuits.
       - Number of Iterations around 1 to 8 for poweramps (generally.) Exceptions will be noted in the circuit list.
         - These are more or less starting points. Your mileage may vary, so do experiement with whichever works best for you sound and performance-wise.
   - For REAPER users, LiveSPICE will run in parallel, so all instances of LiveSPICE will open the same circuit. To be able to use more than one circuit across multiple instances, do the following workaround:
     - `Add FX ⊳ Right-click on "VST3: LiveSPICE (mono) ⊳ Run as... ⊳ Dedicated process` 
 - Some of the circuits may be "preamp only" sections available due to the following reasons:
   - The referenced schematic does not include the diagram for the power amp section. 
   - The tube stages use the phase inverter of the power amp to cascade more gain.
   - The power amp section is solid state-based.
 - There may be some circuits that are broken down into several parts. It's a compromise I had to resort to for CPU usage. For convenience, I will note which circuits this workaround applies to.
 - May not be a regular occurence, but circuits that use dual (or more) SP3T/SP4T/SP5T switches will not work in the VST version. To compensate, they are their own separate switch controls. Please match the switch positions accordingly.

**_If any of these are the case, please refer to the schematic file for further details and instructions._**

# List of Circuits
Circuits of various guitar/bass amps and FX pedals. This list may expand over time.

 - ## Pedals & Effectors
   - Andromeda Natural Overdrive
   - Dallas Rangemaster Treble Booster
   - Dan Armstrong Blue Clipper
   - Dan Armstrong Green Ringer
   - Dan Armstrong Purple Peaker
   - Dan Armstrong Red Ranger
   - Dan Armstrong Yellow Humper
   - MXR Distortion III
   - Nobels ODS-1 Overdrive

 - ## Guitar & Bass Amplifiers
   - Alamo Fury 2566
     - Requires matching poweramp circuit for intended behavior and sound.
     - Number of iterations for the poweramp circuit at 16 _minimum_.
   - Ampeg VH140-C
     - Signal chain for Channel A:
       - Distortion ⊳ EQ & Output
   - Ceriatone Marshall Plexi Super Lead "Dookie Mod"
   - Crate Stealth GT50-H
     - Signal chain for Channel 2:
       - 1st Tube ⊳ Distortion ⊳ 2nd Tube, EQ, & Master Volume
     - Simulation Diverged workarounds, placed before the Distortion circuit:
       - Limiter threshold at -12dB
       - 20Hz high-pass filter for dynamics. (optional)
   - Diezel VH4*
     - _These are alleged, as VH4's are known to vary extensively. These circuits are bits and pieces that I could pick up from the source mentioned in the schematic files._
   - Fender Metalhead MH-500
   - "Fortin Cali Mod" (assumed to be incorrect)
   - Legend Rock 'n Roll 50
     - Signal chain:
       - 1st & 2nd Tube Stages ⊳ Phase Inverter
   - Marshall "Jose Master Volume" mod (by Fusedbrain)
     - Derived from 1987x
   - Marshall "Martin Golub/Dookie Mod" (by Misery Party / julio)
     - Derived from JCM800 2203 / JMP Superlead 100w
   - Marshall 4140 Club & Country
   - Marshall 6100 30th Anniversary
   - Marshall JCM600
     - Simulation Diverged workarounds, placed before the Overdrive preamp circuit:
       - Limiter threshold at -15dB.
       - 20Hz high-pass filter for dynamics. (optional)
   - Marshall Silver Jubilee 2550/2555
     - Simulation Diverged workarounds, placed before the preamp circuit:
       - Limiter threshold at -15dB.
       - 20Hz high-pass filter for dynamics. (optional)
   - Marshall Valvestate 8100
     - Signal chain:
       - Normal / Boost ⊳ Master Volume
       - The Master Volume circuit is optional, but I find that it adds some subtle saturation.
   - Park 1210 Rock Head
   - Peavey Decade preamp section
   - ~~Pignose 7-100 preamp section~~ (faulty circuit as of 3/19/2025, currently attempting to fix this.)
   - Roland DAC15
     - Signal chain:
       - Gain Stages / Gain Stages + Clipper ⊳ EQ & Master Volume
   - Selmer Treble 'n Bass 50w MKII
   - Tube Works MosValve RT-2100
     - Signal chain:
       - Clean Channel / Drive Channel [Input ⊳ Tube Stages  ⊳ EQ & Master Volume] ⊳ Output
   - Vox AC30C2
   - Vox UL730
     - Requires matching poweramp circuit for intended behavior and sound.
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
   - Lab Series L5
     - Operational transconductance amplifiers that are found in the Compression/Distortion/Master circuit of the amp are not supported in LiveSPICE.

## Special Thanks
 - [Emil Rohbe]( https://www.youtube.com/@Rohbemusic ) for showcasing LiveSPICE a few years back.
 - [Ed S]( https://www.youtube.com/@eds4754/ ) for some of his demos of relatively obscure amps as inspiration.
 - [Misery Party]( https://www.youtube.com/@miseryparty3726 ) / julio ([@walkingcontrad1ction]( https://www.instagram.com/walkingcontrad1ction/ ) on Instagram) for his accurate schematic of the Martin Golub/Dookie mod.

## Sound Demos
 - [1 hr. and 14 min. high gain shootout]( https://www.youtube.com/watch?v=8n2cJ84vBjc ) by [@cmd_f5]( https://www.youtube.com/@cmd_f5 )
 - [Fender Metalhead MH-500]( https://youtu.be/JuXZqc2LVPo ) by me.
 - [Martin Golub's "Green Day Dookie" Marshall mod]( https://youtu.be/Woa6odWk67s ) by me.
 - [Peavey Decade]( https://youtu.be/CR4IU-_BRPQ ) by me.
 - [Tube Works MosValve RT-2100]( https://youtu.be/AjsVQ49L4hQ ) by me.
