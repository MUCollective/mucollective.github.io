---
layout: paper
category: paper automation
title:  "Keeping Multiple Views Consistent: Constraints, Validations, and Exceptions in Visualization Authoring"
authors: "Zening Qu, Jessica Hullman"
venue: "IEEE Trans. Visualization & Comp. Graphics (Proc. INFOVIS) 2017"
thumb: "assets/images/paper-thumb-consistency.png"
banner: "assets/images/paper-banner-consistency.png"
caption: "Visualizations that contain multiple views have multiple scales (e.g., xy scales, color scales). We develop and study authors' reactions to a model that formalizes visual encoding consistency between scale pairs as the above constraints. C1.1, C1.2, C2.1, and C2.2 require a pair of quantitative or nominal fields to be encoded using the same or different xy scales across two views depending on whether the fields are the same or different. Applying a similar logic to color, C1.3 and C1.4 require the same quantitative and nominal fields to have the same color scales. C2.3 requires different quantitative fields to have different hues, while C2.4 requires palettes of different nominal fields to not overlap. C2.5 requires nominal palettes to not include constant colors of other views."
pdf: "assets/papers/2017-consistency.pdf"
honorable: true
---

<!-- abstract -->
Visualizations often appear in multiples, either in a single display (e.g., small multiples, dashboard) or across time or space (e.g., slideshow, set of dashboards). However, existing visualization design guidelines typically focus on single rather than multiple views. Solely following these guidelines can lead to effective yet inconsistent views (e.g., the same field has different axes domains across charts), making interpretation slow and error-prone. Moreover, little is known how consistency balances with other design considerations, making it difficult to incorporate consistency mechanisms in visualization authoring software. We present a wizard-of-oz study in which we observed how Tableau users achieve and sacrifice consistency in an exploration-to-presentation visualization design scenario. We extend (from our prior work) a set of encoding-specific constraints defining consistency across multiple views. Using the constraints as a checklist in our study, we observed cases where participants spontaneously maintained consistent encodings and warned cases where consistency was overlooked. In response to the warnings, participants either revised views for consistency or stated why they thought consistency should be overwritten. We categorize participants’ actions and responses as constraint validations and exceptions, depicting the relative importance of consistency and other design considerations under various circumstances (e.g., data cardinality, available encoding resources, chart layout). We discuss automatic consistency checking as a constraint-satisfaction problem and provide design implications for communicating inconsistencies to users.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{consistency-2017,
	title        = {Keeping Multiple Views Consistent: Constraints, Validations, and Exceptions in Visualization Authoring},
	author       = {Qu, Zening and Hullman, Jessica},
	year         = 2018,
	journal      = {IEEE Transactions on Visualization and Computer Graphics},
	volume       = 24,
	number       = 1,
	pages        = {468--477},
	doi          = {10.1109/TVCG.2017.2744198}
}
</pre>
</div>