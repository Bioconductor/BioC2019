---
layout: default
---
# BioC 2019: Where Software and Biology Connect

When: June 24 - 27, 2019<br />
What: Developer Day, Main Conference, Symposium<br />
Where: [NYU and Rockefeller University][venue], New York City, USA<br />
Slack: [Bioconductor Team][] (`#bioc2019` channel)<br />
Twitter: [#bioc2019][tweet]<br />

[tweet]: https://twitter.com/hashtag/bioc2019?f=tweets
[venue]: ./travel-accommodations
[Bioconductor Team]: https://bioc-community.herokuapp.com/

## Community-Contributed Talks (Tentative)

- See the Conference [Schedule](schedule.md) for invited talks.

- Lee S\*, Cook D, Lawrence M. _[plyranges][]: a fluent interface to
  Bioconductor's Ranges infrastructure_. The Bioconductor project has
  created many powerful S4 classes for reasoning about genomics data,
  such as the SummarizedExperiment class for representing experimental
  assays and the Ranges family of classes for representing genomic
  intervals. For new users of Bioconductor who are unfamiliar with
  object oriented programming or genomic data analysis, the learning
  curve for these classes is steep. New users often find themselves
  asking: how do I get my data into an appropriate class for my
  analysis? What are accessors and why do I have to use them? Why does
  this function return an object of class that I have not seen before?
  This results in analysts trying to solve problems that have been
  efficiently dealt with in other Bioconductor packages or writing
  code they may not fully understand.

  The goal of a fluent interface is to enable users to write
  human-readable code via method chaining and consistent function
  returns. Fluent interfaces fit naturally in the context of
  Bioinformatics workflows because they enable writing succinct
  pipelines. We have developed plyranges a package that attempts to
  construct a fluent interface to the Ranges classes defined in the
  IRanges and [GenomicRanges][] packages. This package is inspired by
  [dplyr][] and implements and extends its grammar of data
  manipulation to Ranges. We have defined methods for constructing,
  grouping, mutating, filtering, and summarising Ranges. We have also
  defined an algebra for reasoning about actions on Ranges and
  relationships between Ranges. By having an expansive grammar, we
  hope to cover the majority of analysis tasks a new user may face and
  thereby enable users to write clearer and more reproducible code.

- Zhun Miao\*, Ke Deng, Xiaowo Wang, Xuegong Zhang. _[DEsingle][] for
  detecting three types of differential expression in single-cell
  RNA-seq data_. The excessive amount of zeros in single-cell RNA-seq
  (scRNA-seq) data includes ‘real’ zeros due to the on-off nature of
  gene transcription in single cells and ‘dropout’ zeros due to
  technical reasons. Existing differential expression (DE) analysis
  methods cannot distinguish these two types of zeros.

  We developed an R package [DEsingle][] which employed Zero-Inflated
  Negative Binomial model to estimate the proportion of real and
  dropout zeros and to define and detect three types of DE genes in
  scRNA-seq data, with regard to different expression status (DEs),
  differential expression abundance (DEa), and general differential
  expression (DEg).

  Results showed that [DEsingle][] outperforms existing methods for
  scRNA-seq DE analysis, and can reveal different types of DE genes
  that are enriched in different biological functions.

- Abbas Rizvi\*, Ezgi Karaesmen\*, Leah Preus, Michael Sovic, Junke
  Wang, Lara Sucheston-Campbell. _[gwasurvivr][]: an R package to
  perform survival association testing on imputed genetic data_.
  Increasingly researchers have become interested in time-to-event
  outcomes in the context of genetic variation. Existing software for
  performing survival analyses across millions of SNPs are
  limited. Recently, comprehensive stand-alone software packages,
  genipe and SurvivalGWAS_SV, were developed, however, they require
  user interaction with the raw output after imputation opening room
  for error during analysis. GWASTools, while available in R and can
  implement survival, is primarily for storing large SNP datasets and
  rigorous QC/QA. To address this unmet need, we developed an
  R/Bioconductor package to conduct fast and efficient genome wide
  survival analyses for on imputed genetic data generated using
  IMPUTE2 and VCF data generated from Michigan or Sanger imputation
  servers.

  [gwasurvivr][] implements Cox proportional hazards models to test
  SNP association with outcome; the package allows for covariates and
  SNP-covariate interaction. To potentially decrease the number of
  iterations needed for convergence when optimizing the parameters
  estimates in the Cox model, we modified survival::coxph.fit, to fit
  covariates without the SNP and use those parameter estimates as
  initial starting points. For models without covariates the parameter
  estimation optimization begins with null initial value. Users can
  internally subset the data by providing sample IDs and pre-filter
  SNPs by info score and MAF. Output for each SNP includes parameter
  estimates, p-values, MAFs, INFO scores, number of events and total
  sample N. [gwasurvivr][] is well-suited for multi-core processors
  and users can specify node preferences used during computation. To
  overcome R memory limitations [gwasurvivr][] iteratively performs
  survival on subsets of the entire data.

  We benchmarked our package with genipe, SurvivalGWAS_SV, and
  GWASTools using IMPUTE2 data for varying sample sizes (n=100,
  n=1000, n=5000) and SNPs (p=1000, p=10000, p=100000) including two
  non-genetic covariates. All packages showed excellent agreement
  across MAF estimates, coefficient estimates, and p-values, with
  [gwasurvivr][] outperforming the other packages in time to
  completion for all simulations.

- Ludwig Geistlinger, Gergely Csaba, Mara Santarelli, Lucas Schiffer,
  Marcel Ramos, Ralf Zimmer, and Levi Waldron. _Towards a gold
  standard for benchmarking gene set enrichment analysis._ Although
  gene set enrichment analysis has become an integral part of
  high-throughput gene expression data analysis, the assessment of
  enrichment methods remains rudimentary and ad hoc. In the absence of
  suitable gold standards, the evaluation is commonly restricted to
  selected data sets and biological reasoning on the relevance of
  resulting enriched gene sets.  However, this is typically incomplete
  and biased towards the individual investigation goals. In this
  article, we present a curated compendium of 50 expression data sets
  investigating 34 different human diseases.  The compendium features
  microarray and RNA-seq measurements, and each data set is associated
  with a precompiled GO/KEGG relevance ranking for the corresponding
  disease under investigation. We perform a comprehensive assessment
  of 20 major enrichment methods based on the benchmark set, thereby
  identifying methods that accurately recover the a priori defined
  relevance rankings. The compendium is embedded in a directly
  executable benchmark system, the _R / Bioconductor_
  [GSEABenchmarkeR][] package, allowing straightforward execution on
  additional enrichment methods.

- Nima Hejazi\*, Alan Hubbard, Mark van der Laan. _Data-Adaptive
  Estimation and Inference for Differential Methylation Analysis_. DNA
  methylation is amongst the best studied of epigenetic mechanisms
  impacting gene expression. While much attention has been paid to the
  proper normalization of bioinformatical data produced by DNA
  methylation assays, linear models remain the current standard for
  analyzing post-processed methylation data, for the ease they afford
  for both statistical inference and scientific interpretation. We
  present a new, general statistical algorithm for the model-free
  estimation of the differential methylation of DNA CpG sites,
  complete with straightforward and interpretable statistical
  inference for such estimates. The new approach leverages variable
  importance measures, a class of parameters arising in causal
  inference, in a manner that facilitates their use in obtaining
  targeted estimates of the importance of each CpG site. The proposed
  procedure is computationally efficient and self-contained,
  incorporating techniques to isolate a subset of candidate CpG sites
  based on cursory evidence of differential methylation and providing
  a multiple testing correction that appropriately controls the False
  Discovery Rate in such multi-stage analysis settings. The
  effectiveness of the new methodology is demonstrated by way of data
  analysis with real DNA methylation data, and a recently developed R
  package (methyvim; available via Bioconductor) that provides support
  for data analysis with this methodology is introduced.

- Albert Y Zhang, Shian Su, Matthew E Ritchie, and Charity W
  Law\*. _Unpacking signal from RNA-seq intron reads using Rsubread and
  limma packages_. RNA-seq datasets contain up to millions of intron
  reads per library. These reads are typically removed from downstream
  analysis without even considering the proportion at which they
  contribute to total reads. By default only reads overlapping
  annotated exons are thought to be informative since mature mRNA is
  assumed to be the major component sequenced, especially when
  examining poly(A) RNA samples. Using Bioconductor packages, Rsubread
  and limma, we show that intron reads contain signal that is
  biologically relevant. Multi-dimensional scaling plots show that
  samples separate into biological and experimental groups using
  conservative intron counts, where the degree of separation is
  similar to that of exon counts despite there being far fewer intron
  reads in comparison to exon reads. The coverage of exon and intron
  regions are assessed for thousands of genes, showing a tendency for
  an increase in read coverage from 3' to 5' in poly(A) RNA
  samples. Coverage in Total RNA samples tend to be more uniform in
  appearance. We show that intron signal is prevalent across multiple
  datasets and discuss the possibility of its origin from pre-mRNA and
  intron retention. Results presented here can be used in the
  development of future Bioconductor packages to interrogate different
  biological aspects relating to intron signal, and inspire
  modifications to existing methods for RNA-seq analysis.

- Rachael V Phillips\*, Alan Hubbard. _Data Adaptive Evaluation of
  Preprocessing Methods using Ensemble Machine Learning_. For many
  types of biological data generated by high-throughput technologies,
  there is no single gold-standard for converting the raw data into a
  form that can be analyzed for relationships of the relevant
  biomarkers to exposures and disease. For example, much of the
  variation in the raw data generated by Illumina HumanMethylationEPIC
  and 450K arrays is due to the technicalities of the experimental
  design (comprising two different assay methods, two different color
  channels, and batch effects) and potentially less so due to the
  biological factor(s) of interest. Accordingly, several preprocessing
  methods have been developed, however it is unclear which combination
  should be retained in downstream analysis. To address this issue, we
  have developed a data adaptive methodology that incorporates
  ensemble machine learning to assess which preprocessing streams
  generate better signal-to-noise ratio, according to the prediction
  of positive and negative control variables. We employ this method to
  select normalizations for EPIC and 450K arrays in a principled
  way. The results suggest 1) differences in the relative performance
  of the possible preprocessing choices and 2) that such machine
  learning approaches can be practically applied to complex omics data
  to choose among the growing number of choices for preprocessing.

- Steinbaugh MJ\*, Kirchner RD, Ho Sui S. _bcbioSingleCell: R package
  for bcbio single-cell analysis_. Single-cell RNA sequencing
  (scRNA-seq) has ushered in a new era of genomics research, enabling
  researchers to visualize dynamic changes in cell populations, and
  quantify changes in gene expression at an unprecedented new level of
  resolution. While this new technology is extremely exciting and
  empowering, it remains overly challenging for the vast majority of
  biologists to import and analyze their results with confidence. The
  bcbio toolkit addresses this problem, offering native best-practice
  support for quantification of multiple barcoded droplet platforms,
  including inDrops, Drop-seq, 10X Genomics Chromium, and Illumina
  SureCell. The corresponding R package, _bcbioSingleCell_, provides
  support for easy loading of results into the SingleCellExperiment
  container class. Using the standardized SingleCellExperiment
  container enables researchers to efficiently pass their data to
  other single-cell packages available on Bioconductor. Additionally,
  the package offers a suite of quality control functions optimized
  for low quality cellular barcode removal, along with clustering and
  visualization functions that integrate with the Seurat
  toolkit. Differential expression analysis is supported and utilizes
  the zero-inflated negative binomial model provided by zinbwave, thus
  unlocking downstream testing with the robust DESeq2 or edgeR RNA-seq
  packages.

- Righelli D\*, Koberstein J, Gomes B, Zhang N, Angelini C, Peixoto L,
  Risso D. _Differential Enriched Scan 2 ([DEScan2][]): a fast
  pipeline for broad peak analysis_.  We present DEScan2 a novel
  bioconductor package for the analysis of Sono-Seq/Atac-Seq data,
  with the aim to facilitate the investigation of broad peak regions
  data.

  The method consists of three main steps: 1) a peak caller, 2) a peak
  filtering and 3) a method to efficiently compute a count matrix of
  the filtered peaks.

  The peak caller in step 1) is a standard moving window scan that
  compares the counts within a sliding window to the counts in a
  larger region outside the window, using a simple Poisson likelihood,
  providing a final z-score for each peak. However, the package can
  work with any external peak caller returning results in terms of bed
  files, indeed the package provides additional functionalities to
  load bed files of peaks and handle them as [GenomicRanges][]
  structures.

  The filtering step 2 is aimed to determine if a peak is a “true
  peak” on the basis of its replicability in other samples. Basing on
  this idea, we developed the filtering step to filter out those peaks
  not present in at least a user given number of samples. A further
  threshold can be used over the peak score.

  Finally, the third step produces a count matrix where each column is
  a sample and each row a filtered peak computed in the filtering
  step. The value of the matrix cell is the number of reads for the
  peak in the sample.

  Furthermore, our package provides several functionalities for
  [GenomicRanges][] data structure handling. One over the others gives
  the possibility to split a [GenomicRanges][] over the chromosomes to
  speed-up the computations parallelizing them over the chromosomes.

- Love MI\*, Hickey P, Soneson, C, and Patro R. _Automatic metadata
  propagation for RNA-seq_. tximeta performs numerous annotation and
  metadata gathering tasks on behalf of users during the import of
  transcript quantifications from Salmon into _R / Bioconductor_. The
  key idea within tximeta is to store a signature of the transcriptome
  sequence, computed and stored by the index and quant functions of
  Salmon. This signature acts as the identifying information for later
  building out rich annotations and metadata in the background, on
  behalf of the user. This should greatly facilitate genomic
  workflows, where the user can immediately begin overlapping their
  transcriptomic data with other genomic datasets, e.g. epigenetic
  tracks such as ChIP or methylation, as the data has been embedded
  within an organism and genome context, including the proper genome
  version. We seek to reduce wasted time of bioinformatic analysts,
  prevent costly bioinformatic mistakes, and promote computational
  reproducibility by avoiding situations of annotation and metadata
  ambiguity, when files are shared publicly or among collaborators but
  critical details go missing.

- Adithya M, Bhargava A, Wright E\*. _Improving the accuracy of
  taxonomic classification for identifying taxa in microbiome
  samples_. It has become increasingly clear that the microbiome is an
  essential component of human and ecosystem health. Microbiome
  studies frequently involve sequencing a taxonomic marker, such as
  the 16S rRNA or ITS, to identify the microorganisms that are present
  in a sample of interest. Here I will describe a new method, named
  IDTAXA, for taxonomic classification of marker gene sequences that
  exhibits a substantially lower error rate than previous
  approaches. In particular, IDTAXA avoids misclassifying sequences
  belonging to novel taxonomic groups that are not represented in
  existing taxonomic databases, which is the predominant type of error
  made by current classifiers. For example, the popular RDP Classifier
  incorrectly assigns 26.0% of novel 16S rRNA sequences to an existing
  taxonomic group when the organism actually belongs to a novel
  taxonomic group. In contrast, IDTAXA only incorrectly classifies
  13.6% of such sequences, while correspondingly improving on the
  fraction of sequences correctly classified to known taxonomic
  groups. This has a major impact on the interpretation of microbiome
  data because many microbial communities contain a large fraction of
  previously undescribed microorganisms that are not yet represented
  in taxonomic databases. Furthermore, we find that many taxonomic
  databases contain a considerable number of misclassified sequences
  that can corrupt the classification process. IDTAXA is able to
  automatically identify errors in the training taxonomy so that users
  are able to take corrective action. This enables us to
  systematically contrast existing taxonomic databases and make
  recommendations for their use. Collectively, these improvements
  often lead to substantially different classifications on real
  microbiome data, which may considerably alter its
  interpretation. IDTAXA is available as part of the [DECIPHER][]
  package in R (http://DECIPHER.codes).

- Innes BT\* and Bader GD. _scClustViz - Single-cell RNAseq Cluster
  Assessment and Interactive Visualisation_.  Single-cell RNA
  sequencing is becoming an increasingly popular technology, used both
  in large multi-centre projects, and for more directed biological
  experiments.  A common purpose for applying this technology is the
  in silico classification of cell types in a tissue.  This is
  generally done using one of a myriad of clustering algorithms, based
  on the assumption that cells within a cell type are share similar
  transcriptomes, which are distinct from other cell types in the
  tissue.  However, nearly all clustering algorithms have tunable
  parameters which affect, either directly or indirectly, the number
  of clusters they will return from the data.

  The R Shiny software tool outlined here provides a simple
  interactive interface for assessing the biological relevance of
  clustering results.  Given that cell types are expected to have
  distinct gene expression patterns, it uses differential gene
  expression between clusters as a metric for assessing overfitting of
  clustering (Yuzwa et al., Cell
  Reports 2017. DOI:10.1016/j.celrep.2017.12.017).  Along with this,
  it also provides interactive visualisation of: cluster-specific
  distributions of technical factors and other metadata; cluster-wise
  gene expression statistics to simplify annotation of cell types and
  identification of marker genes; and gene expression distributions
  over all cells.

  Interactive user interfaces for single-cell RNAseq analysis already
  exist, but this tool fills a distinct niche, as it is explicitly
  designed to assist in the biological interpretation of clustering
  solutions.  Since it is meant to be included in analysis workflows,
  it has intentionally been built to be easily customized by the
  bioinformatician, as well as used by the non-technical biologist.

  This tool provides an interactive interface for visualisation,
  assessment, and biological interpretation of cell-type
  classifications in single-cell RNAseq experiments that can be easily
  added to existing analysis pipelines, allowing non-technical
  biologists easier access to their data.

[DECIPHER]: https://bioconductor.org/packages/DECIPHER
[DEScan2]: https://bioconductor.org/packages/DEScan2
[DEsingle]: https://bioconductor.org/packages/DEsingle
[GSEABenchmarkeR]: https://bioconductor.org/packages/GSEABenchmarkeR
[GenomicRanges]: https://bioconductor.org/packages/GenomicRanges
[dplyr]: https://bioconductor.org/packages/dplyr
[gwasurvivr]: https://bioconductor.org/packages/gwasurvivr
[plyranges]: https://bioconductor.org/packages/plyranges
