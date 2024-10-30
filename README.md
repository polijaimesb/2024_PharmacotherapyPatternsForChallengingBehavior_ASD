
### PharmacotherapyPatternsForChallengingBehavior_ASD
This repository contains different markdown scripts for cleaning and processing the data and identifying the patterns of medication to treat co-occurring conditions in children with Autism Spectrum Disorder (ASD) who exhibit challenging behaviors. 

### Prerequisites 
The following libraries must be installed. 

```
library(dplyr)
library(tidyr)
library(stringr)
library(stringi) 
library(RColorBrewer)
library(data.table)
library(networkD3)
library(htmlwidgets)
```
### Authorization 
Data used in this project is not available for public access. 
### How to use it
The first markdown script (1.ASDCohortSelection) contains the code for all the cleaning, processing, and extraction of the study cohort necessary for the project. 

The second markdown script (2.SankeyDiagram) comprises the code to identify the patterns of use of each medication over time and the visualization through a Sankey Diagram. 

### Analysis
To observe individual-level shifts in medications, we identified new individuals who received only one medication per year from the SSRIs or the Atypical Antipsychotics, considering refills. Then, we verified if the selected individuals for each year have also one medication prescribed the next year. We extracted the initial and the subsequent prescribed medication year by year and counted the patients with the same pattern. We aggregate by drug class, changing the name of the medication by their corresponding classification. In addition, we added a classification called “Other”, which represents the medications that are not part of the SSRIs or Atypical Antipsychotics. The patients included were followed through the years and the medications shifted were extracted. A new patient can be part of the subsequent year analysis if the patient did not receive medication from SSRIs or Atypical Antipsychotics the previous year. 

For 2019, we extracted the new patients with just one medication prescribed between SSRIs, aripiprazole, or risperidone for each of the months. Then, we verified if those patients had one medication prescribed the next month and took out the name of it. Individuals who passed the two criteria were followed through the next months. A new patient can be part of the subsequent month's analysis if the patient did not receive medication from SSRIs or Atypical Antipsychotics the previous month. We constructed a Sankey Diagram using the networkD3 library from R to examine the patterns found. 

### Publication 
This code supports the analysis intended to be published in a research letter in the next months.  



