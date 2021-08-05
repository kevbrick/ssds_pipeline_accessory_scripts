# SSDS pipeline v2.0 Accessory Scripts:
**_Initial paper:_** [Khil et al. Genome Research 2012](https://genome.cshlp.org/content/22/5/957.long)

**_Technical paper:_** [Brick, Pratto et al., Methods in Enzymology 2018](https://www.sciencedirect.com/science/article/pii/S0076687917303750?via%3Dihub)

These scripts are part of the nf-core implementation of the SSDS pipeline. They can also be used stand-alone. 

## Requirements:
*Python modules :*
    - biopython
    - pysam
    - pybedtools

### parse_SSDS_BAM.py
```
parse_SSDS_BAM.py \
  --bam <<bam - BAM from BWA-alignment of SSDS reads>>  \
  --name <<output file prefix>>
```

### parse_SSDS_BAM.py
```
calculate_SPoT.py \
calculate_SPoT.py \\
  --reads <<BED file of reads/fragments>> \
  --intervals <<BED file of intervals to test>> \
  --name <<sample name>> \
  --iname <<intervals name>> \
  --g <<genome index - FASTA.FAI file>>
```