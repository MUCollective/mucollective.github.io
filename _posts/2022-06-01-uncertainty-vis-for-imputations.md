---
layout: paper
category: paper
title:  "Evaluating the Use of Uncertainty Visualisations forImputations of Data Missing At Random in Scatterplots"
authors: "Abhraneel Sarma, Shunan Guo, Jane Hoffswell, Ryan Rossi, Fan Du, Eunyee Koh, and Matthew Kay"
venue: "IEEE Trans. Visualization & Comp. Graphics (Proc. INFOVIS) 2022"
thumb: "assets/images/paper-thumb-uncertainty-vis-for-imputations.png"
banner: "assets/images/paper-banner-uncertainty-vis-for-imputations.png"
caption: "Datasets often have missing values (A). Not accounting for missing values in data can often lead to incorrect conclusions when performing common visualisation tasks such as mean or trend estimation (B). We can use various statistical methods to impute estimates for the missing values in the data, which may provide the necessary information required for correct inference (C). We use six different visual representations to present imputation and associated uncertainty information in charts (D), and measure how analysts may perform in mean or trend estimation tasks (E)"
pdf: "assets/papers/2022-uncertainty-vis-for-imputations.pdf"
supplementary: "https://osf.io/q4y5r/"
---

<!-- abstract -->
Most real-world datasets contain missing values yet most exploratory data analysis (EDA) systems only support visualising data points with complete cases. This omission may potentially lead the user to biased analyses and insights. Imputation techniques can help estimate the value of a missing data point, but introduces additional uncertainty. In this work, we investigate the effects of visualising imputed values in charts using different ways of representing data imputations and imputation uncertainty—no imputation, mean,95% confidence intervals, probability density plots, gradient intervals, and hypothetical outcome plots. We focus on scatterplots, which is a commonly used chart type, and conduct a crowdsourced study with 202 participants. We measure users’ bias and precision in performing two tasks—estimating average and detecting trend—and their self-reported confidence in performing these tasks. Our results suggest that, when estimating averages, uncertainty representations may reduce bias but at the cost of decreasing precision.When estimating trend, only hypothetical outcome plots may lead to a small probability of reducing bias while increasing precision.Participants in every uncertainty representation were less certain about their response when compared to the baseline. The findings point towards potential trade-offs in using uncertainty encodings for datasets with a large number of missing values. This paper and the associated analysis materials are available at: [https://osf.io/q4y5r/](https://osf.io/q4y5r/)

<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{uncertainty-vis-for-imputations-2022,
	title        = {Evaluating the Use of Uncertainty Visualisations for Imputations of Data Missing At Random in Scatterplots},
	author       = {Sarma, Abhraneel and Guo, Shunan and Hoffswell, Jane and Rossi, Ryan and Du, Fan and Koh, Eunyee and Kay, Matthew},
	year         = 2023,
	journal      = {IEEE Transactions on Visualization and Computer Graphics},
	volume       = 29,
	number       = 1,
	pages        = {602--612},
	doi          = {10.1109/TVCG.2022.3209348}
}
</pre>
</div>