---
layout: paper
category: paper
title:  "Evaluating Visualization Sets: Trade-offs Between Local Effectiveness and Global Consistency"
authors: "Zening Qu, Jessica Hullman"
venue: "BELIV 2016"
thumb: "assets/images/paper-thumb-tradeoff-consistency.png"
banner: "assets/images/paper-banner-tradeoff-consistency.png"
caption: "Two maps show different UK healthcare group locations. The same colors represent different data in the two views, requiring viewers to maintain several meanings for each color value in memory as they analyze the set."
pdf: "assets/papers/2016-tradeoff-consistency.pdf"
---

<!-- abstract -->
Evaluation criteria like expressiveness and effectiveness favor optimal use of space and visual encoding channels in a single visualization. However, individually optimized views may be inconsistent with one another when presented as a set in recommender systems and narrative visualizations. For example, two visualizations might use very similar color palettes for different data fields, or they might render the same field but in different scales. These inconsistencies in visualization sets can cause interpretation errors and increase the cognitive load on viewers trying to analyze a set of visualizations. We propose two high-level principles for evaluating visualization set consistency: (1) the same fields should be presented in the same way, (2) different fields should be presented differently. These two principles are operationalized as a set of constraints for common visual encoding channels (x, y, color, size, and shape) to enable automated visualization set evaluation. To balance global (visualization set) consistency and local (single visualization) effectiveness, trade-offs in space and visual encodings have to be made. We devise an effectiveness preservation score to guide the selection of which conflicts to surface and potentially revise for sets of quantitative and ordinal encodings and a palette resource allocation mechanism for nominal encodings.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@inproceedings{tradeoff-consistency-2016,
	title        = {Evaluating Visualization Sets: Trade-Offs Between Local Effectiveness and Global Consistency},
	author       = {Qu, Zening and Hullman, Jessica},
	year         = 2016,
	booktitle    = {Proceedings of the Sixth Workshop on Beyond Time and Errors on Novel Evaluation Methods for Visualization},
	publisher    = {ACM},
	series       = {BELIV '16},
	pages        = {44–52},
	doi          = {10.1145/2993901.2993910}
}
</pre>
</div>