# Copying results

### On AWS:

Navigate to directory with your results

* Check size of files and directories, and think about what you'd like to save
* Don't need original data (we have that for you on the course website), software tools (can be downloaded)

```
cd ~/workspace/rnaseq/integrated_assignment
du -sh *
```

This shows size of all files and directories in the integrated assignment folder
* hisat2 directory is very big--probably don't need to save this because we can recreate the indexes from the original data


Best to compress files into one folder for transferring (quicker, more organized)
* Make a directory to store the files you want to copy over

```
mkdir rna-backup
```

* Move files into this directory
* List everything you want to move, and the last item in the list is where the files will be moved
* Use regex to grab similarly named files (`*`)

```
mv Normal* Tumor* adapter ballgown expression multqc_report.html trimmed_reads rna-backup
```

Compress the folder that will be copied to your computer
* name of compressed file, followed by what you are compressing (can be multiple files/directories)

```
tar -vczf rna-backup.tar.gz rna-backup
```

### On your home computer

Navigate to the directory with your AWS permisions key (CBWNY.pem, CBWNY.pbk)
* Copy over using your student number instead of XX

```
rsync -azv -e "ssh -i CBWNY.pem" ubuntu@XX.oicrcbw.ca:/home/ubuntu/workspace/rnaseq/integrated_assignment/rna-backup.tar.gz .
```
