


# ProPublica’s COMPAS Data Revisited

This repository contains the *Rmarkdown* program that generates all the
Figures and Tables in my July 8, 2019, [arXiv
paper](https://arxiv.org/abs/1906.04711). In the paper, I examine
ProPublica’s COMPAS score and *two-year general* recidivism dataset. I
also include the actual full-length paper here as a *markdown* output
file (which allows one to view it as a webpage on GitHub). This
repository also contains several other related files. The files in this
repository are the
following:

[**Analysis\_ProPub\_COMPAS\_Revisited.Rmd**](https://github.com/mbarenstein/ProPublica_COMPAS_Data_Revisited/blob/master/Analysis_ProPub_COMPAS_Revisited.Rmd)

  - This file contains the **Rmarkdown program** that generates all the
    Figures and Tables (in HTML format) in my *arXiv* paper from July 8,
    2019.

[**Code\_to\_correct\_ProPub\_two\_year\_data.md**](https://github.com/mbarenstein/ProPublica_COMPAS_Data_Revisited/blob/master/Code_to_correct_ProPub_two_year_data.md)

  - This file contains the few lines of **R code** one can use to
    implement the simple April 1, 2014, COMPAS screening date *cutoff*
    rule I use in my paper to correct ProPublica’s two-year general
    recidivism dataset. (This code also appears in the *Rmarkdown*
    program listed above, which generates all the Figures and Tables in
    my
paper)

[**R\_session\_information.md**](https://github.com/mbarenstein/ProPublica_COMPAS_Data_Revisited/blob/master/R_session_information.md)

  - This file contains the R session information, including the R
    version (3.5.1) and R packages used to generate my
paper.

[**arXiv\_ProPub\_COMPAS\_Revisited.md**](https://github.com/mbarenstein/ProPublica_COMPAS_Data_Revisited/blob/master/arXiv_ProPub_COMPAS_Revisited.md)

  - This file contains the *markdown* output file that renders a
    (full-length) copy of **my arXiv paper**. This allows one to view
    the paper as a webpage on GitHub. Except for formatting differences
    and the correction of two typos regarding the writing (detailed
    below), this is identical to my July 8, 2019, arXiv
paper.

[**formatting\_GitHub\_vs\_arXiv**](https://github.com/mbarenstein/ProPublica_COMPAS_Data_Revisited/blob/master/formatting_GitHub_vs_arXiv.md)

  - Here, I list a few *formatting differences* between the GitHub
    markdown version of my July 8, 2019, arXiv paper in this repository
    and the PDF version on the arXiv
website.

[**minor\_clarifications.md**](https://github.com/mbarenstein/ProPublica_COMPAS_Data_Revisited/blob/master/minor_clarifications.md)

  - Here, I list a few *minor clarifications* regarding some of the
    writing in my arXiv paper (and the same copy of that paper in this
    repository).

(ProPublica’s own COMPAS GitHub repository is
[here](https://github.com/propublica/compas-analysis))

-----

### Summary of my [arXiv paper](https://arxiv.org/abs/1906.04711)

<!-- This is a shorter version of the abstract in the arXiv paper <https://arxiv.org/abs/1906.04711>. -->

I examine the **COMPAS recidivism risk score** and **criminal history**
data collected by **ProPublica** in 2016 that fueled intense debate and
research in the nascent field of *fair* machine learning or *algorithmic
fairness*. My paper takes a closer look at the actual datasets put
together by ProPublica. In particular, the **sub-datasets** built to
study the likelihood of **recidivism within two years** of a defendant’s
original COMPAS survey screening
date.<!-- (typically administered the same day or one day after the arrest) -->

I visualize these data by analyzing the distribution of defendants
across COMPAS screening dates. Doing so, **I find** that **ProPublica
made a substantial data processing error** when it created these
datasets, **failing to implement a two-year sample cutoff rule for
recidivists** in such datasets (whereas it implemented a two-year sample
cutoff rule for non-recidivists).

I show this data processing error in the Figure below, which is the key
Figure in my paper (**Figure
4**).

<img src="arXiv_ProPub_COMPAS_Revisited_files/figure-gfm/compas-screen-date-figures-by-recid-ProPub-2year-data-1.png" title="Figure 4: Persons by COMPAS Screen Date (7-day bins) by Recidivism Status - ProPublica Two-Year Dataset" alt="Figure 4: Persons by COMPAS Screen Date (7-day bins) by Recidivism Status - ProPublica Two-Year Dataset" style="display: block; margin: auto;" />

*\[Note: There is also a visible drop in COMPAS screens or cases during
two months in mid-2013 (for recidivists and non-recidivists alike). This
is a separate issue, however, which seems to be present in the original
dataset that ProPublica received from Broward County, FL. So this
particular issue does not appear to be a data processing mistake by
ProPublica, and I do not address this in my paper\]*

As I show in my paper, the data processing mistake I identify **leads to
recidivism rates that are biased upward by over 24%**. It also affects
the positive and negative predictive values. On the other hand, the data
processing error has little impact on some of the other key statistical
measures, which are less susceptible to changes in the relative share of
recidivists, such as the false positive and false negative rates, and
the overall accuracy.

-----

**Matias Barenstein**

First version of my paper on arXiv: **June 11**, 2019. E-mail:
<mbarenstein@gmail.com>. The author is a staff economist at the Federal
Trade Commission (FTC). This study was conducted independently of his
work at the FTC. The views expressed in this article are those of the
author. They do not necessarily represent those of the Federal Trade
Commission or any of its Commissioners.

**Bibtex citation**:

``` 
    @ARTICLE{2019arXiv190604711B,
       author = {{Barenstein}, Matias},
        title = "{ProPublica's COMPAS Data Revisited}",
      journal = {arXiv e-prints},
         year = "2019",
        month = "Jun",
          eid = {arXiv:1906.04711},
        pages = {arXiv:1906.04711},
archivePrefix = {arXiv},
       eprint = {1906.04711},
 primaryClass = {econ.GN},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2019arXiv190604711B},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
      }
```

**Keywords:** Fair Machine Learning, Algorithmic Fairness, Recidivism,
Risk, Bias, COMPAS, ProPublica
