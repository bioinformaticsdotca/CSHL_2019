---
layout: tutorial_page
permalink: /CSHL_2019_laptop_setup
title: HT-Biology
header1: Workshop Pages for Students
header2: High-Throughput Biology - From Sequence to Networks
image: /site_images/CBW-CSHL-graphic-square.png
home: https://bioinformaticsdotca.github.io/CSHL_2019
---

1) Install latest version of R which can be downloaded from http://probability.ca/cran/.

1b) Download and install the most recent version of [R Studio desktop](http://www.rstudio.com/).  If prompted to install git, select yes.

2) Install the BioConductor core packages. To do this, open R and at the '>' prompt, paste the commands:

```r
source("http://bioconductor.org/biocLite.R"); 
biocLite();
```

3) A robust text editor.   

* For Windows/PC - [notepad++](http://notepad-plus-plus.org/)  
* For Linux - [gEdit](http://projects.gnome.org/gedit/)  
* For Mac – [TextWrangler](http://www.barebones.com/products/textwrangler/download.html)

4) A file decompression tool.  

* For Windows/PC – [7zip](http://www.7-zip.org/).  
* For Linux – [gzip](http://www.gzip.org).   
* For Mac – already there.

5) A robust internet browser such as Firefox or Safari (Internet Explorer and Chrome are not recommended because of Java issues).

6) Java -The visualization program that we will be using (IGV) requires Java. Check if you have Java installed: https://www.java.com/verify/ and download Java if you do not have it installed (Java 8).

7) Integrative Genomics Viewer 2.3 (IGV) - Once java is installed, go to http://www.broadinstitute.org/igv/ and register in order to get access to the downloads page. Once you have gained access to the download page, click on the appropriate launch button that matches the amount of memory available on your laptop (if you have space, 1.2GB is good, more is better).   

**Note** Chrome does not launch "java webstart" files by default. Instead, the launch buttons below will download a "jnlp" file. This should appear in the lower left corner of the browser. Double-click the downloaded file to run.   

**Windows users:** To run with more than 1.2 GB you must install 64-bit Java. This is often not installed by default even with the latest Windows 7 machines with many GB of memory. In general trying to launch with more memory than your OS/Java combination supports will result in the obscure error "could not create virtual machine".

8) SSH client - Mac and Linux users already have a command line ssh program that can be run from the terminal. For Windows users, please download [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).  

9) SCP/SFTP client - We will be moving data from the servers to the student laptops for visualization. Mac and Linux users already have a command line scp and sftp program. For Windows users, please install [WinSCP](http://winscp.net/eng/download.php).

10) A PDF viewer (Adobe Acrobat or equivalent).

11) fastqc – This tool is available for Windows/Mac/Linux [here](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/).

12) Install [Cytoscape 3.4.0](http://chianti.ucsd.edu/cytoscape-3.4.0/).  

Choose the version corresponding to your operating system (OS, Windows or UNIX) 
Cytoscape requires Java8: check your version at  https://www.java.com/verify/ and download Java8 if you do not have it installed. Contact your system administrator if you have trouble with Java installation. 

13) Within the Cytoscape program, install the following Cytoscape apps.  

From the menu bar, select ‘Apps’ , ‘Manage Apps’.
 
Within all apps, search for the following and install:  

 * EnrichmentMap 
 * EnrichmentMap Pipeline Collection (it will install ClusterMaker2, WordCloud and AutoAnnotate) 
 * GeneMania 
 * Iregulon  
 * ReactomeFIPlugin - http://apps.cytoscape.org/apps/reactomefiplugin  
 
 
4) Install the data set within GeneMANIA.

Select GeneMania from Apps Manager and Choose Another Data Set.  
From the list of available data sets, select the most recent (2014-08-12/1 June 2014) and under ‘Include only these networks’: select ‘all’. Click on ‘Download’.  
An ‘Install Window’ will pop-up. Select H.Sapiens Human (2384 MB). Click on ‘Install’.  
This requires time and a good network connection to download completely, so be patient (around 15mins).  

  
5) Install GSEA.  

Go to the [GSEA page](http://www.broadinstitute.org/gsea/index.jsp)    
Register  
Login  
In menu, choose Downloads  
Go to the javaGSEA Java Jar file section and download the gsea2-2.2.3.jar file and save in your Documents folder (do not leave it in the “Downloads”folder).  
 
To run GSEA during the workshop, you must use the command line. You will need to open a terminal and execute the install commands. Since we will need to run GSEA this same way each time, it will be a good idea to save this information on how to run GSEA.
 
**MAC/Linux Computer** 

* On a MAC, the Terminal window is located in Applications/Utilities. Tip: add the terminal window to your dock so it is easy to open when needed.  
* At the prompt, type the command in your terminal window and hit enter:

```
java -Xmx2G -jar ~/Documents/gsea2-2.2.3.jar
```

**PC/Windows Computer** 

* On Windows, go to the start icon and type cmd (for command prompt) in the search box.  
* At the prompt, type the following commands, hitting enter in between each command and waiting for the prompt before the next command:

```
cd Documents
java -Xmx2G -jar gsea2-2.2.3.jar
```
