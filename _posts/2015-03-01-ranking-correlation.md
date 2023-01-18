---
layout: paper
category: paper
title:  "Beyond Weber’s Law: A Second Look at Ranking Visualizations of Correlation"
authors: "Matthew Kay, Jeffery Heer"
venue: "IEEE Trans. Visualization & Comp. Graphics (Proc. INFOVIS) 2015"
thumb: "assets/images/paper-thumb-ranking-correlation.png"
banner: "assets/images/paper-banner-ranking-correlation.png"
caption: ""
pdf: "assets/papers/2015-ranking-correlation.pdf"
honorable: true
github: "https://github.com/mjskay/ranking-correlation"
---

<!-- abstract -->
Models of human perception – including perceptual “laws” – can be valuable tools for deriving visualization design recommendations. However, it is important to assess the explanatory power of such models when using them to inform design. We present a secondary analysis of data previously used to rank the effectiveness of bivariate visualizations for assessing correlation (measured with Pearson’s r) according to the well-known Weber-Fechner Law. Beginning with the model of Harrison et al. [1], we present a sequence of refinements including incorporation of individual differences, log transformation, censored regression, and adoption of Bayesian statistics. Our model incorporates all observations dropped from the original analysis, including data near ceilings caused by the data collection process and entire visualizations dropped due to large numbers of observations worse than chance. This model deviates from Weber’s Law, but provides improved predictive accuracy and generalization. Using Bayesian credibility intervals, we derive a partial ranking that groups visualizations with similar performance, and we give precise estimates of the difference in performance between these groups. We find that compared to other visualizations, scatterplots are unique in combining low variance between individuals and high precision on both positively- and negatively- correlated data. We conclude with a discussion of the value of data sharing and replication, and share implications for modeling similar experimental data.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{ranking-correlation-2016,
	title        = {Beyond Weber's Law: A Second Look at Ranking Visualizations of Correlation},
	author       = {Kay, Matthew and Heer, Jeffrey},
	year         = 2016,
	journal      = {IEEE Transactions on Visualization and Computer Graphics},
	volume       = 22,
	number       = 1,
	pages        = {469--478},
	doi          = {10.1109/TVCG.2015.2467671}
}
</pre>
</div>