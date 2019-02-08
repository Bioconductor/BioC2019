---
layout: default
speakers:
  - name: Jeffrey Leek
    inst: Johns Hopkins University
    url: http://jtleek.com/
    blurb: "Dr. Leek leads a group of researchers, educators, and data scientists using data to solve problems in molecular biology, human health, meta-research, education, and anything else they think could be useful for the world. They produce data tools and code that you can use for your projects as well."
  - name: Lieven Clement
    inst: Ghent University, Belgium.
    url: https://statomics.github.io/
    blurb: "The Clement group develops novel statistical methods and tools for the interpretation of omics data. Their research is structured according to three ‘omics domain: Meta-genomics, Transcriptomics (RNA-seq and single cell RNA-seq) and Proteomics (Identification and Differential Analysis in Mass Spectrometry based Quantitative Proteomics). They also leverage expertise in experimental design and data analysis for omics to researchers in the life sciences and have a keen interest in ‘omics data integration."
  - name: Lihua Julie Zhu
    inst: University of Massachusetts
    url: https://profiles.umassmed.edu/display/129880
    blurb: "Dr. Zhu is interested in the understanding of gene regulation and cancer etiology, biomarker discovery, and development and application of genome editing technology by mining and integrating various high-throughput datasets such as ChIP-seq, RNA-seq, ATAC-seq, miRNA-seq, Hi-C, shRNA-seq, PAS-seq, NAD-seq and GUIDE-seq. Her expertise is algorithm and computational tool development, and her group is an active contributor to the Bioconductor project. She has developed a dozen packages with various utilities, ranging from machine learning, peak calling, motif identification and alignment, quality assessment of ATACseq data, annotation, data integration, visualization, gRNA design and genome-wide offtargets identification in CRISPR genome editing studies."
  - name: Simina Boca
    inst: Georgetown University
    url: https://icbi.georgetown.edu/Boca
    blurb: "Dr. Boca analyzes omics data, including metabolomics and genomics, and considers their downstream application in precision medicine. In particular, she developed novel computational and statistical methods for high-dimensional data analysis, led the first comprehensive metabolomic study for Duchenne muscular dystrophy, and contributed to several of the early exome sequencing projects of human tumors. Additional areas of interest include cancer epidemiology and population genetics."
  - name: Anshul Kundaje
    inst: Stanford University
    url: https://profiles.stanford.edu/anshul-kundaje
    blurb: "Anshul Kundaje is an Assistant Professor of Genetics and Computer Science at Stanford University. His primary research area is large-scale computational regulatory genomics. The Kundaje lab specializes in developing statistical and machine learning methods for large-scale integrative analysis of heterogeneous, high-throughput functional genomic and genetic data to decipher regulatory elements and long-range regulatory interactions, learn predictive regulatory network models across individuals, cell-types and species and improve detection and interpretation of natural and disease-associated genetic variation."
  - name: Elli Papaemmanuil
    inst: Memorial Sloan Kettering Cancer Center
    url: https://www.mskcc.org/research-areas/labs/elli-papaemmanuil
    blurb: "The Papaemmanuil lab is a collective of clinical, computational, molecular and mathematic research investigators with an interest to study the role of acquired mutations in cancer development and how these determine clinical phenotype and response to therapy. Her mission is to execute research that informs and moves clinical practices in oncology forward."
---
# BioC 2019: Where Software and Biology Connect

When: June 24 - 27, 2019<br />
What: Developer Day, Main Conference, Symposium<br />
Where: [NYU and Rockefeller][venue], New York City, USA<br />
Slack: [Bioconductor Team][] (`#bioc2019` channel)<br />
Twitter: [#bioc2019][tweet]<br />

[tweet]: https://twitter.com/hashtag/bioc2019?f=tweets
[venue]: ./travel-accommodations
[Bioconductor Team]: https://bioc-community.herokuapp.com/

This conference highlights current developments within and beyond
_Bioconductor_. Morning scientific talks and afternoon workshops
provide conference participants with insights and tools required for
the analysis and comprehension of high-throughput genomic
data. 'Developer Day' precedes the main conference on June 24,
providing developers and would-be developers an opportunity to gain
insights into project direction and software development best
practices.

The conference will take place in two venues:
- Developer Day (June 24) at NYU Langone School of Medicine ([1st Avenue and East 30th Street](https://goo.gl/maps/WbtSVCpnrR92))
- Main Conference and Robert Gentleman Symposium (June 25-27) at Rockefeller University
([York Avenue and East 66th Street](https://goo.gl/maps/JkRcufXyhrq)).

## Confirmed Speakers
<!--
* [Jeffrey Leek](http://jtleek.com/)
* [Lieven Clement](https://statomics.github.io/)
* [Lihua Julie Zhu](https://profiles.umassmed.edu/display/129880)
* [Simina Boca](https://icbi.georgetown.edu/Boca)
* [Anshul Kundaje](https://profiles.stanford.edu/anshul-kundaje) -->

{% for s in page.speakers %}
{% assign imgpath = "images/speakers/" | append: s.name | remove: ' ' | append: '.jpg' %}
<img src="{{ imgpath }}" style="float:right; width:120px; height:150px; object-fit: cover">
### [{{ s.name }}]({{ s.url }}), {{ s.inst}}

> {{ s.blurb }}

{% endfor %}



More information: [workshop@bioconductor.org][contact]

<a href="https://twitter.com/intent/tweet?button_hashtag=bioc2019&ref_src=twsrc%5Etfw" class="twitter-hashtag-button" data-show-count="false">Tweet #bioc2019</a><script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

[contact]: mailto:workshop@bioconductor.org?subject=BioC2019%20question
