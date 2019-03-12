---
layout: tutorial_page
permalink: /CSHL_2019_Post-Workshop
title: HT-Bio
header1: Workshop Pages for Students
header2: High-throughput Biology - From Sequence to Networks 2019 - Post Workshop
image: /site_images/CBW-CSHL-graphic-square.png
home: https://bioinformaticsdotca.github.io/CSHL_2019
description: HT-Bio Post Workshop
author: Zhibin Lu
modified: March 12, 2019
---

# Post Workshop Access and Instructions

## Docker Container
Docker container from Mathieu Bourgey is [here:](https://hub.docker.com/r/c3genomics/genpipes)

To set up using Docker:
```
mkdir ~/cvmfs_cache
docker run --privileged -v /tmp:/tmp --network host -it -w $PWD -v $HOME:$HOME  -v ~/cvmfs_cache:/cvmfs-cache/    c3genomics/genpipes:0.7
```

To setup using Singularity:
```
singularity run -B ~/cvmfs_cache:/cvmfs-cache/ docker://c3genomics/genpipes:0.7  -V 3.1.2
```

## Data Sets

The data sets in the workshop can be downloaded from below. If your download speed is slow, please contact zhibin&lt;at>gmail.com who can provide you with the alternative methods.

- [Module3 (12.1G)](http://www.hpc4health.ca/cbw/2019/CSHL/Module3.tar)
- [Module4 (3.7G)](http://www.hpc4health.ca/cbw/2019/CSHL/Module4.tar)
- [Module5 (18.7G)](http://www.hpc4health.ca/cbw/2019/CSHL/Module5.tar)
- [Module6 (2.0G)](http://www.hpc4health.ca/cbw/2019/CSHL/Module6.tar)
- [Integrative Assignment for RNA (16.1G)](http://www.hpc4health.ca/cbw/2019/CSHL/Integrative_Assignment_RNA.tar)

## AWS Image

After all the workshop, we will public our AMI. The AMI ID will be here.

## Tools and Installation Instructions
### bioperl
```
sudo apt install expat
perl -MCPAN -e shell
install Module::Build
o conf prefer_installer MB
o conf commit
d /bioperl/
install CJFIELDS/BioPerl-1.007002.tar.gz
```
### R
add "deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/" into /etc/apt/sources.list.d/R.list
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
sudo apt update
sudo apt-get install r-base r-base-dev
```
### abyss
```
sudo apt-get install abyss
```

### bam-readcount
```
git clone https://github.com/genome/bam-readcount.git
cmake bam-readcount/
make
```
### bamtools
```
git clone git://github.com/pezmaster31/bamtools.git
cd bamtools
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=/usr/local ..
make
sudo make install
```
### bedtools
```
wget https://github.com/arq5x/bedtools2/releases/download/v2.27.1/bedtools-2.27.1.tar.gz
tar zxf bedtools-2.27.1.tar.gz
cd bedtools2/
make
sudo make install
```
### blast+
```
wget ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/ncbi-blast-2.8.1+-x64-linux.tar.gz
tar zxf ncbi-blast-2.8.1+-x64-linux.tar.gz
```
### bowtie2
```
wget http://cfhcable.dl.sourceforge.net/project/bowtie-bio/bowtie2/2.3.4.3/bowtie2-2.3.4.3-linux-x86_64.zip
unzip bowtie2-2.3.4.3-linux-x86_64.zip
```
### bwa
```
wget https://newcontinuum.dl.sourceforge.net/project/bio-bwa/bwa-0.7.17.tar.bz2
tar -jxvf bwa-0.7.17.tar.bz2
cd bwa-0.7.17/
make
```
### canu
```
wget wget https://github.com/marbl/canu/releases/download/v1.8/canu-1.8.Linux-amd64.tar.xz
xz -dv canu-1.8.Linux-amd64.tar.xz
tar -xvf canu-1.8.Linux-amd64.tar
```
### Centrifuge
```
wget https://github.com/infphilo/centrifuge/archive/v1.0.4-beta.tar.gz
tar zxf v1.0.4-beta.tar.gz
cd centrifuge-1.0.4-beta/
make

```
### DELLY
```
wget https://github.com/dellytools/delly/releases/download/v0.8.1/delly_v0.8.1_linux_x86_64bit
mv delly_v0.8.1_linux_x86_64bit delly
chmod +x delly
```
### FastQC
```
wget http://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.8.zip
unzip fastqc_v0.11.8.zip
cd FastQC
chmod +x fastqc
```
### Flexbar
```
sudo apt install flexbar
```
### GATK
```
download from https://www.broadinstitute.org/gatk/download (need to log in)
unzip gatk-4.1.0.0.zip
```
### gffcompare
```
wget http://ccb.jhu.edu/software/stringtie/dl/gffcompare-0.10.6.Linux_x86_64.tar.gz
tar zxf gffcompare-0.10.6.Linux_x86_64.tar.gz
```
### GMAP
```
wget http://research-pub.gene.com/gmap/src/gmap-gsnap-2018-07-04.tar.gz
tar -zxf gmap-gsnap-2018-07-04.tar.gz
cd gmap-2018-07-04
./configure
make
sudo make install
```
### HISAT2
```
wget http://ccb.jhu.edu/software/hisat2/dl/hisat2-2.1.0-Linux_x86_64.zip
unzip hisat2-2.1.0-Linux_x86_64.zip && rm hisat2-2.1.0-Linux_x86_64.zip
```
### HMMER
```
wget http://eddylab.org/software/hmmer3/3.1b2/hmmer-3.1b2-linux-intel-x86_64.tar.gz
tar zxf hmmer-3.1b2-linux-intel-x86_64.tar.gz
```
### HTSeq
```
sudo pip install HTSeq
```
### JellyFish
```
wget https://github.com/gmarcais/Jellyfish/releases/download/v2.2.10/jellyfish-linux
chmod +x jellyfish-linux
```
### kallisto
```
wget https://github.com/pachterlab/kallisto/releases/download/v0.45.0/kallisto_linux-v0.45.0.tar.gz
tar zxf kallisto_linux-v0.45.0.tar.gz
```
### medaka
need to modify medaka_variant and medaka_consensus to use python3 because the system default python is version 2.
```
sudo pip3 install medaka
```
### minimap2
```
curl -L https://github.com/lh3/minimap2/releases/download/v2.16/minimap2-2.16_x64-linux.tar.bz2 | tar -jxvf -
./minimap2-2.16_x64-linux/minimap2
```
### MultiQC
```
pip install multiqc
```
### Picard
```
wget https://github.com/broadinstitute/picard/releases/download/2.18.26/picard.jar
```
### pilon
```
wget https://github.com/broadinstitute/pilon/releases/download/v1.23/pilon-1.23.jar
```
### QUAST
```
wget wget https://downloads.sourceforge.net/project/quast/quast-5.0.2.tar.gz
python ./setup.py build
sudo python ./setup.py install
```
### racon
```
wget https://github.com/isovic/racon/releases/download/1.3.2/racon-v1.3.2.tar.gz
tar zxf racon-v1.3.2.tar.gz
cd racon-v1.3.2/
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
```
### regtools
```
wget https://github.com/griffithlab/regtools/archive/0.5.0.tar.gz
cd regtools-0.5.0
mkdir build
cd build/
cmake ..
make
```
### RSEM
```
wget https://github.com/deweylab/RSEM/archive/v1.3.1.tar.gz
tar zxf v1.3.1.tar.gz
cd RSEM-1.3.1/
make
sudo make ebseq (need ‘blockmodeling’, ‘testthat’ R packages)
sudo make install
```
### RSeQC
```
sudo pip install RSeQC
```
### Salmon
```
wget https://github.com/COMBINE-lab/salmon/releases/download/v0.12.0/salmon-0.12.0_linux_x86_64.tar.gz
tar xzf salmon-0.12.0_linux_x86_64.tar.gz
```
### SAMStat
needs samtools to be installed first.
```
wget http://downloads.sourceforge.net/project/samstat/samstat-1.5.1.tar.gz
tar -xzvf samstat-1.5.1.tar.gz
cd samstat-1.5.1/
./configure
make
sudo make install
```
### samtools
```
wget https://downloads.sourceforge.net/project/samtools/samtools/1.9/samtools-1.9.tar.bz2
tar -jxvf samtools-1.9.tar.bz2
cd samtools-1.9
make
sudo make install
```
### snpEff
```
wget https://downloads.sourceforge.net/project/snpeff/snpEff_latest_core.zip
unzip snpEff_latest_core.zip
```
### SPAdas
```
wget http://cab.spbu.ru/files/release3.13.0/SPAdes-3.13.0-Linux.tar.gz
tar xvf SPAdes-3.13.0-Linux.tar.gz
```
### STAR
```
wget https://github.com/alexdobin/STAR/archive/2.7.0c.tar.gz
tar -xzf 2.7.0c.tar.gz
```
### STAR-Fusion
```
wget https://github.com/STAR-Fusion/STAR-Fusion/releases/download/STAR-Fusion-v1.5.0/STAR-Fusion-v1.5.0.FULL.tar.gz
tar zxf STAR-Fusion-v1.5.0.FULL.tar.gz
```
### Strelka
```
wget https://github.com/Illumina/strelka/releases/download/v2.9.10/strelka-2.9.10.release_src.tar.bz2
tar -jxf strelka-2.9.10.release_src.tar.bz2
cd strelka-2.9.10.release_src
mkdir build && cd build
../configure
make -C .
sudo make install
put /usr/local/libexec into PATH
```
### stringtie
```
wget http://ccb.jhu.edu/software/stringtie/dl/stringtie-1.3.5.Linux_x86_64.tar.gz
tar zxf stringtie-1.3.5.Linux_x86_64.tar.gz
```
### TransDecoder
```
wget https://github.com/TransDecoder/TransDecoder/archive/TransDecoder-v5.5.0.tar.gz
tar zxf TransDecoder-v5.5.0.tar.gz
```
### Trimmomatic
```
wget http://www.usadellab.org/cms/uploads/supplementary/Trimmomatic/Trimmomatic-0.38.zip
unzip Trimmomatic-0.38.zip
```
### Trinity
```
wget https://github.com/trinityrnaseq/trinityrnaseq/archive/Trinity-v2.8.4.tar.gz
tar -zxvf Trinity-v2.8.4.tar.gz
cd trinityrnaseq-Trinity-v2.8.4
make
make plugins
```
### Trinotate
```
wget https://github.com/Trinotate/Trinotate/archive/Trinotate-v3.1.1.tar.gz
tar zxf Trinotate-v3.1.1.tar.gz
```

