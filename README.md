# EMBO Practical Course: Metabolite and species dynamics in microbial communities (MCD26-01)

Meta-repository collecting the computational materials for the
[EMBO Practical Course MCD26-01](https://www.embl.org/about/info/course-and-conference-office/events/mcd26-01/).
Each part of the course lives in its own repository and is included here as a
git submodule.

## About the course

- **Dates:** 4–9 October 2026
- **Locations:** EMBL Heidelberg (Germany) and Bangalore Life Science Cluster (India)
- **Organisers:** Sunil Laxman, Ian Probert, Flora Vincent, Elisabeth Zielonka,
  Maria Zimmermann-Kogadeeva

The course introduces integrative approaches for gaining mechanistic insights
into microbiota–environment interactions across native and synthetic
communities, combining top-down (large-scale metagenomic analysis) and
bottom-up (experimental design in the lab) approaches.

Course modules include:

- Experimental design, culture setup and sampling
- 16S analysis using Nanopore sequencing
- Metabolomics analysis (LC-MS)
- Interaction mapping plating experiments
- Computational analysis (RStudio / Python)
- Metabolic community modelling

## Repositories

| Submodule | Description |
|-----------|-------------|
| [`NanoCLUST`](NanoCLUST) | Fork of the [NanoCLUST](https://github.com/genomicsITER/NanoCLUST) pipeline for de novo clustering and consensus building of ONT 16S sequencing data |
| [`Practical5_16S`](Practical5_16S) | Computational practical 5: 16S analysis of axenic and xenic *Chaetoceros neogracilis* cultures — running NanoCLUST on an assigned barcode, then R-based composition, Bray–Curtis and PCoA analysis of the combined profiles |
| [`Practical6_Metabolomics`](Practical6_Metabolomics) | Computational practical 6: untargeted LC-MS metabolomics in R — quality control and feature filtering of an MS-DIAL peak-area export, followed by PCA, ANOVA, heatmap and volcano plot |
| [`Practical7_MetabolicModelling`](Practical7_MetabolicModelling) | Computational practical 7: metabolic modelling of community interactions |

## Usage

Clone the repository together with all submodules:

```bash
git clone --recurse-submodules git@git.embl.org:grp-zimmermann-kogadeeva/EMBO_MCD2026.git
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

Pull the latest commits of all submodules:

```bash
git submodule update --remote --merge
```

### Adding a new part of the course

```bash
git submodule add <repo-url> <directory-name>
git commit -m "Add <directory-name> submodule"
```

Then add a row for it to the [Repositories](#repositories) table above.
