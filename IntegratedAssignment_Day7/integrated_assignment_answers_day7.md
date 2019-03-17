---
layout: tutorial_page
permalink: /CSHL_2019_IA_Answers_Day7
title: HT-Bio
header1: Workshop Pages for Students
header2: High-throughput Biology - From Sequence to Networks 2019 - Integrated Assignment Day 7
image: /site_images/CBW-CSHL-graphic-square.png
home: https://bioinformaticsdotca.github.io/CSHL_2019
description: HT-Bio Integrated Assignment Answers Day 7
author: Veronique Voisin
modified: June 27th, 2018
---

**This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/deed.en_US). This means that you are able to copy, share and modify the work, as long as the result is distributed under the same license.**

# Pathway and Network Analysis Integrated Assignment: Answers to questions and Screenshots

By Veronique Voisin


The results are stored in this [folder](https://github.com/bioinformaticsdotca/HT-Biology_2017/tree/master/Pathways/integrated_assignment_1/results).

## g:Profiler

**Question**: What is the most significant GO:term? What is the p-value for this GO:term 

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/IntegratedAssignment_Day7/img/gprofilerresultGO.png?raw=true" alt="gprofilerresultGO.png" width="750" />

**Answer**: extracellular matrix organization


**Question**: Is this p-value already corrected for multiple testing? What type of correction is used for your current analysis? 

**Answer**: yes, it is already corrected for multiple hypothesis testing. I set the Significance threshold box to  "Benjaminin-Hochberg FDR". 


Re-run the analysis with User p-value threshold set to 0.0001. 

**Question**: What has been changed?

**Answer:** Only the gene-set with adjusted pvalue equal or less than 0.0001 are displayed. The list is reduced compared to the results obtained with the default settings. 

Ordered query: 

**Question**: Do you seen any changes in the output in comparison to the analysis of the unordered gene list (PART 2) 

**Answer** Although some terms are similar, their pvalues changed as well as the number of term genes used to calculate the pvalue.


**Question** What can you conclude about these networks? 

**Answer** The pathways are relevant to the biological model under study. The changes are related to the transformation of the epithelial cells into mesenchymal ones. 
  

## REACTOME FI

Pathway enrichment on the whole network. 

**Question** What is the pathway with the lowest (best) FDR? 

**Answer** The pathway with the lowest FDR is Endometrial cancer (K) with an FDR equal to 5.78w-16. 

<img 
src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/IntegratedAssignment_Day7/img/ReacFI1.png?raw=true" alt="gprofilerresultGO.png" width="750" />


Cluster the network and perform pathway enrichment on the network.

**Question** How many clusters did the analysis retrieve?  

**Answer** The analysis retrieved 10 clusters named module 0 to module 9. 

<img 
src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/IntegratedAssignment_Day7/img/ReacFI3.png?raw=true" alt="gprofilerresultGO.png" width="750" />

**Question** What is the FDR value of the most significant pathway of module 0?

**Answer** RAF/MAP kinase cascade (first row)

<img 
src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/IntegratedAssignment_Day7/img/ReacFI4.png?raw=true" alt="gprofilerresultGO.png" width="750" />


## GeneMANIA

**Question** What is the number of nodes in the CTNBB1 network. 

**Answer** There are 22 nodes.

<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/INA9.png?raw=true" alt="INA9" width="750" />



