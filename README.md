# Geisbert lab viral genomics analysis pipeline

> DOI pending

## Workflow

1. **Create a host index:** Pull the host reference genome FASTA from [Ensembl](https://ensembl.org) or [NCBI](https://www.ncbi.nlm.nih.gov/home/genomes/). Run `index-bowtie2.sh` to create the [Bowtie2](https://doi.org/10.1038/nmeth.1923) index. 

2. **Create a viral index:** Pull the viral reference genome FASTA from [NCBI](https://www.ncbi.nlm.nih.gov/home/genomes/) as well as the relevant annotation (GTF) file. Run `index-bowtie2.sh` to create the index. Several viral genomes and annotation files are already populated in the `pipeline/` directory. 

3. **Pull the relevant Kraken2 database** from [this link](https://benlangmead.github.io/aws-indexes/k2) or build your own. *Be sure the database directory is located at `pipeline/kraken2db`.*

4. **Run `viral-genomics.sh`** to generate coverage, SNV, consensus, alignment, and metagenomic assignment outputs. All output files will be written to `$ODIR/$SAMPLE/*`.

## Published viruses

| ID | Virus | Strain | GenBank |
| -- | ----- | ------ | ------- |
| `sample033` | JUNV | Rumero | *PENDING* |
