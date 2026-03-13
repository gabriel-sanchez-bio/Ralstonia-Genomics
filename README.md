# Ralstonia-Genomics 🧬
Bioinformatics pipeline for de novo and hybrid genomic assembly of Ralstonia strains using Illumina and Long Read Technology. Includes quality control and evaluation of assembly metrics.
# Ralstonia Genome Assembly 🧬🔋

This repository documents the pipeline used for assembling the genomes of Ralstonia strains (SENASICA). The project covers everything from quality control of raw reads to the generation of high-quality hybrid assemblies.

## 📁 Project Structure

* **`QC-FastQC/`**: Quality reports of sequencing reads (.html files).

* **`Assembly-SPADEs-Illumina_novogene/`**: Scripts and logs of the initial assembly using only short reads (Illumina-novogene).
* **`Assembly-SPADEs-Illumina_SENASICA/`**: Scripts and logs of the initial assembly using only short reads (Illumina-SENASICA).
  
* **`Assembly-Unicycler/`**: Results of the hybrid assembly to obtain circular and complete genomes.

* **`Evaluation-QUAST/`**: Statistical reports to compare the quality between assemblers.

* **`Scripts/`**: Bash files used for process automation.

## Tools and Methodology

### 1. Quality Control
Library quality was assessed using **FastQC**. GC content metrics and Phred scores were reviewed to ensure data integrity.

### 2. De Novo Assembly (Illumina)
Using **SPAdes**, initial contigs were generated. This stage was crucial for identifying the genomic complexity of the *Ralstonia* strains.

### 3. Hybrid Assembly
**Unicycler** was used to combine the precision of short reads (Illumina) with the scaffolding capabilities of long reads. This allowed for the resolution of repetitive regions and, in some cases, the closure of chromosomes and plasmids.

### 4. Quality Assessment
The **QUAST** tool was used to generate a comparative table of metrics:
* **N50**: Smallest contig length in which 50% of the genome is represented.

* **L50**: Minimum number of contigs that cover 50% of the genome.

## 📚 Citations
* **SPADEs**: Bankevich, A., et al. (2012).

* **Unicycler**: Wick, R. R., et al. (2017).

* **QUAST**: Gurevich, A., et al. (2013).

---
