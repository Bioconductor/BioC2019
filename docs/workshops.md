---
layout: default
---
# BioC 2018: Where Software and Biology Connect

When: July 25 (Developer Day) 26 and 27, 2018 <br />
Where: [Victoria University][venue], University of Toronto, Toronto, Canada<br />
Twitter: [#bioc2018][tweet]

[tweet]: https://twitter.com/hashtag/bioc2018
[venue]: ./travel-accommodations

## Workshops

Join the _[Bioconductor][]_ Community Slack and #bioc2018-workshops
channel for up-to-date information.

- [Main Conference](#main-conference)
- [Developer Day](#developer-day)

### Main Conference

- Lee S*, Lawrence M. _Fluent genomic data analysis with
  [plyranges][]_. [Syllabus & Materials][Lee_Plyranges].

  In this workshop, we will give an overview of how to
  perform low-level analyses of genomic data using the grammar of
  genomic data transformation defined in the plyranges package. We
  will cover:

    - introduction to GRanges
    - overview of the core verbs for arithmetic, restriction, and
      aggregation of GRanges objects
    - performing joins between GRanges objects
    - designing pipelines to quickly explore data from AnnotationHub
    - reading BAM and other file types as GRanges objects

  The workshop will be a computer lab, in which the participants will
  be able to ask questions and interact with the instructors."

- MacDonald J, Shepherd L. _Introduction to [Bioconductor][]
  annotation resources_. [Syllabus & Materials][MacDonald_Annotation].

  There are various annotation packages provided by the
  _[Bioconductor][]_ project that can be used to incorporate
  additional information to results from high-throughput
  experiments. This can be as simple as mapping Ensembl IDs to
  corresponding HUGO gene symbols, to much more complex queries
  involving multiple data sources. In this workshop we will cover the
  various classes of annotation packages, what they contain, and how
  to use them efficiently.

- Levi Waldron, Benjamin Haibe-Kains, Sean Davis. _Public Data
  Resources and [Bioconductor][]_. [Syllabus & Materials][Waldron_PublicData].

  The goal of this workshop is to introduce _[Bioconductor][]_
  packages for finding, accessing, and using large-scale public data
  resources including the Gene Expression Omnibus
  [GEO](https://www.ncbi.nlm.nih.gov/geo), Sequence Read Archive
  [SRA](https://www.ncbi.nlm.nih.gov/sra), the Genomic Data Commons
  [GDC](https://portal.gdc.cancer.gov/), and _[Bioconductor][]_-hosted
  curated data resources for metagenomics, pharmacogenomics, and The
  Cancer Genome Atlas.

- Love MI.  _RNA-seq data analysis with [DESeq2][]_. [Syllabus & Materials][Love_DESeq2].

  In this workshop, we will give a quick overview of the most useful
  functions in the [DESeq2][] package, and a basic RNA-seq
  analysis. We will cover: how to quantify transcript expression from
  FASTQ files using Salmon, import quantification from Salmon with
  [tximport][] and [tximeta][], generate plots for quality control and
  exploratory data analysis EDA (also using [MultiQC][]), perform
  differential expression (DE) (also using [apeglm][]), overlap with
  other experimental data (using [AnnotationHub][]), and build reports
  (using [ReportingTools][] and [Glimma][]). We will give a short
  example of integration of [DESeq2][] with the zinbwave package for
  single-cell RNA-seq differential expression. The workshop is
  designed to be a lab with plenty of time for questions throughout
  the lab.

- Charity Law , Monther Alhamdoosh, Shian Su, Gordon Smyth and Matthew
  Ritchie. _RNA-seq analysis is easy as 1-2-3 with [limma][],
  [Glimma][] and [edgeR][]_. [Syllabus & Materials][Law_RNAseq123].

  In this workshop, we analyse RNA-sequencing data from the mouse
  mammary gland, demonstrating use of the popular edgeR package to
  import, organise, filter and normalise the data, followed by the
  [limma][] package with its voom method, linear modelling and
  empirical Bayes moderation to assess differential expression. This
  pipeline is further enhanced by the [Glimma][] package which enables
  interactive exploration of the results so that individual samples
  and genes can be examined by the user. The complete analysis offered
  by these three packages highlights the ease with which researchers
  can turn the raw counts from an RNA-sequencing experiment into
  biological insights using _[Bioconductor][]_.


- Michael Lawrence, Martin Morgan.  _Solving common bioinformatic
  challenges using [GenomicRanges][]_. [Syllabus & Materials][Lawrence_GenomicRanges].

  We will introduce the fundamental concepts underlying the
  [GenomicRanges][] package and related infrastructure. After a
  structured introduction, we will follow a realistic workflow, along
  the way exploring the central data structures, including `GRanges`
  and `SummarizedExperiment`, and useful operations in the ranges
  algebra. Topics will include data import/export, computing and
  summarizing data on genomic features, overlap detection, integration
  with reference annotations, scaling strategies, and
  visualization. Students can follow along, and there will be plenty
  of time for students to ask questions about how to apply the
  infrastructure to their particular use case.

- Zhaleh Safikhani, Petr Smirnov, Benjamin Haibe-Kains. _Biomarker
  discovery from large pharmacogenomics datasets_. [Syllabus & Materials][Safikhani_Pharmacogenomics].

  This workshop will focus on the challenges encountered when applying
  machine learning techniques in complex, high dimensional biological
  data. In particular, we will focus on biomarker discovery from
  pharmacogenomic data, which consists of developing predictors of
  response of cancer cell lines to chemical compounds based on their
  genomic features. From a methodological viewpoint, biomarker
  discovery is strongly linked to variable selection, through methods
  such as Supervised Learning with sparsity inducing norms (e.g.,
  ElasticNet) or techniques accounting for the complex correlation
  structure of biological features (e.g., mRMR). Yet, the main focus
  of this talk will be on sound use of such methods in a
  pharmacogenomics context, their validation and correct
  interpretation of the produced results. We will discuss how to
  assess the quality of both the input and output data. We will
  illustrate the importance of unified analytical platforms, data and
  code sharing in bioinformatics and biomedical research, as the data
  generation process becomes increasingly complex and requires high
  level of replication to achieve robust results. This is particularly
  relevant as our portfolio of machine learning techniques is ever
  enlarging, with its set of hyperparameters that can be tuning in a
  multitude of ways, increasing the risk of overfitting when
  developing multivariate predictors of drug response.

- Ludwig Geistlinger and Levi Waldron. _Functional enrichment analysis
  of high-throughput omics
  data_. [Syllabus & Materials][Geistlinger_Omics].

  This workshop gives an in-depth overview of existing methods for
  enrichment analysis of gene expression data with regard to
  functional gene sets, pathways, and networks.

  The workshop will help participants understand the distinctions
  between assumptions and hypotheses of existing methods as well as
  the differences in objectives and interpretation of results. It will
  provide code and hands-on practice of all necessary steps for
  differential expression analysis, gene set- and network-based
  enrichment analysis, and identification of enriched genomic regions
  and regulatory elements, along with visualization and exploration of
  results.


- Ramos M, Geistlinger L, Waldron L. _Workflow for Multi-omics
  Analysis with [MultiAssayExperiment][]_. [Syllabus & Materials][Ramos_MultiAssayExperiment].

  This workshop demonstrates data management and analyses of multiple
  assays associated with a single set of biological specimens, using
  the `MultiAssayExperiment` data class and methods. It introduces the
  `RaggedExperiment` data class, which provides efficient and powerful
  operations for representation of copy number and mutation and
  variant data that are represented by different genomic ranges for
  each specimen. "

- Das D*, Street K*, Risso D. _Analysis of single-cell RNA-seq data:
  Dimensionality reduction, clustering, and lineage inference_.
  [Workshop Syllabus & Materials][Das_SingleCellRNAseq].

  This workshop will be presented as a lab session (brief introduction
  followed by hands-on coding) that instructs participants in a
  _[Bioconductor][]_ workflow for the analysis of single-cell
  RNA-sequencing data, in three parts:

    1. dimensionality reduction that accounts for zero inflation,
       over-dispersion, and batch effects
    2. cell clustering that employs a resampling-based approach
       resulting in robust and stable clusters
    3. lineage trajectory analysis that uncovers continuous, branching
       developmental processes

  We will provide worked examples for lab sessions, and a set of
  stand-alone notes in this repository.

- Isserlin R,Innes B, Bader GD. _[Cytoscape][] Automation in R using
  [Rcy3][]_.  [Workshop Syllabus & Materials][Isserlin_Rcy3].

  [Cytoscape][] is one of the most popular applications for
  network analysis and visualization. In this workshop, we will
  demonstrate new capabilities to integrate Cytoscape into
  programmatic workflows and pipelines using R. We will begin with an
  overview of network biology themes and concepts, and then we will
  translate these into Cytoscape terms for practical applications. The
  bulk of the workshop will be a hands-on demonstration of accessing
  and controlling Cytoscape from R to perform a network analysis of
  tumor expression data.

- Coetzee SG and Hazelett DJ. _Variant Functional Annotation using
  [StatePaintR][], [FunciVar][] and
  [MotifBreakR][]_. [Syllabus & Materials][Coetzee_StatePaintR].

  This workshop focuses on _[Bioconductor][]_ based tools for
  non-coding variant annotation. I will present a high level overview
  of these concepts and the bioconductor tools our group uses to
  address them *in silico*. These tools can be used for germline or
  somatic variants, but as we will see, can also be used for any other
  feature represented as GRanges objects.

- Cooley N and Wright E. _Working with Genomic Data in R with the
  DECIPHER package_. [Syllabus & Materials][Cooley_DECIPHER].

  [DECIPHER][] is a multifaceted package that includes many tools for
  working with genome-scale sequence data. Genomic sequences undergo a
  variety of large-scale mutational processes, including
  rearrangements, inversions, duplications, insertions, and
  deletions. Since genomes are often not collinear, it is often useful
  to map syntenic regions between genomes to facilitate
  analyses. DECIPHER contains a synteny mapping function that locates
  syntenic regions among genomes and can be used to identify
  orthologous genes. Additional functions allow for alignment and
  downstream analyses of these syntenic regions. This workshop will
  walk through a complete workflow for analyzing a set of genomes
  using DECIPHER, starting with importing genomes from local files or
  external repositories. Synteny will be mapped among multiple genomes
  and used as the basis for ortholog prediction. We will show how to
  use these sets of orthologous genes to construct phylogenetic trees
  representing the evolutionary history of the core-genome and
  pan-genome.

### Developer Day

- Hickey P.F.* _Effectively using the [DelayedArray][] framework to
  support the analysis of large
  datasets_. [Syllabus & Materials][Hickey_DelayedArray].

  This workshop will teach the fundamental concepts underlying the
  DelayedArray framework and related infrastructure. It is intended
  for package developers who want to learn how to use the
  [DelayedArray][] framework to support the analysis of large
  datasets, particularly through the use of on-disk data storage. The
  first part of the workshop will provide an overview of the
  [DelayedArray][] infrastructure and introduce computing on
  DelayedArray objects using delayed operations and
  block-processing. The second part of the workshop will present
  strategies for adding support for [DelayedArray][] to an existing
  package and extending the [DelayedArray][] framework. Students can
  expect a mixture of lecture and question-and-answer session to teach
  the fundamental concepts. There will be plenty of examples to
  illustrate common design patterns for writing performant code,
  although we will not be writing much code during the workshop.

- Nitesh Turaga. Roswell Park Comprehensive Cancer
  Center. _Maintaining your [Bioconductor][]
  package_. [Syllabus & Materials][Turaga_MaintainBioc].

  Once an R package is accepted into _[Bioconductor][]_, maintaining
  it is an active responsibility undertaken by the package developers
  and maintainers. In this short workshop, we will cover how to
  maintain a _[Bioconductor][]_ package using existing
  infrastructure. _[Bioconductor][]_ hosts a range of tools which
  maintainers can use such as daily build reports, landing page
  badges, RSS feeds, download stats, support site questions, and the
  bioc-devel mailing list. Some packages have their own continuous
  integration hook setup on their github pages which would be an
  additional tool maintainers can use to monitor their package. We
  will also highlight one particular git practice which need to be
  done while updating and maintaining your package on out git system.

[AnnotationHub]: https://bioconductor.org/packages/AnnotationHub
[Bioconductor]: https://bioconductor.org/developers
[DESeq2]: https://bioconductor.org/packages/DESeq2
[DECIPHER]: https://bioconductor.org/packages/DECIPHER
[DelayedArray]: https://bioconductor.org/packages/DelayedArray
[FunciVar]: https://bioconductor.org/packages/FunciVar
[GenomicRanges]: https://bioconductor.org/packages/GenomicRanges
[Glimma]: https://bioconductor.org/packages/Glimma
[MotifBreakR]: https://bioconductor.org/packages/MotifBreakR
[MultiAssayExperiment]: https://bioconductor.org/packages/MultiAssayExperiment
[MultiQC]: https://bioconductor.org/packages/MultiQC
[Rcy3]: https://bioconductor.org/packages/Rcy3
[ReportingTools]: https://bioconductor.org/packages/ReportingTools
[StatePaintR]: https://bioconductor.org/packages/StatePaintR
[apeglm]: https://bioconductor.org/packages/apeglm
[edgeR]: https://bioconductor.org/packages/edgeR
[limma]: https://bioconductor.org/packages/limma
[plyranges]: https://bioconductor.org/packages/plyranges
[tximport]: https://bioconductor.org/packages/tximport
[txmeta]: https://bioconductor.org/packages/txmetta

[Cytoscape]: http://www.cytoscape.org/

[Coetzee_StatePaintR]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Coetzee_StatePaintR.Rmd
[Cooley_DECIPHER]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Cooley_DECIPHER.Rmd
[Das_SingleCellRNAseq]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Das_SingleCellRNAseq.Rmd
[Geistlinger_Omics]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Geistlinger_Omics.Rmd
[Hickey_DelayedArray]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Hickey_DelayedArray.Rmd
[Isserlin_Rcy3]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Isserlin_Rcy3.Rmd
[Law_RNAseq123]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Law_RNAseq123.Rmd
[Lawrence_GenomicRanges]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Lawrence_GenomicRanges.Rmd
[Lee_Plyranges]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Lee_Plyranges.Rmd
[Love_DESeq2]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Love_DESeq2.Rmd
[MacDonald_Annotation]: https://github.com/Bioconductor/BiocWorkshops/blob/master/MacDonald_Annotation.Rmd
[Ramos_MultiAssayExperiment]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Ramos_MultiAssayExperiment.Rmd
[Safikhani_Pharmacogenomics]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Safikhani_Pharmacogenomics.Rmd
[Turaga_MaintainBioc]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Turaga_MaintainBioc.Rmd
[Waldron_PublicData]: https://github.com/Bioconductor/BiocWorkshops/blob/master/Waldron_PublicData.Rmd
