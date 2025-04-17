
# **Replication Package for 2025 School Psychology Review Publication**
<!-- TODO: UPDATE WITH NEW STRUCTURE NOW ITS OWN REPO, NOT PUBLICATIONS SUBFOLDER--->

**Date of Release:** 3/31/2025  
**Title:** Reporting of Student Demographics in School-Based Depression Prevention Trials: The Need for a Core Baseline Set in School Psychology
**OSF Component:** <https://osf.io/> <br> <!-- TODO: INSERT LINK AFTER PUBLICATION -->
**Package Author:** Shaina Trevino 



## **🔹 Overview**
This folder contains the replication materials for the following publication:  

<!-- TODO: INSERT CITATION/DOI AFTER PUBLICATION -->
Grant, S., Dussan, H., Sebree, M., Trevino, S. D., Steinka-Fry, K., Chinn, L. K., Day, E., & Tanner-Smith, E. E. (2025). Reporting of Student Demographics in School-Based Depression Prevention Trials: The Need for a Core Baseline Set in School Psychology.

This replication package follows **[AEA Data and Code Availability Standards](https://datacodestandard.org/)** and includes:
- Datasets used to generate reported results.
- R code necessary to reproduce quantitative results reported.
- Computational environment details to ensure reproducibility.


## **🔹 Data and Code Availability Statement**
### **Data Sources**
The data used in this publication include review and study characteristics from our larger [living systematic review on school-based depression prevention](https://github.com/HEDCO-Institute/Depression_Prevention_Overview), as well as additional demographic details extracted in DistillerSR specifically for this publication.
- Datasets from the living review used for this publication reflect a fixed version of the data, captured during analysis. 
- Metadata (variable names and descriptions) are provided as the first tab of each data file.

The following datasets used for analyses are available in the `data` subfolder:

| Data File | Description | Data Structure |
|-----------|-------------|-----------| 
| `2025_SPR_review_characteristics.xlsx` | Extracted descriptive data for eligible reviews | One row per eligible review | 
| `2025_SPR_study_characteristics.xlsx` | Extracted descriptive data for eligible primary studies | One row per eligible primary study |
| `2025_SPR_SchoolPyschRev_Data.xlsx` | Extracted demographic information from primary studies | One row per reported demographic | 
<br>

### **Analysis Script**
The analysis script used to generate quantitative results for this publication is an `Rmarkdown` file in the `code` subfolder (`2025_SPR_analysis_script.Rmd`). 

### **Data Citation**
Please cite this version of the data as follows:

<!-- TODO: INSERT CITATION/DOI AFTER PUBLICATION -->
Trevino, S. D., Grant, S., Dussan, H., Sebree, M., Steinka-Fry, K., Chinn, L. K., Day, E., & Tanner-Smith, E. E. (2025). Data for "Reporting of Student Demographics in School-Based Depression Prevention Trials: The Need for a Core Baseline Set in School Psychology." OSF.

### **Handling of Missing Data**
- Missing values in the datasets are coded as `-999`, `Not Reported`, or `NA` and indicate those values were not reported in studies/reviews.


## **🔹 Instructions for Replication**

### **Data Preparation and Analysis**
To replicate our results: 

**If you have Rstudio and Git installed and connected to your GitHub account:**

1. Clone the [repository](https://github.com/HEDCO-Institute/Depression_Prevention_Demographics) to your local machine ([click for help](https://book.cds101.com/using-rstudio-server-to-clone-a-github-repo-as-a-new-project.html#step---2))
1. Open the `Depression_Prevention_Demographics.Rproj` R project in R Studio (this should automatically activate the `renv` environment)
1. Navigate to the `code` folder
1. Run the `2025_SPR_analysis_script.Rmd` script 

**If you need to install or connect R, Rstudio, Git, and/or GitHub:**

1. [Create a GitHub account](https://happygitwithr.com/github-acct.html#github-acct)
1. [Install R and RStudio](https://happygitwithr.com/install-r-rstudio.html)
1. [Install Git](https://happygitwithr.com/install-git.html)
1. [Link Git to your GitHub account](https://happygitwithr.com/hello-git.html)
1. [Sign into GitHub in Rstudio](https://happygitwithr.com/https-pat.html)

**To reproduce our results without using Git and GitHub, you may use the following steps:** 

1. Download the ZIP file from the [repository](https://github.com/HEDCO-Institute/Depression_Prevention_Demographics)
1. Extract all files to your local machine
1. Open the `Depression_Prevention_Demographics.Rproj` R project in R Studio (this will automatically set the working directory and activate the `renv` environment)
1. Navigate to the `code` folder
1. Run the `2025_SPR_analysis_script.Rmd` script 


## **🔹 Notes on Reproducibility**
- All file paths are relative; no hardcoded paths are used.
- Data cleaning and analyses are fully automated in the provided `.Rmd` analysis script.

### **Non-Reproducible Elements**
Some components cannot be reproduced using the analysis script:
- Qualitative findings, such as the specific categories or groups reported, are not generated by the analysis script. 
- Table 1, was manually created in Word and is not generated by the analysis script.

### **Known Discrepancies**
<!-- TODO: INSERT CITATION/DOI AFTER PUBLICATION -->
At this time, there are no known discrepancies between results from the analysis script and those reported in the publication/preprint.


## **🔹 Computational Requirements**
### **Software Environment**
- **R Version:** 4.2.2  
- **Operating System:** Windows 10 Enterprise (x86_64-w64-mingw32/x64)  

### **Reproducing the Environment**
Opening the `Depression_Prevention_Demographics` R project will automatically install the correct package versions and set up the environment using the `renv` package. To manually load the environment:

1. Install `renv` (if not already installed):
```r
if (!requireNamespace("renv", quietly = TRUE)) install.packages("renv")
```

2. Restore any missing packages:
```r
renv::restore()
```

3. If needed, load the environment:
```r
renv::load()
```

Once the environment is restored, run the script starting with loading the necessary packages:
```r
pacman::p_load(tidyverse, rio, here)
```


## **🔹 Folder Structure**
```
📁 Depression_Prevention_Demographics/
│── 📁 code/                   # Analysis scripts for reproducibility
│    └── 2025_SPR_analysis_script.Rmd
│
│── 📁 data/                   # Datasets used for this publication
│    ├── 2025_SPR_review_characteristics.xlsx
│    ├── 2025_SPR_SchoolPsychRev_Data.xlsx
│    ├── 2025_SPR_study_characteristics.xlsx
│
│── 📁 renv/                   # Renv environment for reproducibility
│── 📄 renv.lock               # Package versions and dependencies
│── 📄 .Rprofile               # Renv configuration file
│── 📄 README.md               # This README document
│── 📄 LICENSE                 # Liscense for this repo
```


## **🔹 Licensing**
The code and data in this replication package are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0); see the LICENSE file in the main root directory for full terms



## **🔹 Contact Information**
For questions about this replication package, contact:  
✉️ **Shaina Trevino** (strevino@uoregon.edu)  

