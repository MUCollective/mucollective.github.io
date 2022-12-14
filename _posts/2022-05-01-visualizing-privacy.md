---
layout: paper
category: paper
title:  "Visualizing Privacy-Utility Trade-Offs in Differentially Private Data Releases"
authors: "Priyanka Nanayakkara, Johes Bater, Xi He, Jessica Hullman, and Jennie Rogers"
venue: "Proceedings on Privacy Enhancing Technologies 2022"
thumb: "assets/images/paper-thumb-visualizing-privacy.gif"
banner: "assets/images/paper-banner-visualizing-privacy.png"
caption: "Differentially private mechanisms can be used to calculate statistics in a way that preserves the privacy of those whose information is represented in the dataset. Using these mechanisms, however, requires setting privacy budgets, a task for which there is little to no formal guidance. We introduce an interactive visualization interface, Visualizing Privacy (ViP), which is designed to assist a practitioner in considering multiple probabilistic trade-offs to set context-appropriate privacy budgets both for privacy-preserving point estimates and privacy-preserving confidence intervals."
pdf: "assets/papers/2022-visualizing-privacy.pdf"
---

<!-- abstract -->
Organizations often collect private data and release aggregate statistics for the public’s benefit. If no steps toward preserving privacy are taken, adversaries may use released statistics to deduce unauthorized information about the individuals described in the private dataset. Differentially private algorithms address this challenge by slightly perturbing underlying statistics with noise, thereby mathematically limiting the amount of information that may be deduced from each data release. Properly calibrating these algorithms— and in turn the disclosure risk for people described in the dataset—requires a data curator to choose a value for a privacy budget parameter, ϵ. However, there is little formal guidance for choosing ϵ, a task that requires reasoning about the probabilistic privacy–utility tradeoff. Furthermore, choosing ϵ in the context of statistical inference requires reasoning about accuracy trade-offs in the presence of both measurement error and differential privacy (DP) noise.

We present <strong>Vi</strong>sualizing <strong>P</strong>rivacy (ViP), an interactive interface that visualizes relationships between ϵ, accuracy, and disclosure risk to support setting and splitting&nbsp;ϵ among queries. As a user adjusts ϵ, ViP dynamically updates visualizations depicting expected accuracy and risk. ViP also has an inference setting, allowing a user to reason about the impact of DP noise on statistical inferences. Finally, we present results of a study where 16 research practitioners with little to no DP background completed a set of tasks related to setting ϵ using both ViP and a control. We find that ViP helps participants more correctly answer questions related to judging the probability of where a DP-noised release is likely to fall and comparing between DP-noised and non-private confidence intervals.
