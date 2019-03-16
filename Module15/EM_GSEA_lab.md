---
layout: tutorial_page
permalink: /CSHL_2019_Module15_lab_1
title: HT-Bio
header1: Workshop Pages for Students
header2: High-throughput Biology - From Sequence to Networks 2019 - Lab 15 - Part 1
image: /site_images/CBW-CSHL-graphic-square.png
home: https://bioinformaticsdotca.github.io/CSHL_2019
description: HT-Bio Module 15 Lab - Part 1
author: Veronique Voisin
modified: June 27th, 2018
---

**This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/deed.en_US). This means that you are able to copy, share and modify the work, as long as the result is distributed under the same license.**

# Network Visualization and Analysis with Cytoscape: create an enrichment map from GSEA results

By Veronique Voisin

## Goal of the exercise:

**Create an enrichment map and navigate through the network**

During this exercise, you will learn how to create an EnrichmentMap from gene-set enrichment results. The enrichment tool chosen for this exercise is GSEA but an enrichment map can be created from various gene-set tools using the generic format or the more specific g:Profiler, DAVID or BiNGO formats.

**Post analysis (add drug target gene-sets to the network)**

As second part of the exercise, you will learn how to expand the network by adding an extra layer of information.

**Autoannotate**

A last optional exercise guides you toward the creation of automatically generated cluster labels to the network.

## Data

The data used in this exercise is gene expression data obtained from high throughput RNA sequencing.
They correspond to Ovarian serous cystadenocarcinoma samples. We use precomputed results of the GSEA analysis [[GSEA part](https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/Module15/mod2_lab_GSEA.md)] to create an enrichment map with the aim to transform the tabular format in a network to better visualize the relationships between the significant gene-sets:


<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/workflow.png?raw=true" alt="workflow" width="750" />

## GSEA output and EnrichmentMap

The output results of GSEA are 2 tables:

*	One table (*pos*) contains all pathways with an enrichment score (significant or not) related to enrichment of the mesenchymal category (positive score).

*	One table (*neg*) contains all pathways with an enrichment score (significant or not) related to enrichment of the immunoreactive category (negative score).

*	These 2 tables are uploaded using the EnrichmentMap App which will create a network of mesenchymal and immunoreactive pathways that have a significant score (FDR <= 0.0001) for clearer visualization of the results.

### EnrichmentMap

*	A <font color="red">red circle (node)</font> is a pathway specific of the mesenchymal type.

*	A <font color="blue">blue circle (node)</font> is a pathway specific of the immunoreactive type.

*	<font color="green">Green edges</font> represent genes in common between 2 pathways (nodes).

*	A cluster of nodes represent overlapping and related pathways and may represent a common biological process.

*	Clicking on a node will display the genes included in each pathway.

## Start the exercise

To start the lab practical section, first download the files.

7 Files are needed to create the enrichment map for this exercise (please download these files on your computer):

1.	GMT (file containing all pathways and corresponding genes) - [Human_GOBP_AllPathways_no_GO_iea_December_24_2015_symbol.gmt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_GSEA_data/Human_GOBP_AllPathways_no_GO_iea_December_24_2015_symbol.gmt)

2.	Expression (file containing the RNAseq data for all samples and all genes) - [MesenchymalvsImmunoreactive_rnaseq_expression.txt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_GSEA_data/MesenchymalvsImmunoreactive_rnaseq_expression.txt)

3.	Enrichments 1 (GSEA results for the “pos” mesenchymal phenotype) - [gsea_report_for_na_pos_1453222854028.xls](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_GSEA_data/gsea_report_for_na_pos_1453222854028.xls)

4.	Enrichments 1 (GSEA results for the “neg” immunoreactive phenotype) - [gsea_report_for_na_neg_1453222854028.xls](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_GSEA_data/gsea_report_for_na_neg_1453222854028.xls)

5.	Rank file (file that has been used as input to GSEA) - [MesenchymalvsImmunoreactive_edger_ranks.rnk](https://raw.githubusercontent.com/bioinformaticsdotca/CSHL_2019/master/Module15/MesenchymalvsImmunoreactive_edger_ranks2.rnk)
      

6.	Classes (define which samples are mesenchymal and which samples are immunoreactive) - [MesenchymalvsImmunoreactive_rnaseq_classes.cls](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_GSEA_data/MesenchymalvsImmunoreactive_rnaseq_classes.cls)

7.	Drug target database (preselection of 4 drugs and their target genes u sed in the poast -analysis exercise, <http://www.drugbank.ca/>) - [Human_DrugBank_approved_symbol_selected.gmt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_GSEA_data/Human_DrugBank_approved_symbol_selected.gmt)


Follow the steps described below at your own pace:

### Step 1

Launch Cytoscape and open EnrichmentMap App

**1a**. Double click on the Cytoscape icon

**1b**. Open EnrichmentMap App

* In the top menu bar:

   * Click on Apps -> EnrichmentMap 
 
<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EM1.png?raw=true"  />

A 'Create EnrichmentMap window is now opened.

### Step 2 

Create an enrichment map

**2a**. In the 'Create EnrichmentMap' window, add a dataset of the GSEA type by clicking on the '+' plus sign.

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EMinput.png?raw=true" width="750" />

**2b**. Specify the following parameters and upload the specified files:

*	*Name*: leave default or a name of your choice like "GSEAmap"

*	*Analysis Type*:  GSEA

* *Enrichments Pos*: gsea_report_for_na_pos_1453222854028.xls

* *Enrichments Ned*: gsea_report_for_na_neg_1453222854028.xls

*	*GMT* : Human_GOBP_AllPathways_no_GO_iea_December_24_2015_symbol.gmt

*	*Ranks*: MesenchymalvsImmunoreactive_edger_ranks.rnk

*	*Expressions* : MesenchymalvsImmunoreactive_rnaseq_expression.txt. TIP: this field is optional but recommended
   
*	*Classes*: MesenchymalvsImmunoreactive_rnaseq_classes.cls Tip: this field is optional.

*	*Phenotypes*: In the text boxes place *Mesenchymal*  as the Positive phenotype *Immunoreactive* as the Negative phenotype. Mesenchymal will be associated with red nodes because it corresponds to the positive phenotype and Immunoreactive will be associated with the blue nodes because it corresponds to the negative phenotype.

 *	set FDR q-value cutoff to 0.0001 (= only gene-sets significantly enriched at a value of 0.0001 or less will be displayed on the map). Tip: it will be displayed as  1E-04 in the scientific notation. 

**2c**. Click on *Build*

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EMinput2.png?raw=true" alt="EM" width="750" />

###IMPORTANT### 
We populated the fields manually. If you work with your own data, a way to populate automatically the fields is to drag and drop your GSEA folder in the 'Data Set' window. You are encouraged to give it a try once you finished the lab with your own GSEA results.


**Unformatted results**:

**Note**: layout will be different for each user (there is a random seed in the layout algorithm) but it does not change the results or interpretation (the connections are the same, only the display is different).
 
<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EM3.png?raw=true" alt="EM" width="750" />


### Step 3 

Navigate the enrichment map to gain a better understanding of a EnrichmentMap network. 

General layout of Cytoscape panel: In addition to the main window where the network is displayed, there are 2 panels: the Control Panel on the left side and the Table Panel at the bottom of the window. 

Steps: 

**3a**. In the Cytocape menu bar, select *View* and * Show Graphic details*. It will turn the squared nodes into circles and the gene-set labels will be visible. 
  
<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM5.png?raw=true" alt="EM" width="350" />

**3b**: Zoom in or out using + or - in toolbar or scroll button on mouse until you are able to read the labels comfortably.
 

<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM6.png?raw=true" alt="EM" width="350" />

**3c**:  Use the bird’s eye view (located at the bottom of the control panel) to navigate around the network by moving the blue rectangle using the mouse or trackpad.


<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM7.png?raw=true" alt="EM" width="350" />
  
**3d**: Click on an individual node of interest.

For this example, you could use *Integrins signalling pathway*. 

TIP: If you are unable to locate *Integrins signalling pathway*, type "Integrins signalling pathway" in the search box (quotes are important).  Selected nodes appear yellow (or highlighted) in the network.

**3e**. In the Table Panel in the * EM Heat map* tab change:

* Expressions: "Row Norm*

* Compress: -None-

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EM8.png?raw=true" alt="EM" width="750" />
  
Tip: Genes in the heatmap that are highlighted yellowm (rank column)  represent genes part of the leading edge for this gene set, i.e. contributed the most to the enriched phenotype. Leading edge genes will only be highlighted if an individual node has been selected and the Enrichment Map was created from GSEA results. Troubleshooting: if you don't see the sort column highlighted in yellow, reselect the node of interest and click on the GSEARanking Data Set 1 text in the EM Heatmap tab.


### Step 4

Use Filters to automatically select nodes on the map: Move the blue nodes to the left side of the window and the red nodes to the right side of the window.

**4a**. Locate the *Select* tab from the *Control Panel*.

**4b**. Click on the + sign to view the menu and select *Column Filter*.

**4c**. From the *Choose column …* box, select *Node: ES_dataset1* and set filter values from -0.953 and 0 inclusive.

**4d**. The blue nodes are now automatically selected. Zoom out to be able to look at the entire network and drag all blue nodes to the left side of the screen.
  

<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM9.png?raw=true" alt="EM" width="750" />

**4e**. Optional. Change *is* to *is not* to select the red nodes.
  

<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM10.png?raw=true" alt="EM" width="750" />

Note: the red pathways (nodes) are specific of the mesenchymal phenotype. There were listed in the *pos* table of the GSEA results. The enrichment score (ES) in this table are all positive values. The blue pathways are specific of the immunoreactive phenotype and were listed in the *neg* table of the GSEA results. The ES in this table are all negative values. This information has been used to set the filtering criteria.


### Step 5

Add drug target gene-sets to the network (Add Signature Gene-Sets...).

**5a**. In Control Panel, go to the EnrichmentMap tab and click on "Add Signature Gene Sets..." located below the white 'Data Sets:' window. A window named "EnrichmentMap: Add Signature Gene Sets (Post-Analysis) is now opened.

**5b**. Using the 'Load from File...' button, select the *Human_DrugBank_approved_symbol_selected.gmt* file that you saved on your computer.

**5c**. Click on "Finish". 
  
Note: Four additional nodes are now added to the network and visible as grey diamonds. Dotted orange edges represent their overlap with the nodes of our network. These additional nodes represent gene targets of some approved drugs and these genes are either specific of the mesenchymal type (dotted orange edges connected to red nodes) or specific of the immunoreactive type (dotted orange edges connected to blue nodes).

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/drug1.png?raw=true" alt="EM" width="250" />

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/drug2.png?raw=true" alt="EM" width="750" />

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/drug3.png?raw=true" alt="EM" width="750" />

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/drug4.png?raw=true" alt="EM" width="750" />

tip: more info using this link: https://enrichmentmap.readthedocs.io/en/latest/PostAnalysis.html

### Step 6

Auto-annotate the network with cluster labels.

Important note 1: the Apps WordCloud, ClusterMaker and Autoannotate have to be installed.

Important note 2: if you run step 5, delete the drug targets diamond nodes and associated edge before performing step 6:
select the 4 nodes and associated dotted orange edges by browsing the mouse and click "delete" on your keyboard or in the Cytoscape menu, 'Edit', 'Delete Selected Nodes and Edges'.


**6a**. In the menu bar, select *Apps*, *AutoAnnotate*, *New Annotation Set …*. An *Autoannotate: Create Annotation Set* window pops up. Leave default settings and click on *Create Annotations*.  


<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM12.png?raw=true" alt="EM" width="350" />


In the case that an *AutoAnnotate* window pops up with the message *AutoAnnotate will manage all groups in this network view*, click *OK*.
  

<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM13.png?raw=true" alt="EM" width="350" />


<img src="https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM14.png?raw=true" alt="EM" width="750" />

**Note**: The network is now subdivided into clusters that are represented by ellipses. Each of these clusters are composed of pathways (nodes) interconnected by many common genes. These pathways represent similar biological processes. The app WordCloud take all the labels of the pathways in one cluster and summarize them as a unique cluster label displayed at the top of each ellipse. 

**Tip 1**: further editing and formatting can be performed on the AutoAnnote results using the *AutoAnnotate Display* in the *Results Panels* located at the right side of the window. For example, it is possible to change Ellipse to Rectangle, uncheck *Scale font by cluster size* and increase the *Font Scale* using the scaling bar. It is also possible to reduce the length of the cluster label by checking the "Word Wrap" option.

**Tip 2**: The AutoAnnotate window on the left side in Result Panel contains the list of all clusters. Clicking on a cluster label will highlight in yellow all nodes in this cluster. It is then easy to move the nodes using the mouse to avoid cluster overlaps. 

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/AAStep6dnew.png?raw=true" alt="workflow" width="750" />


**6b**. If your network is dense and clusters are overlapping, there is an option in AutoAnnotate that you can try that expands the network to prevent cluster overlap. In the menu bar, select *Apps*, *AutoAnnotate*, *New Annotation Set …*. An *Autoannotate: Create Annotation Set* window pops up. Check the *Layout network to prevent cluster overlap* and click on *Create Annotations*.  

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/AA6f.png?raw=true" alt="workflow" width="500" />

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/AA6g.png?raw=true" alt="workflow" width="750" />

### Step 7

Visualize genes in a pathway/node of interest using the apps STRING and GeneMANIA. This will create a protein-protein  interaction network using the genes included in the pathway. Note: GeneMANIA theory and practical will be covered in next module.

**7a**: Click on an individual node of interest.

For this example, you could use *Integrins in angiogenesis*. 

TIP: If you are unable to locate *Integrins in angiogenesis*, type "Integrins in angiogenesis" in the search box (quotes are important).  The selected node appears yellow (or highlighted) in the network. If you have annotated your network, it should be included in the *ecm receptor interaction* cluster.

**7b**: Right Click on the node of interest to diplay the option menu. Select *Apps*, *EnrichmentMap - Show in STRING*
A *STRING Protein Query* box appears. Unselect all genes *Select None* and select only the collagen genes with gene name starting with *COL*. Click on *OK*. 

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/Stringa.png?raw=true" alt="workflow" width="500" />

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/Stringb.png?raw=true" alt="workflow" width="500" />

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/Stringc.png?raw=true" alt="workflow" width="750" />


**7c**:Go back to enrichment map network. In Control Panel (left side of the window), select the "Network" tab and click on the Enrichment Map network as shown in below screenshot. 

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/sting_genemani.png?raw=true" alt="workflow" width="500" />


**7d**: Search again for the node labelled *Integrins in angiogenesis* as in Step 7a. Right Click on the node of interest to diplay the option menu. Select *Apps*, *EnrichmentMap - Show in GeneMANIA*. A *GeneMANIA Query* box appears. Unselect all genes *Select None* and select only the collagen genes with gene name starting with *COL*. Click on *OK*. 


<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/Stringa.png?raw=true" alt="workflow" width="500" />

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/Genemaniab.png?raw=true" alt="workflow" width="500" />

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/genemaniaquery.png?raw=true" alt="workflow" width="500" />

<img src="https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/Module15/img/Genemaniac.png?raw=true" alt="workflow" width="750" />


Tip: It is possible to view gene expression data for the nodes in the STRING network. See the section https://enrichmentmap.readthedocs.io/en/latest/Integration.html and try it out after the workshop. 


###SAVE YOUR FILE!###
 



