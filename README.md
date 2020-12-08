# Sld-R-Data

Dan Villarreal (University of Pittsburgh)

This repository contains data for the under-review paper "Gender separation and the Speech Community: Rhoticity in early 20th century Southland New Zealand English." The data consists of 30,777 non-prevocalic /r/ tokens from Southland New Zealand English. Almost all tokens are coded for /r/, most by the classifier. 10,337 tokens were analyzed in at least one model due to various exclusions (e.g., only content words); information on which tokens were analyzed in which model is encoded in the columns `In_Mod_AllF`, `In_Mod_AllM`,  `In_Mod_NurseF`, `In_Mod_NurseM` (with `In_AnyMod` encoding whether tokens were included in at least one model). To ensure anonymity, both the Speaker and Word columns have been replaced with anonymous codes.

The data is in two formats: .Rds (for use in the R statistical computing environment) and .csv (with blanks for what are called `NA`s in R parlance).

If you have any questions, please do not hesitate to email me (d.vill atsign pitt.edu) or create a GitHub issue.
