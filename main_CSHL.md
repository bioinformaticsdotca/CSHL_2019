---
layout: workshop_main_7day
permalink: /CSHL_2019
title: HT-Bio
header1: Workshop Pages for Students
header2: High-throughput Biology - From Sequence to Networks 2019
image: /site_images/CBW-CSHL-graphic-square.png
keywords: Visualize genomic data, pathway analysis, integrate clinical data
description: Course covers the key bioinformatics concepts and tools required to analyze  genomic data sets and access and work with data sets in the cloud. 
instructors: Sara Goodwin, Jared Simpson, Mathieu Bourgey, Zhibin Lu, Heather Gibling, Malachi Griffith, Obi Griffith, Peter Ronning, Kelsy Cotto, Juri Reimand, Robin Haw, Veronique Voisin, Quaid Morris, Michael Hoffman
length: 7 days
---

# Welcome <a id="welcome"></a>

Welcome to High-throughput Biology - From Sequence to Networks 2019.  

The course schedule can be found [here](https://bioinformaticsdotca.github.io/CSHL_2019_schedule)  

Pre-readings, pre-work, and laptop setup instructions can be found [here](https://bioinformaticsdotca.github.io/CSHL_2019_laptop_setup).

If you have questions or comments, visit the workshop [Q&A forum](https://classroom.google.com). You may need to join the group by clicking on the "+" symbol and entering the class code.

You can download the printed course manual [here]().  

Thank you for attending the workshop! Help us make this workshop better by filling out [our survey]().
***

# Class Photo

Coming soon! 

***

# Pre-Workshop Materials <a id="preworkshop"></a>

## Laptop Setup Instructions

Instructions to setup your laptop can be found [here](https://bioinformaticsdotca.github.io/CSHL_2019_laptop_setup).

## Pre-workshop Tutorials

1) **R Preparation tutorials**: You are expected to have completed the following tutorials in **R** beforehand. The tutorial should be very accessible even if you have never used **R** before.

* The [CBW R tutorial](http://bioinformatics-ca.github.io/CBW_R_Tutorial/)
* [Quick and Dirty Guide to **R**](http://ww2.coastal.edu/kingw/statistics/R-tutorials/text/quick&dirty_R.txt)  
* The [R Tutorial](http://www.cyclismo.org/tutorial/R/) up to and including 5. Basic Plots
* The [R command cheat sheet](../../resources/R_Short-refcard.pdf)

2) **UNIX Preparation tutorials**:  

* [UNIX Bootcamp](https://github.com/griffithlab/rnaseq_tutorial/wiki/Unix-Bootcamp)
* Tutorials #1-3 on [UNIX Tutorial for Beginners](http://www.ee.surrey.ac.uk/Teaching/Unix/)  
* [Unix Cheat sheet](http://www.rain.org/~mkummel/unix.html) 

3) [Sequencing Terminology](http://www.ncbi.nlm.nih.gov/projects/genome/glossary.shtml)

4)  **Cytoscape Preparation tutorials**: Complete the [introductory tutorial to Cytoscape](http://opentutorials.cgl.ucsf.edu/index.php/Portal:Cytoscape3)

* Introduction to Cytoscape3 - User Interface

* Introduction to Cytoscape3 - Welcome Screen

* Filtering and Editing in Cytoscape 3

###  Pre-workshop Readings  

  Before coming to the workshop, read these:
  
  * [Using cloud computing infrastructure with CloudBioLinux, CloudMan, and Galaxy](http://www.ncbi.nlm.nih.gov/pubmed/22700313)
  
  * [Integrative Genomics Viewer (IGV): high-performance genomics data visualization and exploration](http://www.ncbi.nlm.nih.gov/pubmed/22517427)
  
  * [Genome structural variation discovery and genotyping](http://www.ncbi.nlm.nih.gov/pubmed/21358748)
  
  * [A survey of sequence alignment algorithms for next-generation sequencing](http://www.ncbi.nlm.nih.gov/pubmed/20460430)
  
  * [Genotype and SNP calling from next-generation sequencing data](http://www.ncbi.nlm.nih.gov/pubmed/21587300)
  
  * [Differential gene and transcript expression analysis of RNA-seq experiments with TopHat and Cufflinks](http://www.ncbi.nlm.nih.gov/pubmed/22383036)
  
  * [ENCODE RNA-Seq Standards](https://genome.ucsc.edu/ENCODE/protocols/dataStandards/ENCODE_RNAseq_Standards_V1.0.pdf)
  
  * [Methods to study splicing from high-throughput RNA sequencing data](http://www.ncbi.nlm.nih.gov/pubmed/24549677)
  
  * [Differential analysis of gene regulation at transcript resolution with RNA-seq](http://www.ncbi.nlm.nih.gov/pubmed/23222703)
  
  * [A comprehensive assessment of RNA-seq accuracy, reproducibility and information content by the Sequencing Quality Control Consortium](http://www.ncbi.nlm.nih.gov/pubmed/25150838)
  
  * [Recurrent chimeric RNAs enriched in human prostate cancer identified by deep sequencing](http://www.ncbi.nlm.nih.gov/pubmed/21571633)
  
  * [iRegulon: From a Gene List to a Gene Regulatory Network Using Large Motif and Track Collections](http://www.ncbi.nlm.nih.gov/pubmed/25058159)
  
  * [The GeneMANIA prediction server: biological network integration for gene prioritization and predicting gene function](http://www.ncbi.nlm.nih.gov/pubmed/20576703)
  
  * [GeneMANIA Prediction Server 2013 Update](http://www.ncbi.nlm.nih.gov/pubmed/23794635)
  
  * [How to visually interpret biological data using networks](http://www.ncbi.nlm.nih.gov/pubmed/19816451)
  
  * [g:Profiler--a web-based toolset for functional profiling of gene lists from large-scale experiments](http://www.ncbi.nlm.nih.gov/pubmed/17478515)
  
  * [g:Profiler--a web server for functional interpretation of gene lists (2011 update)](http://www.ncbi.nlm.nih.gov/pubmed/21646343)
  
  * [Gene set enrichment analysis: a knowledge-based approach for interpreting genome-wide expression profiles](http://www.ncbi.nlm.nih.gov/pubmed/16199517)
  
  * [Expression data analysis with reactome](http://www.ncbi.nlm.nih.gov/pubmed/25754994)  

***

# Day 1 <a id="day1"></a>

## Welcome

*<font color="#827e9c">Ann Meyer</font>*

## Module 1: Introduction to High-throughput Sequencing

*<font color="#827e9c">Jared Simpson</font>* 

[Lecture]()
[Lab Practical]()  

## Module 2: Data Visualization

*<font color="#827e9c">Florence Cavalli</font>* 

[Lecture]()

[Lab Practical]()

## Module 3: Genome Alignment

*<font color="#827e9c">Mathieu Bourgey</font>* 

[Lecture]()

[Lab Practical: Connecting to the Cloud]()

[Lecture]()  

* We have set up 30 instances on the Amazon cloud - one for each student. In order to log in to your instance, you will need a security certificate. If you plan on using Linux or Mac OS X, please download [this certificate](http://cbwmain.dyndns.info/private/CBWNY.pem). Otherwise if you plan on using Windows (with Putty and Winscp), please download [this certificate](http://cbwmain.dyndns.info/private/CBWNY.ppk).

[Lab Practical]()  
[Lab Practical on GitHub]()

***

# Day 2 <a id="day2"></a>

## Module 4: Small-Variant Calling and Annotation

*<font color="#827e9c">Mathieu Bourgey</font>* 

[Lecture]()

[Lab Practical]()  
[Lab Practical on GitHub]()

## Module 5: Structural Variant Calling

*<font color="#827e9c">Mathieu Bourgey</font>* 

[Lecture]()

[Lab Practical]()  
[Lab Practical on GitHub]()  

## Module 6: De Novo Assembly

*<font color="#827e9c">Jared Simpson</font>* 

[Lecture]()

[Lab Practical]()

[Supplemental]()

## Integrated Assignment

[Integrated Assignment]()

***

# Day 3 <a id="day3"></a>

**Day 3 and Day 4 refer to content in the [RNA-Seq wiki](https://github.com/griffithlab/rnaseq_tutorial/wiki).**

## Module 7: Introduction to RNA Sequencing Analysis

*<font color="#827e9c">Malachi Griffith</font>* 

[Lecture]()

### Lab Practical

[Lab practical]()

  [Installation](https://github.com/griffithlab/rnaseq_tutorial/wiki/Installation)
  
  [Reference Genomes](https://github.com/griffithlab/rnaseq_tutorial/wiki/Reference-Genome)
  
  [Annotations](https://github.com/griffithlab/rnaseq_tutorial/wiki/Annotation)
  
  [Indexing](https://github.com/griffithlab/rnaseq_tutorial/wiki/Indexing)
  
  [Data](https://github.com/griffithlab/rnaseq_tutorial/wiki/RNAseq-Data)
  
  [Data QC](https://github.com/griffithlab/rnaseq_tutorial/wiki/PreAlignment-QC)


## Module 8: RNA-seq Alignment and Visualization

*<font color="#827e9c">Fouad Yousif</font>* 

[Lecture]()

### Lab Practical

[Lab Practical]()

  [Adapter Trim](https://github.com/griffithlab/rnaseq_tutorial/wiki/Adapter-Trim)
  
  [Alignment](https://github.com/griffithlab/rnaseq_tutorial/wiki/Alignment)
  
  [IGV](https://github.com/griffithlab/rnaseq_tutorial/wiki/IGV-Tutorial)

  [Alignment Visualization](https://github.com/griffithlab/rnaseq_tutorial/wiki/PostAlignment-Visualization)
  
  [Alignment QC](https://github.com/griffithlab/rnaseq_tutorial/wiki/PostAlignment-QC)

## Integrated Assignment

*<font color="827e9c">Fouad Yousif</font>*

Paper: [Recurrent chimeric RNAs enriched in human prostate cancer identified by deep sequencing](http://www.ncbi.nlm.nih.gov/pubmed/21571633)

[Assignment Questions](https://github.com/griffithlab/rnaseq_tutorial/wiki/Integrated-Assignment)

[Assignment Answers](https://github.com/griffithlab/rnaseq_tutorial/wiki/Integrated-Assignment-Answers)  


***

# Day 4 <a id="day4"></a>

## Module 9: Expression and Differential Expression

*<font color="#827e9c">Obi Griffith</font>* 

[Lecture]()

### Lab Practical

[Lab Practical]()

 [Expression](https://github.com/griffithlab/rnaseq_tutorial/wiki/Expression)
 
 [Differential Expression](https://github.com/griffithlab/rnaseq_tutorial/wiki/Differential-Expression)
 
 [DE Visualization](https://github.com/griffithlab/rnaseq_tutorial/wiki/DE-Visualization)

## Module 10: Reference Free Alignment

*<font color="#827e9c">Malachi Griffith</font>* 

[Kallisto](https://github.com/griffithlab/rnaseq_tutorial/wiki/Kallisto)  

## Module 11: Isoform Discovery and Alternative Expression

*<font color="#827e9c">Malachi Griffith</font>* 

[Lecture]()

### Lab Practical

[Lab Practical]()

  [Ref Guided](https://github.com/griffithlab/rnaseq_tutorial/wiki/Reference-Guided-Transcript-Assembly)
  
  [De novo](https://github.com/griffithlab/rnaseq_tutorial/wiki/de-novo-Transcript-Assembly)
  
  [Merging](https://github.com/griffithlab/rnaseq_tutorial/wiki/Transcript-Assembly-Merge)
  
  [Differential Splicing](https://github.com/griffithlab/rnaseq_tutorial/wiki/Differential-Splicing)
  
  [Splicing Visualization](https://github.com/griffithlab/rnaseq_tutorial/wiki/Transcript-Assembly-Visualization)

## Integrated Assignment

[Assignment Questions](https://github.com/griffithlab/rnaseq_tutorial/wiki/Integrated-Assignment)  

[Assignment Answers](https://github.com/griffithlab/rnaseq_tutorial/wiki/Integrated-Assignment-Answers)  

## Keeping Up-to-date with RNA-Seq Analysis Developments

For additional resources, tutorials, future directions, and more please refer to the [RNA-seq wiki](http://www.rnaseq.wiki/)

***

# Day 5 <a id="day5"></a>

## Module 12: Introduction to Pathway and Network Analysis

*<font color="#827e9c">Jüri Reimand</font>* 

[Lecture]()

## Module 13: Finding Over-Represented Pathways

*<font color="#827e9c">Jüri Reimand</font>* 

[Lecture]()

### Lab practical: Enrichment-Based Analysis - Performing ORA
  *<font color="#827e9c">Jüri Reimand and Veronique Voisin</font>*

[Introduction]()

gProfiler

[Exercise 1]()  
  
[Precomputed results for exercise 1]()   

GSEA
[Exercise 2]()  

[Precomputed results for Exercise 2]()  


## Module 14: Network Visualization and Analysis with Cytoscape

*<font color="#827e9c">Veronique Voisin</font>* 

[Lecture Part 1]()  

[Lecture Part 2]()  

### Lab practical: Cytoscape Demo, Enrichment Map
  *<font color="#827e9c">Veronique Voisin</font>*


[Exercise 1]()  
  
[Exercise 2]()  

***

# Day 6 <a id="day6"></a>

## Module 15: More Depth on Network and Pathway Analysis

*<font color="#827e9c">Robin Haw</font>* 

[Lecture]()

### Lab practical: *De Novo* Subnetwork Clustering Analysis in Reactome

[Lecture]()  

[Lab Practical]() 

[Lab answers]()  

## Module 16: Gene Function Prediction

*<font color="#827e9c">Quaid Morris</font>* 

[Lecture]()   

[Lab Practical]()  

## Integrated Assignment
[Integrated Assignment]()

[Integrated Assignment Answers]()

***

# Day 7 <a id="day7"></a>

## Module 17: Regulatory Network Analysis

*<font color="#827e9c">Michael Hoffman</font>* 

[Lecture]()

#### Lab practical: iRegulon

*<font color="#827e9c">Veronique Voisin</font>*

[Lab lecture]() 

[Lab practical]()  

[Precomputed results cys file]() and [Precomputed results irf file]()  

To use the precomputed results:  

1) launch Cytoscape 

2) open the "prostate_cancer_genemania_network.cys" file 

3) go to App > iRegulon > 'Load results from the iregulon_results.irf file'  
  
[Download a zip file of the git repo here]()  


