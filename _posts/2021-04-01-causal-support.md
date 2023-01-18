---
layout: paper
category: paper
title:  "Causal Support: Modeling Causal Inferences with Visualizations"
authors: "Alex Kale, Yifan Wu, Jessica Hullman"
venue: "IEEE Trans. Visualization & Comp. Graphics (Proc. INFOVIS) 2021"
thumb: "assets/images/paper-thumb-causal-support.png"
banner: "assets/images/paper-banner-causal-support.png"
caption: "Modeling causal inferences with visualizations: (A) Users view and may interact with data visualizations; (B) Ideally, users reason through a series of comparisons that allow them to allocate subjective probabilities to possible data generating processes; and (C) We elicit users’ subjective probabilities as a Dirichlet distribution across possible causal explanations and compare these causal inferences to a computed benchmark of causal support, which we derive from Bayesian inference across possible causal models."
pdf: "assets/papers/2021-causal-support.pdf"
supplementary: "https://osf.io/zbu5e/"
github: "https://github.com/kalealex/causal-support"
---

<!-- abstract -->
Analysts often make visual causal inferences about possible data-generating models. However, visual analytics (VA) software tends to leave these models implicit in the mind of the analyst, which casts doubt on the statistical validity of informal visual “insights”. We formally evaluate the quality of causal inferences from visualizations by adopting causal support—a Bayesian cognition model that learns the probability of alternative causal explanations given some data—as a normative benchmark for causal inferences. We contribute two experiments assessing how well crowdworkers can detect (1) a treatment effect and (2) a confounding relationship. We find that chart users’ causal inferences tend to be insensitive to sample size such that they deviate from our normative benchmark. While interactively cross-filtering data in visualizations can improve sensitivity, on average users do not perform reliably better with common visualizations than they do with textual contingency tables. These experiments demonstrate the utility of causal support as an evaluation framework for inferences in VA and point to opportunities to make analysts’ mental models more explicit in VA software.


<h3><svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-bookmark" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z"/>
</svg> Citation</h3>
<div class="bibtex">
<!-- bibtex -->
<h4>BibTeX</h4>
<pre>
@article{causal-support-2022,
	title        = {Causal Support: Modeling Causal Inferences with Visualizations},
	author       = {Kale, Alex and Wu, Yifan and Hullman, Jessica},
	year         = 2022,
	journal      = {IEEE Transactions on Visualization and Computer Graphics},
	volume       = 28,
	number       = 1,
	pages        = {1150--1160},
	doi          = {10.1109/TVCG.2021.3114824}
}
</pre>
</div>