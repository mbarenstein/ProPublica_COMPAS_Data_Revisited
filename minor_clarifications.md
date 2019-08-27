Minor Clarifications
================



<!-- author: "Matias Barenstein" -->

<!-- date: "August 26, 2019" -->

Here I list a few *minor* clarifications regarding some of the writing
in my arXiv paper and the copy of that paper in this GitHub repository.
(I do write some of these clarifications in two more recent *Towards
Data Science* blog posts,
[here](https://towardsdatascience.com/the-data-processing-error-in-the-most-prominent-fair-machine-learning-dataset-short-version-d27d8d390fea)
and
[here](https://towardsdatascience.com/the-data-processing-error-in-one-of-the-most-prominent-fair-machine-learning-datasets-4fa205daa3c4?source=friends_link&sk=258477f738e83d46808bc9bb9d34591b),
where I write two summarized versions of my paper)

**i.** In the *Abstract, Introduction*, and *Conclusion*, I wrote:

> “I take a new yet simple approach to visualize these data…”

   I do a basic histogram. My approach is *new* only in the sense that I
seem to be the first to *visualize* the  
   COMPAS screening dates in ProPublica’s two-year recidivism
sub-dataset(s).

**ii.** In the *Introduction* I wrote:

> “Doing so, I find that ProPublica made an important data processing
> error creating some of the key datasets most often used by other
> researchers.”

   For clarity, I should have emphasized that these are the ***two-year
recidivism sub***-datasets.

**iii.** In section 3, *ProPublica’s Data Processing Mistake*, I should
have added the following text for clarity:

  "Presumably, ProPublica realized that it was not necessary to observe
recidivists for a full two-years *outside*  
   jail and prison. Given that they recidivated and could be put in
prison for a non-trivial amount of time for  
   their re-offense after their original COMPAS screen date. And one
would still clearly want to include such  
   people in the data."

  "While it is logical not to implement a requirement that recidivists
must be observed *outside* jail or prison  
   for two years, **one should still apply** a COMPAS screen date sample
cutoff on or before April 1, 2014, for them.  
   (But ProPublica failed to do so)"

**iv.** In the last paragraph of the *Conclusion*, for clarity, perhaps
I should have added:

  "Many potential measurement issues may affect the estimated recidivism
rate in ProPublica’s COMPAS data (as I  
   mention in the Appendix). Some of these could be putting downward
pressure on the estimate, perhaps offsetting  
   to some degree the upward bias I identify here. Nevertheless, this
does not invalidate the emphasis on the data  
   processing issue I identify and the ensuing data correction I call
for. My focus is on the *internal* validity  
   of the data processing. I am not claiming that after this correction,
the data will not have any remaining  
   issues, nor necessarily that it will have *external* validity, which
is beyond the scope of my paper."

Matias Barenstein
