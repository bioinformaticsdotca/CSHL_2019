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

