# SSDS pipeline Accessory Scripts:
**_Initial paper:_** [Khil et al. Genome Research 2012](https://genome.cshlp.org/content/22/5/957.long)

**_Technical paper:_** [Brick, Pratto et al., Methods in Enzymology 2018](https://www.sciencedirect.com/science/article/pii/S0076687917303750?via%3Dihub)

These scripts are part of the nf-core implementation of the SSDS pipeline. They can also be used stand-alone. 

## Requirements:
*Python modules :*
    <br>- biopython
    <br>- pysam
    <br>- pybedtools

### parse_SSDS_BAM.py\
Parse the BWA-aligned BAM file from an SSDS experiment. Identifies DNA derived from ssDNA, dsDNA and other unclassifiable things. Outputs BED & BAM files for fragments of each type. 
```
parse_SSDS_BAM.py
  --bam <<bam - BAM from BWA-alignment of SSDS reads>>
  --name <<output file prefix>>
  --vers <<show version>>
```

### calculate_SPoT.py
Calculates the Signal Portion of Tags (SPoT) - actually fragments, but that's OK :) - for a given BED file of intervals. Generally used to check SSDS signal @ DSB hotspots / origins of replication.
```
calculate_SPoT.py
  --reads <<BED file of reads/fragments>>
  --intervals <<BED file of intervals to test>>
  --name <<sample name>>
  --iname <<intervals name>>
  --g <<genome index - FASTA.FAI file>>
  --o <<output report prefix - file will be $prefix.SSDS_SPoT_report.txt>>
  --norand <<do not get SPoT for a randomized set>>
  --vers <<show version>>
```
