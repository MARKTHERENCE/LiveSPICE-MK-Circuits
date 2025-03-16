# LiveSPICE-MK-Circuits
![livespice-mk-circuits](https://github.com/user-attachments/assets/b2af7ccc-bb4a-4518-81c5-2767758b60af)

Schematic files drawn for use with [LiveSPICE]( https://github.com/dsharlet/LiveSPICE ), developed by Dillon ([@dsharlet]( https://github.com/dsharlet ).)

## IMPORTANT!
 - The amp models require more than one instance of LiveSPICE for the desired results, separated into preamp and poweramp sections.
   - For REAPER users, LiveSPICE will run in parallel, so all instances of LiveSPICE will open the same circuit. To be able to use more than one circuit across multiple instances, do the following workaround:
     - `Add FX ⊳ Right-click on "VST3: LiveSPICE (mono) ⊳ Run as... ⊳ Dedicated process` 

 - Some of the circuits may be "preamp only" sections available due to the following reasons:
   - The referenced schematic does not include the diagram for the power amp section. 
   - The tube stages use the phase inverter of the power amp to cascade more gain.
   - The power amp section is solid state-based.
 - There may be some circuits that are broken down into several parts. It's a compromise I had to resort to for CPU usage. For convenience, I will note which circuits this workaround applies to.

If any of these are the case, please refer to the schematic file for further details and instructions.

# List of Circuits
Circuits of various guitar/bass amps and FX pedals. This list may expand over time.

 - ## Effector Pedals
   - Andromeda Natural Overdrive
   - Nobels ODS-1 Overdrive

 - ## Guitar Amplifiers
   - Ceriatone Marshall Plexi Super Lead "Dookie Mod"
   - Crate Stealth GT50-H
   - Fender Metalhead MH-500
   - "Fortin Cali Mod" (assumed to be incorrect)
   - Lab Series L5 (Preamp section only)
     - Signal chain:
       - Channel I / Channel II [Input ⊳ Tone Buffer and Multifilter] ⊳ Distortion & Master
   - Legend Rock 'n Roll 50
     - Signal chain:
       - 1st & 2nd Tube Stages ⊳ Phase Inverter
   - Marshall "Jose Master Volume" mod (by Fusedbrain)
     - Derived from 1987x
   - Marshall "Martin Golub/Dookie Mod" (by Misery Party / julio)
     - Derived from JCM800 2203 / JMP Superlead 100w
   - Marshall Silver Jubilee 2550/2555
   - Park 1210 Rock Head
   - Pignose 7-100 preamp section
   - Selmer Treble 'n Bass 50w MKII
   - Tube Works MosValve RT-2100
     - Signal chain:
       - Clean Channel / Drive Channel [1st Tube Stage ⊳ 2nd Tube Stage, EQ, & Master Volume] ⊳ Output
   - Vox AC30C2

## Special Thanks
 - [Emil Rohbe]( https://www.youtube.com/@Rohbemusic ) for showcasing LiveSPICE a few years back.
 - [Ed S]( https://www.youtube.com/@eds4754/ ) for some of his demos of relatively obscure amps as inspiration.
 - [Misery Party]( https://www.youtube.com/@miseryparty3726 ) / julio ([@walkingcontrad1ction]( https://www.instagram.com/walkingcontrad1ction/ ) on Instagram) for his accurate schematic of the Martin Golub/Dookie mod.
