# Mandatory Rules

This file including several mandatory rules of naming, coding, and updating.  
  
## 1 Naming  
There is an additional type of scripts in daily analyses except ata washing (DW), analysis (AN), visualization (VI), which is to store some useful self-defined functions, assistant function (AF). They also take the ordered number in the project. To manage them, we build this repo, but these AF scripts still need to follow the naming rules of "GitHubManagementProcedure", which is temporally stored in DP05 repo <https://github.com/MichaelChaoLi-cpu/COVID-19_and_Land_Cover_NDVI/blob/master/GitHubManagementProcedure.md>.  
**After this repo publiclized, this file should be moved to this repo**  

All Rscripts should be ordered from 01. Version should add at the ending of the name, form v1. Working version is v0. The aim of the code should be including in the name with five words using camel methods. All the element should be connected by "_". Moreover, since these scripts are cross-repo, so they should contain the internal codes (such as DP05) in the intros.  
e.g.: 07_AF_OutputSplmImpactFunction_V1.R  

## Coding
We currently just make a content connect them to the README.md of this repo. Therefore the structure of **Function** section in the README.md should first mention the name of the function, and then give the intro.  
e.g.:  
Name: [07_AF_OutputSplmImpactFunction_V1.R](https://github.com/MichaelChaoLi-cpu/COVID-19_and_Land_Cover_NDVI/blob/master/04_Code/07_AF_OutputSplmImpactFunction_V1.R)  
Intro: This function is to output spml model impacts in the DP05 repo <https://github.com/MichaelChaoLi-cpu/COVID-19_and_Land_Cover_NDVI>.
Keyword: "spml", "impacts", "spatial panel model"
