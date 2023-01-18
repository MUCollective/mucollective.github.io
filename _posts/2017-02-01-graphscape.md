---
layout: paper
category: paper automation
title:  "GraphScape: A Model for Automated Reasoning about Visualization Similarity and Sequencing"
authors: "Younghoon Kim, Kanit Wongsuphasawat, Jessica Hullman, Jeffrey Heer"
venue: "ACM Human Factors in Computing Systems (CHI) 2017"
thumb: "assets/images/paper-thumb-graphscape.png"
banner: "assets/images/paper-banner-graphscape.png"
caption: "A GraphScape model. Nodes represent Vega-Lite chart specifications, edges represent edit modifications between charts. Edge weights encode estimated transition costs between charts."
pdf: "assets/papers/2017-graphscape.pdf"
honorable: true
github: "https://github.com/uwdata/graphscape"
---

<!-- abstract -->
We present GraphScape, a directed graph model of the visualization design space that supports automated reasoning about visualization similarity and sequencing. Graph nodes represent grammar-based chart specifications and edges represent edits that transform one chart to another. We weight edges with an estimated cost of the difficulty of interpreting a target visualization given a source visualization. We contribute (1) a method for deriving transition costs via a partial ordering of edit operations and the solution of a resulting linear program, and (2) a global weighting term that rewards consistency across transition subsequences. In a controlled experiment, subjects rated visualization sequences covering a taxonomy of common transition types. In all but one case, GraphScape’s highest-ranked suggestion aligns with subjects’ top-rated sequences. Finally, we demonstrate applications of GraphScape to automatically sequence visualization presentations, elaborate transition paths between visualizations, and recommend design alternatives (e.g., to improve scalability while minimizing design changes).


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@inproceedings{graphscape-2017,
	title        = {GraphScape: A Model for Automated Reasoning about Visualization Similarity and Sequencing},
	author       = {Kim, Younghoon and Wongsuphasawat, Kanit and Hullman, Jessica and Heer, Jeffrey},
	year         = 2017,
	booktitle    = {Proceedings of the 2017 CHI Conference on Human Factors in Computing Systems},
	publisher    = {ACM},
	series       = {CHI '17},
	pages        = {2628–2638},
	doi          = {10.1145/3025453.3025866}
}
</pre>
</div>