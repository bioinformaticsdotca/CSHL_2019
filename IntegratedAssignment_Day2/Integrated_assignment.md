---
layout: tutorial_page
permalink: /CSHL_2019_IA_Day2
title: HT-Bio
header1: Workshop Pages for Students
header2: High-throughput Biology - From Sequence to Networks 2019 - Integrated Assignment Day 2
image: /site_images/CBW-CSHL-graphic-square.png
home: https://bioinformaticsdotca.github.io/CSHL_2019
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

#### Task list:

1. Check read QC

2. Trim unreliable bases from the read ends

3. Align the reads to the reference & sort the alignments by chromosome position

4. Realign short indels

5. Mark duplicates

6. Recalibrate the base quality

7. Generate alignment metrics


#### Discussion/Questions:

1. Explain the purpose of each step

2. Which software tool can be used for each step? 



The full commands can be found [here](https://github.com/bioinformaticsdotca/CSHL_2019/blob/master/IntegratedAssignment_Day2/integrative_assigment_commands.sh), but try to work on it yourself before checking!

---

### Optional

Perform the same analysis as in Module 4, but using the mother and father samples, i.e sample NA12891 and NA12891.

Some additional things you can look at:

1. **If you load up all three realigned BAM files and all three final vcf files into IGV, do the variants look plausible?** Use a [Punnett square](https://en.wikipedia.org/wiki/Punnett_square) to help evaluate this. i.e. if both parents have a homozygous reference call and the child has a homozygous variant call at that locus, this might indicate a trio conflict. [solution](https://github.com/mbourgey/CBW_HTseq_module4/blob/master/solutions/_trio1.md)

 2. **Do you find any additional high or moderate impact variants in either of the parents?** [solution](https://github.com/mbourgey/CBW_HTseq_module4/blob/master/solutions/_trio2.md)

 3. **Do all three family members have the same genotype for Rs7538876 and Rs2254135?** [solution](https://github.com/mbourgey/CBW_HTseq_module4/blob/master/solutions/_trio3.md)

 4. GATK produces even better variant calling results if all three BAM files are specified at the same time (i.e. specifying multiple `-I filename` options). Try this and then perform the rest of module 5 on the trio vcf file. **Does this seem to improve your variant calling results? Does it seem to reduce the trio conflict rate?** [solution](https://github.com/mbourgey/CBW_HTseq_module4/blob/master/solutions/_trio4.md)

 Remember to quit the singularity container environment on AWS:

```
exit
```
