# High-throughput Culture Screening


## Purpose

This protocol describes a screening strategy to screen microbes for growth/metabolic traits. A 96-well plate of organisms can be assayed in quadruplicate (4 vehicle and 4 test compound well per strain) using dual 384-well plates. To avoid human errors and cross contamination. Plates are stamped using multichannel and the 384-well plates set up using robotics. All media and supplies need to be deoxygenated by placing in the anaerobic chamber of a minimum of 48 h before experimentation.

## Materials
- [ ] Deep well plate with arrayed strain collection (CATALOG NUMBER：VWR 75870-796)
- [ ] 96 well pin replicator (CATALOG NUMBER: Fisher Sci NC1567338)
- [ ] 96 well culture plate (CATALOG NUMBER: Fisher Sci 877254)
- [ ] Appropriate growth media (Often BHI CHV or BHI CHVR: see media recipes)
- [ ] Sterile test compound disolved at least 100x concentration in water (prefered), DMSO, DMF, or methanol
- [ ] Sterile Breathable Plate Seals (CATALOG NUMBER: VWR 490006-676)
- [ ] Sterile Aluminum Foil Plate Seals
- [ ] 2 x 384 well plates (CATALOG NUMBER: Sigma CLS3701-100EA)
- [ ] Anaerobic Chamber with 20% CO2, 5% H2, 75% N2
- [ ] OT2 with 20 µL multichannel head on right mount with 1 boxes of tips
- [ ] 8-channel 200µL pipette with appropriate tips
- [ ] ICE BLOCK THINGY (CATALOG NUMBER: Neta Sci 432051)
- [ ] Plate vortex (IKA CATALOG NUMBER: Neta Sci IKA-0003319000)
- [ ] 2 Multiskan SkyHigh Plate Readers
- [ ] 3 x 50 mL Conical Tubes (We use: VWR, Cat# 89039-658)
- [ ] Resorvoirs (We use: VWR, Cat#	53504-035)

# Protocol

*Note: Before starting work for the day spray all surfaces with 70% ethanol or isopropanol (in anaerobic chamber). Outside of anaerobic chamber, always work by flame or inside biological safety cabinet. Remember all surfaces in the anaerobic chamber are potentially contaminated and extra precaution should be taken during handling.*

## Preparation of Materials

### Day -2 (At least 48 hours before starting source plate)
- [ ] Aliquot 2 x 35 mL tube, and 1 20 mL tube of media to anaerobic chamber
- [ ] Gather 1 96-well plate, 2 x 384-well plates, media resorvoirs, and syringe and syringe-filters if needed. 
- [ ] Transfer to anaerobic chamber

### Day 2
- [ ] Remove Deep well strain block from -80˚C freezer and place on freezer block
- [ ] Transfer strain block into anaerobic chamber
- [ ] Working one column at a time, carefully remove lids from strain array plate with 8-channel decapper and discard (Frozen lids may not unseal easily and spread droplets, allow to defrost longer if needed)
- [ ] Use p200 multichannel pipettor to press 200 µL tip to exposed column of tubes
- [ ] Quickly remove tips and transfer into corresponding row of 96 well plate which contains 150 µL of sterile media (source plate)
- [ ] Discard tips
- [ ] Use 8-channel decapper to collect a column of fresh lids, cap exposed tubes
- [ ] Repeat transfer steps to transfer to all columns
- [ ] Check lids on strain array plate to ensure tight fit
- [ ] Place inoculation plate in 37˚C incubator for 48 h
- [ ] Return strain array plate to -80˚C freezer

## Setting up assay

### Day 5
- [ ] Remove the inoculation plate from the incubator and place onto plate vortex
- [ ] Vortex for 60 seconds at 1000 rpm (do not exceed this number as it may lead to spillage and/or cross contamination)
- [ ] Transfer 96 well plate to plate reader and measure OD600
- [ ] Save these results to transfer to server
- [ ] Carefully examine corner wells (sterile controls) and internal sterile wells. If signs of growth: STOP! Also, if majority of strains have not grown: STOP!
- [ ] Add vehicle and drug to corresponding conical containing 35 mL of media
- [ ] Into the odd rows of both 384-well plates, transfer 80 µL of appropriate growth media with 1% vehicle (whatever drug is dissolved in)
- [ ] Into the even rows of both 384-well plates, transfer 80 µL of the appropriate growth media with 1% test compound
- [ ] If running multiple plates, create new source plate (150 µL of desired media to each well of a new 96-well plate)
- [ ] Remove the source plate from the incubator and place onto deck position 3 of the OT2
- [ ] Transfer the 384-well plates with media/drug to deck positions 1 and 2
- [ ] Put 1 box sterile 20 µL filter tips in deck position 6
- [ ] If using, place new source plate onto deck position 4
- [ ] Carefully remove all lids avoiding cross contamination (Typically place on a freshly cleaned part of work surface)
- [ ] Close OT2 door
- [ ] Load OT2 software and makeGCs.py script
- [ ] Set parameters to indicate if you are regenerating source plate, the default for mixing is usually sufficient
- [ ] Calibrate all deck positions (especially important for 384 well plates, align first tip to the center of A1 of each plate **NOT** to space between wells)
- [ ] Run script
- [ ] After completion (about 15 minutes), transfer breathable seals onto both 384 well plates
- [ ] Carefully wrap exterior edges of plates with tape and transfer to plate readers
- [ ] Set up both plate readers to run at 37˚C for 48h with OD600 reads every 15 minutes (Naming Convention: YYYYMMDD_plate0X_drug_left|right)
- [ ] Discard source plate (unless you want to save it to verify strains after the fact), and tip box (note: tips in the box are contaminated and must be marked/discard to prevent their reuse

## Storing/Analyzing Data

### Day 5
- [ ] When the run is complete the plates will sometimes eject and sometime stay in
- [ ] Discard plates, but note if there has been any issues with evaporation on edges/ corners
- [ ] Carefully examine corner wells (sterile controls) and internal sterile wells. If signs of growth: STOP! Also, if majority of strains have not grown: STOP! (Some growth in sterile wells is okay, but a good run will have 
- [ ] If repeating experiment repeat steps on Day 3 using regenerated source plate
- [ ] Save the runs and export data to excel files
- [ ] If done with experiments turn off plate readers and OT-2 at the power strip
- [ ] Transfer your pre-run ODs and the growth curve data to the lab server
- [ ] Download a copy of RunTemplate.Rmd and rename to your project. Store in your new directory
- [ ] Load Rmd file in Rstudio server (bisanzlab.science.psu.edu:443) and modify lines XX-XX to match the information for your plate. Hit Knit to compile the report/process data

## Notes:

- [ ] There are significant time savings in running multiple plates in a row, so consider doing that if possible.
- [ ] Removing the source plate from the incubator too early can result in excessive amounts of condensation on the lid. This is a possible source of contamination, so only remove from incubator when ready to load onto OT-2
- [ ] It can be helpful to manually check for growth and no growth on the source plates as the OD600 values can be very low for weak growers
- [ ] The presence of oxygen especially if the oxygen concentration is different between vehicle and drug can severely impact results. So it is critical to put the vehicle and the drug into the anaerobic chamber at the same time. 

