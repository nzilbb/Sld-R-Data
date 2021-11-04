# Sld-R-Data

Dan Villarreal (University of Pittsburgh)

This repository contains data for the paper "Gender separation and the Speech Community: Rhoticity in early 20th century Southland New Zealand English," published in 2021 in the journal [_Language Variation and Change_](https://doi.org/10.1017/S0954394521000090). The data consists of 30,777 non-prevocalic /r/ tokens from Southland New Zealand English, with one row per token. Almost all tokens are coded for /r/, most by a [sociolinguistic auto-coding algorithm](https://www.journal-labphon.org/articles/10.5334/labphon.216/). 10,337 tokens were analyzed in at least one model due to various exclusions (e.g., only content words were analyzed). To ensure anonymity, both the Speaker and Word columns have been replaced with anonymous codes.

The data is in two formats: .Rds (for use in the R statistical computing environment) and .csv (with blanks for what are called `NA`s in R parlance).

If you have any questions, please do not hesitate to email me (d.vill atsign pitt.edu) or create a GitHub issue.

If you use this data in any published work, please cite it. Citing open data is a small thing you can do to ensure that researchers have the incentive to keep making data open.

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png

## Columns

* `MatchId`: Internal [LaBB-CAT](http://labbcat.sourceforge.net/) code for each token
* `In_Mod_AllF`, `In_Mod_AllM`, `In_Mod_NurseF`, `In_Mod_NurseM`: (Boolean) Was this token included in the respective model?
* `In_AnyMod`: (Boolean) Was this token included in any of the models?
* `TokenNum`: Token counter downloaded from LaBB-CAT
* `Speaker`: Anonymized speaker code
* `Gender`, `BirthYear`: Speaker attributes
* `Generation`: Binned generation groups for the purpose of analysis
* `GrewUpRegion`: Binned subregions within and/or beyond Southland
* `UrbanRural`: Invercargill vs. rural Southland
* `VersionDate`: Inherited from LaBB-CAT
* `Lemma`: Lemma
* `CelexFreqLemma`: Lemma frequency in CELEX
* `CorpusFreqLemma`: Lemma frequency in the Southland corpus
* `PerMilSldLemma`: Lemma frequency in the Southland corpus, normalized per million
* `PerMilBaselineLemma`: Lemma frequency in a corpus of General New Zealand English, normalized per million
* `SldnessLemma`: `PerMilSldLemma`/`PerMilBaselineLemma`
* `Word`: Anonymized word code
* `WordStart`, `WordEnd`: Word boundary timepoints within transcript
* `ContFuncWord`: Word category (content or function)
* `CelexFreqWord`: Word frequency in CELEX
* `CorpusFreqWord`: Word frequency in the Southland corpus
* `PerMilSldWord`: Word frequency in the Southland corpus, normalized per million
* `PerMilBaselineWord`: Word frequency in a corpus of General New Zealand English, normalized per million
* `SldnessWord`: `PerMilSldWord`/`PerMilBaselineWord`
* `Syllable`: Syllable in [DISC](https://groups.linguistics.northwestern.edu/speech_comm_group/documents/CELEX/Phonetic%20codes%20for%20CELEX.pdf) notation
* `SyllStart`, `SyllEnd`: Syllable boundary timepoints within transcript
* `Stress`: Syllable stress: ' for primary, " for secondary, 0 for unstressed
* `TokenStart`, `TokenEnd`: Token boundary timepoints within transcript (where token = vowel + possible /r/)
* `Vowel`: Preceding vowel in [Wells lexical set notation](https://en.wikipedia.org/wiki/Lexical_set#Wells_Standard_Lexical_Sets_for_English)
* `VowelCat`: `Vowel`, with an Other category for contexts that in nonrhotic accents are centering diphthongs or triphthongs (CURE, MOUTH-R, NEAR, PRICE-R, SQUARE)
* `FollSegRawNoPause`: The next segment after the token, ignoring pauses, in Wells notation for vowels and [two-letter ARPABET](https://en.wikipedia.org/wiki/ARPABET#Symbols) notation for consonants
* `FollSegRaw`: The next segment after the token, unless a pause of at least 100 ms came first
* `FollSeg`: `FollSegRaw`, binned for the purposes of analysis
* `SyllFinal`: (Boolean) Does `TokenEnd` equal `SyllEnd` (relevant for determining rhoticity status)?
* `WordFinal`: (Boolean) Does `TokenEnd` equal `WordEnd` (relevant for determining rhoticity status)?
* `FollPause`: (Boolean) Is the token followed by a pause of at least 100 ms?
* `FollPauseDur`: Duration of following pause
* `PrevRInWord`: (Boolean) Does the token follow another /r/ token in the same word?
* `HowCoded`: Whether the `Rpresent` code came from a human hand-coder or [auto-coding algorithm](https://www.journal-labphon.org/articles/10.5334/labphon.216/)
* `Rpresent`: Rhoticity code: Present (aka r-ful, rhotic) vs. Absent (aka r-less, nonrhotic)
* `ProbPresent`: Classifier probability: Probability that each token was Present, as estimated by the [auto-coding algorithm](https://www.journal-labphon.org/articles/10.5334/labphon.216/)

