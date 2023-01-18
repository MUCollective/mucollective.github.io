---
layout: paper
category: paper responsive-visualization
title:  "An Automated Approach to Reasoning About Task-Oriented Insights in Responsive Visualization"
authors: "Hyeok Kim, Ryan Rossi, Abhraneel Sarma, Dominik Moritz, and Jessica Hullman"
venue: "IEEE Trans. Visualization & Comp. Graphics (Proc. INFOVIS) 2021"
thumb: "assets/images/paper-thumb-responsive-vis-insight-preservation.png"
banner: "assets/images/paper-banner-responsive-vis-insight-preservation.png"
caption: "Changes to task-oriented insights under responsive visualization design transformation in terms of identification, comparison, and trend tasks"
pdf: "assets/papers/2021-responsive-vis-insight-preservation.pdf"
supplementary: "https://osf.io/jcvbx/"
---

<!-- abstract -->
Authors often transform a large screen visualization for smaller displays through rescaling, aggregation and other techniques when creating visualizations for both desktop and mobile devices (i.e., responsive visualization). However, transformations can alter relationships or patterns implied by the large screen view, requiring authors to reason carefully about what information to preserve while adjusting their design for the smaller display. We propose an automated approach to approximating the loss of support for task-oriented visualization insights (identification, comparison, and trend) in responsive transformation of a source visualization. We operationalize identification, comparison, and trend loss as objective functions calculated by comparing properties of the rendered source visualization to each realized target (small screen) visualization. To evaluate the utility of our approach, we train machine learning models on human ranked small screen alternative visualizations across a set of source visualizations. We find that our approach achieves an accuracy of 84% (random forest model) in ranking visualizations. We demonstrate this approach in a prototype responsive visualization recommender that enumerates responsive transformations using Answer Set Programming and evaluates the preservation of task-oriented insights using our loss measures. We discuss implications of our approach for the development of automated and semi-automated responsive visualization recommendation.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{responsive-vis-insight-preservation-2021,
	title        = {An Automated Approach to Reasoning About Task-Oriented Insights in Responsive Visualization},
	author       = {Kim, Hyeok and Rossi, Ryan and Sarma, Abhraneel and Moritz, Dominik and Hullman, Jessica},
	year         = 2022,
	journal      = {IEEE Transactions on Visualization and Computer Graphics},
	volume       = 28,
	number       = 1,
	pages        = {129--139},
	doi          = {10.1109/TVCG.2021.3114782}
}
</pre>
</div>