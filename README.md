# AssistantFuctions
This repo mainly includes the self-defined function in r to make the research go smoothly.

## Mandatory Rules
All mandatory rules of this repo are included in the [MandatoryRules.md](MandatoryRules.md)

## Function
  
Name: [07_AF_OutputSplmImpactFunction_V1.R](https://github.com/MichaelChaoLi-cpu/COVID-19_and_Land_Cover_NDVI/blob/master/04_Code/07_AF_OutputSplmImpactFunction_V1.R)  
Intro: This function is to output spml model impacts in the DP05 repo <https://github.com/MichaelChaoLi-cpu/COVID-19_and_Land_Cover_NDVI>.
Keyword: "spml", "impacts", "spatial panel model"

## Necessary Tips of Python
  
### Install Package
   
When we install package in Anaconda Prompt, we meet "Solving environment: failed with initial frozen solve. Retrying with flexible solve". That my be our **conda** version is too old we need to update it.  
  
First we use codes in Anaconda Prompt (Win) or Terminal (MacOS, Linux):  
```
conda update
```
   
There will be some hints. For example in the windows, it require us to type:  
```
conda update --prefix D:\Anaconda anaconda
```
  
Then wait. The updation should go step by step. It might take a long time, if your **conda** is very old.  