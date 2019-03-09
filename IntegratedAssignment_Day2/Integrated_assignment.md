---
layout: tutorial_page
permalink: /HTSeq_2018_IA_lab
title: HTSeq Integrated Assignment
header1: Workshop Pages for Students
header2: Informatics on High-Throughput Sequencing Data
image: /site_images/CBW_High-throughput_icon.jpg
home: https://bioinformaticsdotca.github.io/htseq_2018
---


-----------------------

**This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/deed.en_US). This means that you are able to copy, share and modify the work, as long as the result is distributed under the same license.**

-----------------------

# CBW HT-seq Integrative Assignment

 
Written originally by Mathieu Bourgey, edited by Florence Cavalli and Heather Gibling


### Task
We will perform the same analysis as in Module 3, but using the mother and father samples, i.e sample NA12891 and NA12891.

```bash
The fastq files are in the following directory of the cloud instance: ~/CourseData/HT_data/Module3/

 * raw_reads/NA12891/NA12891_CBW_chr1_R1.fastq.gz
 * raw_reads/NA12891/NA12891_CBW_chr1_R2.fastq.gz
 * raw_reads/NA12892/NA12892_CBW_chr1_R1.fastq.gz
 * raw_reads/NA12892/NA12892_CBW_chr1_R2.fastq.gz
```


### Environment setup

```
#set up
export WORK_DIR=~/workspace/HTseq/Integrative_Assignment/
export REF=$WORK_DIR/reference/


rm -rf $WORK_DIR
mkdir -p $WORK_DIR
cd $WORK_DIR
ln -s ~/CourseData/HT_data/Module3/* .

singularity run -B ~/cvmfs_cache:/cvmfs-cache/ docker://c3genomics/genpipes:0.7  -V 3.1.2

module load mugqic/java/openjdk-jdk1.8.0_72 mugqic/bvatools/1.6 mugqic/trimmomatic/0.36 mugqic/samtools/1.9 mugqic/bwa/0.7.17 mugqic/GenomeAnalysisTK/4.1.0.0 mugqic/R_Bioconductor/3.5.0_3.7


```
Task list:

1. Check read QC

2. Trim unreliable bases from the read ends

3. Align the reads to the reference & sort the alignments by chromosome position

4. Realign short indels

5. Mark duplicates

6. Recalibrate the Base Quality

7. Generate alignment metrics


Discussion/Questions:

1. Explain the purpose of each step

2. Which software tool can be used for each step? 




The full commands can be found here [solution](https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/IntegratedAssignment_Day2/integrative_assigment_commands.sh)



