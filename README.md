
<!-- README.md is generated from README.Rmd. Please edit that file -->

# geneticMapRFiles

This repository stores data files used alongside the
[geneticMapR](https://vegaalfaro.github.io/geneticMapR/) R package.

## Repository Purpose

This data-only repository hosts example and large-scale datasets used
for development, testing, and demonstration of the `geneticMapR`
package. These datasets are not included in the main CRAN package due to
size limitations.

## Folder Structure

- `IDs`: Sample names and pedigree
- `phenotype`: phenotypic data
- `vcf`: genotypic data, usually in vcf format.
- `R_data`: RDAs and other R objects and datasets.

## Usage

These files can be accessed in your R workflows by downloading them
directly or by linking this GitHub repo in your pipeline.

## Related Package

See the main package:
[`geneticMapR`](https://github.com/vegaalfaro/geneticMapR)

## License

MIT

## Files Description

### IDs

- `ID-Pedigrees-Biparentals-2025-01-22.xlsx`: This table contains
  sample-level metadata for individuals in a genetic study which
  corresponds to samples in a VCF file and downstream analysis.

### phenotype

- `phenotypes-binary.csv`: Phenotypic data of root shapes for an
  F<sub>2</sub> mapping population of *Beta vulgaris*. Data includes
  unique identifiers and sample identifiers. Phenotype columns start at
  column I.

### R_data

The **filtered_geno_matrices_1629.RData** file contains the following R
objects:

- `hom_phased_geno_1629`: A genotype matrix of 2845 markers by 104
  individuals. It keeps only homozygous markers (where parents are fixed
  for either 0 or 2 alleles). Filtered for missing data.
- `het_phased_geno_1629`: A genotype matrix of of 12,155 markers and 104
  individuals. It keeps homozygous and heterozygous markers.
- `het_phased_geno_1629_filt`: A filtered version of
  `het_phased_geno_1620` with 6482 markers and 104 individuals.
  Filtering parameters and procedures are explained in this
  [article](https://vegaalfaro.github.io/geneticMapR/articles/Recode.html).
- markers_homozygous: dimensions of `hom_phased_geno_1629`
- markers_heterozygous: dimensions of `het_phased_geno_1629_filt`

The **binned_geno_1629.RData** file contains the following R objects:

- `geno.het.bin`: A genotype matrix of 2480 **binned** markers by 100
  individuals. Includes heterozygous and homozygous markers.

- `geno.hom.bin`: A genotype matrix of 998 **binned** markers by 100
  individuals. Includes homozygous markers only.

- `dendro`: a ggplot object showing a dendrogram used to visualize
  relationship among samples.

The **LODmats_1629-2025-03-12.RData** file contains the following R
objects:

- `LODmat.het`: Large matrix containing LOD scores for each marker pair.
  Heterozygous markers and Homozygous markers.

- `LODmat.hom`:Large matrix containing LOD scores for each marker pair.
  Homozygous markers.

### vcf

- `SNP_updated_IDs_sorted2.vcf.gz`: This is a lightly filtered version
  of the VCF file that contains genetic markers and individuals. The
  marker names have been processed for clarity.

**Last updated:**

    #> [1] "2025-05-06"
