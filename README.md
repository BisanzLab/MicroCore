# High-throughput Culture Screening


## Purpose

This protocol describes a screening strategy to screen microbes for growth/metabolic traits. A 96 well plate of organisms can be assayed in quadruplicate (4 vehicle and 4 test compound well per strain) using dual 384 well plates. To avoid human errors and cross contamination. Plates are stamped using pin replicators and the 384 well plates set up using robotics. All media and supplies need to be deoxygenated by placing in the anaerobic chamber of a minimum of 24 h before experimentation. 

## Materials
- [ ] Deep well plate with arrayed strain collection (VWR: 75870-796)
- [ ] 96 well pin replicator (Scinomix Inc: NC1567338)
- [ ] 96 well culture plate (Falcon: 351177)
- [ ] Appropriate growth media (Often BHI CHV or BHI CHVR: see media recipes)
- [ ] Sterile test compound disolved at least 100x concentration in water (prefered), DMSO, DMF, or methanol
- [ ] Sterile Breathable Plate Seals (Diversified Biotech: 490006-676)
- [ ] Sterile Aluminum Foil Plate Seals
- [ ] 2 x 384 well plates (Corning: 3680)
- [ ] Anaerobic Chamber with 20% CO2, 5% H2, 75% N2
- [ ] OT2 with 20 µL multichannel head on right mount with 1 boxes of tips
- [ ] 8-channel 200µL pipette with appropriate tips
- [ ] CoolBox (Corning: 432022)
- [ ] Plate vortex (IKA: 0003319000)
- [ ] 2 Multiskan SkyHigh Plate Readers

# Protocol

*Note: Before starting work for the day spray all surfaces with 70% ethanol or isopropanol (in anaerobic chamber). Outside of anaerobic chamber, always work by flame or inside biological safety cabinet. Remember all surfaces in the anaerobic chamber are potentially contaminated and extra precaution should be taken during handling.*

## Preparation of Inoculum

### Day 1
- [ ] Transfer 150 µL of sterile media to each well of a 96 well plate (Lower volume lessens chance of cross-contamination) 
- [ ] Cover with breathable plate seal
- [ ] Transfer to anaerobic chamber

### Day 2
- [ ] Remove Deep well strain block from -80˚C freezer and place on freezer block
- [ ] ?Centrifuge strain block at 1000 G for 5 minutes? **(This should be a safe speed!)**
- [ ] Transfer strain block into anaerobic chamber
- [ ] Carefully remove seal avoiding splashing of any condensation that may still be on lid
- [ ] Carefully remove pin replicator from bag being sure not to touch any surface
- [ ] Carefully place pin replicator into deep well plate and dig into glycerol stocks to ensure transfer of material onto pins
- [ ] Quickly remove pin replicator and transfer into 96 well plate which contains 150 µL of sterile media (inoculation plate)
- [ ] Discard pin replicator in biohazard waste
- [ ] Cover strain glycerol block with aluminum seal (To ensure a good seal make sure that he rim of plate is dry)
- [ ] Cover inoculation plate with breathable seal
- [ ] Place inoculation plate in 37˚C incubator for 72h **(Plate 1 can be ready after 1 day, we should see what the optimal time is!!)**
- [ ] Return glycerol strain block to -80˚C freezer


### Day 4
- [ ] Into the odd rows of both 384 well plates, transfer 80 µL of appropriate growth media with 1% vehicle (what ever drug is disolved in)
- [ ] Into the even rows of both 384 well plates, transfer 80 µL of the appropriate growth media with 1% test compound (both drug and vehicle need to be sterile)
- [ ] Cover with breathable seal and transfer into anaerobic chamber

## Setting up assay

### Day 5
- [ ] Remove the inoculation plate from the incubator and place onto plate vortex
- [ ] Vortex for 120 seconds at around 750 rpm (do not exceed this number as it may lead to spillage and/or cross contamination)
- [ ] Transfer 96 well plate to plate reader and measure OD600
- [ ] Save these results to transfer to server
- [ ] Carefully examine corner wells (sterile controls) and internal sterile wells. If signs of growth: STOP! Also, if majority of strains have not grown: STOP!
- [ ] Transfer the inoculation plate into deck position 3 of the OT2
- [ ] Transfer the 384 well plates with media/drug to deck positions 1 and 2
- [ ] Put 1 box sterile 20 µL filter tips in deck position 6
- [ ] Carefully remove all seals avoiding cross contamination
- [ ] Close OT2 door
- [ ] Load OT2 software and makeGCs.py script
- [ ] Calibrate all deck positions (especially important for 384 well plates, for 384 well plates y off-set of 0.50 is a good starting point)
- [ ] Run script
- [ ] After completion (about 7 minutes), transfer breathable seals onto both 384 well plates
- [ ] Carefully wrap exterior edges of plates with tape and transfer to plate readers
- [ ] Set up both plate readers to run at 37˚C for 48h with OD600 reads every 15 minutes
- [ ] Discard inoculation plate (unless you want to save it to verify strains after the fact), and tip box (note: tips in the box are contaminated and must be marked/discard to prevent their reuse

## Storing/Analyzing Data

### Day 7
- [ ] When the run is complete the plates will be ejected
- [ ] Discard plates, but note if there has been any issues with evaporation on edges/ corners.
- [ ] Save the runs and export data to excel files.
- [ ] Create a new directory on the lab server matching the directory structure of /data/MicroCore/runs/YOURPROJECT/YYYYMONDD_Plate[0-9]_COMPOUND/
- [ ] Transfer your pre-run ODs and the growth curve data to these directories
- [ ] Download a copy of RunTemplate.Rmd and rename to your project. Store in your new directory
- [ ] Load Rmd file in Rstudio server (bisanzlab.science.psu.edu:443) and modify lines 33-37 to match the information for your plate. Hit Knit to compile the report/process data.

