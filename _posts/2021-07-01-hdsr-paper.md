---
layout: paper
category: paper
title:  "Designing for interactive exploratory data analysis requires theories of graphical inference"
authors: "Jessica Hullman and Andrew Gelman"
venue: "Harvard Data Science Review 2021"
thumb: "assets/images/paper-thumb-hdsr-paper.png"
banner: "assets/images/paper-banner-hdsr-paper.png"
caption: "Plots of real estate data from Ames, Iowa (De Cock, 2011), created in Tableau Software (Tableau Software, 2021c). (a) Trellis plot of housing sale prices by neighborhood might invoke comparisons to a normal or log-normal distribution, and enables a visual check for a main effect of neighborhood. (b) Scatterplot of housing sale prices by square feet of above ground living area, with number of bedrooms above ground mapped to sequential color might invoke comparisons to a diagonal line representing a perfect positive correlation. (c) Residuals from multiple linear regression of sale price by above ground living area and bedrooms implied in plot b. (d) Trellis plot of sale price by lot configuration and neighborhood enables, among other effects, a visual check for an interaction between lot configuration and neighborhood."
pdf: "assets/papers/2021-hdsr-paper.pdf"
additionals:
  - link: "https://hdsr.mitpress.mit.edu/pub/w075glo6/release/2?readingCollection=c6a3a10e"
    name: "Open Access"
---

<!-- abstract -->
Research and development in computer science and statistics have produced increasingly sophisticated software interfaces for interactive and exploratory analysis, optimized for easy pattern finding and data exposure. But design philosophies that emphasize exploration over other phases of analysis risk confusing a need for flexibility with a conclusion that exploratory visual analysis is inherently “model free” and cannot be formalized. We describe how without a grounding in theories of human statistical inference, research in exploratory visual analysis can lead to contradictory interface objectives and representations of uncertainty that can discourage users from drawing valid inferences. We discuss how the concept of a model check in a Bayesian statistical framework unites exploratory and confirmatory analysis, and how this understanding relates to other proposed theories of graphical inference. Viewing interactive analysis as driven by model checks suggests new directions for software and empirical research around exploratory and visual analysis. For example, systems might enable specifying and explicitly comparing data to null and other reference distributions and better representations of uncertainty. Implications of Bayesian and other theories of graphical inference can be tested against outcomes of interactive analysis by people to drive theory development.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{hdsr-paper-2021,
	title        = {Designing for {Interactive} {Exploratory} {Data} {Analysis} {Requires} {Theories} of {Graphical} {Inference}},
	author       = {Hullman, Jessica and Gelman, Andrew},
	year         = 2021,
	journal      = {Harvard Data Science Review},
	doi          = {10.1162/99608f92.3ab8a587}
}
</pre>
</div>