---
layout: paper
category: paper
title:  "Revealing Perceptual Proxies with Adversarial Examples"
authors: "Brian D. Ondov, Fumeng Yang, Matthew Kay, Niklas Elmqvist, Steven Franconeri"
venue: "IEEE Trans. Visualization & Comp. Graphics (Proc. INFOVIS) 2020"
thumb: "assets/images/paper-thumb-perceptual-proxies.png"
banner: "assets/images/paper-banner-perceptual-proxies.png"
caption: "A “theory-driven” approach (A) and a “data-driven” approach (B) for uncovering how the visual system extracts statistics from a visualization, by pitting correct answers against adversarial models of candidate perceptual proxies"
pdf: "assets/papers/2020-perceptual-proxies.pdf"
---

<!-- abstract -->
Data visualizations convert numbers into visual marks so that our visual system can extract data from an image instead of raw numbers. Clearly, the visual system does not compute these values as a computer would, as an arithmetic mean or a correlation. Instead, it extracts these patterns using perceptual proxies; heuristic shortcuts of the visual marks, such as a center of mass or a shape envelope. Understanding which proxies people use would lead to more effective visualizations. We present the results of a series of crowdsourced experiments that measure how powerfully a set of candidate proxies can explain human performance when comparing the mean and range of pairs of data series presented as bar charts. We generated datasets where the correct answer-the series with the larger arithmetic mean or range-was pitted against an “adversarial” series that should be seen as larger if the viewer uses a particular candidate proxy. We used both Bayesian logistic regression models and a robust Bayesian mixed-effects linear model to measure how strongly each adversarial proxy could drive viewers to answer incorrectly and whether different individuals may use different proxies. Finally, we attempt to construct adversarial datasets from scratch, using an iterative crowdsourcing procedure to perform black-box optimization.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{perceptual-proxies-2020,
	title        = {Revealing Perceptual Proxies with Adversarial Examples},
	author       = {Ondov, Brian D. and Yang, Fumeng and Kay, Matthew and Elmqvist, Niklas and Franconeri, Steven},
	year         = 2021,
	journal      = {IEEE Transactions on Visualization and Computer Graphics},
	volume       = 27,
	number       = 2,
	pages        = {1073--1083},
	doi          = {10.1109/TVCG.2020.3030429}
}
</pre>
</div>