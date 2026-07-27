---
title: "Designing Catalysts by Evolution: Searching 1.7 Billion Molecules Without Calculating Them All"
date: 2026-02-05
categories:
  - Research
tags:
  - Catalysis
  - Inverse Design
  - Machine Learning
  - Frustrated Lewis Pairs
  - CO2 Hydrogenation
excerpt: >
  Can computers design catalysts instead of simply screening them?
  We developed an inverse-design workflow combining quantum chemistry,
  machine learning, and genetic algorithms to discover new frustrated
  Lewis pair catalysts for CO₂ hydrogenation.
header:
  teaser: /assets/images/blog/flp-ga/cover.jpg
layout: single
---

Finding a good catalyst is a bit like looking for a needle in a haystack.

Chemists can often imagine thousands—or even billions—of possible molecular structures that might catalyze a reaction, but experimentally testing every candidate is simply impossible. Instead, quantum mechanical calculations allow us to evaluate catalysts in silico before investing in expensive experiments. Because catalysis is ultimately about breaking and forming chemical bonds, there is no shortcut around quantum mechanics. Yet when the search space contains billions of possible molecules, even computational screening becomes computationally intractable. This raises a fundamental question:

> **How can we search an enormous chemical space without exhaustively computing every molecule?**

In our recent work, published in *Chemical Science*, we tackled this challenge for **frustrated Lewis pair (FLP)** catalysts that convert carbon dioxide into formate—a reaction relevant to carbon capture and utilization.

---

## Why FLPs are worth discovering and why is it challenging?

Frustrated Lewis pairs (FLPs) are combinations of a Lewis acid and a Lewis base in close physical proximity. At first glance, a Lewis acid and a Lewis base should simply react with each other and call it a day. In an FLP, however, bulky substituents or clever molecular design prevent this from happening. The two reactive centers remain close enough to cooperate, but not close enough to quench each other. This "frustration" gives rise to remarkable catalytic properties, including the ability to perform catalysis without the need for transition metals. These cooperative mechanism a both a triumph and a chellenge for their discovery - the two centers must have the right balance of acidity and basicity while being held at just the right distance and orientation. This intricate interplay makes discovering new FLP catalysts considerably more challenging than optimizing conventional single-site catalysts. 

---

## Why conventional screening reaches its limits

Our previous work established quantitative design rules for highly active FLPs based on two simple ingredients:

- the chemical strength of the Lewis acid and base,
- and their relative geometry.

Those principles enabled high-throughput virtual screening of around **25,000** candidates. While successful, this strategy also had an important limitation: candidates that failed one design criterion early in the workflow were discarded, even if they might have been excellent overall catalysts.

---

## Let evolution search for the catalyst

Instead of asking

> *Which catalyst should we calculate next?*

we asked a different question:

> **Can a computer evolve better catalysts automatically?**

To do this, we developed an inverse-design workflow based on a **genetic algorithm**.

Every catalyst is treated as a combination of molecular building blocks—rather like genes in biology. The best-performing catalysts survive, exchange fragments, mutate into new structures, and gradually evolve over successive generations.

Unlike many AI approaches that generate arbitrary molecules, our method assembles catalysts only from chemically meaningful fragments reported in the literature, increasing the likelihood that the proposed molecules are synthetically realistic.

---

## A catalyst is more than activity

A highly active catalyst is useless if it cannot be synthesized or if it immediately deactivates.

For that reason, our algorithm simultaneously optimizes four competing objectives:

- catalytic activity,
- active-site geometry,
- synthetic complexity,
- resistance to catalyst quenching.

Rather than maximizing only one property, the algorithm searches for balanced solutions that satisfy all of these requirements simultaneously.

---

## Searching 1.7 billion possibilities

The chemical space contained approximately **1.7 billion** possible FLP catalysts.

Remarkably, the genetic algorithm needed to evaluate only a tiny fraction of this space before converging on promising candidates. Along the way, it rediscovered known chemical motifs while also identifying entirely new catalyst architectures that conventional screening had missed.

---

## Challenging our own design rules

Perhaps the most interesting outcome was that the algorithm challenged one of our previous assumptions.

Earlier screening suggested that **geminal FLPs** were generally poor catalysts because of their unfavorable geometry. The genetic algorithm revealed that this conclusion was not universally true. By embedding these active sites into rigid molecular frameworks, their geometry could be transformed into highly favorable arrangements for catalysis.

In other words, the algorithm didn't just find better molecules—it improved our understanding of what makes a catalyst work.

---

## Looking ahead

Although this study focused on CO₂ hydrogenation, the framework itself is far more general.

Any catalytic problem that can be expressed in terms of computable molecular properties could, in principle, be explored using the same evolutionary strategy. Rather than replacing quantum chemistry, machine learning, or chemical intuition, inverse design combines all three into a practical workflow for discovering new catalysts.

---

## Read the paper

**Das, S., Laplaza, R., Worakula, T., & Corminboeuf, C.**

*Inverse design of frustrated Lewis pairs for direct catalytic CO₂ hydrogenation: refining and expanding design rules.*

**Chemical Science**, 2026.

**DOI:** https://doi.org/10.1039/D5SC09530A

---

*If you are interested in inverse design, computational catalysis, or machine learning for molecular discovery, feel free to get in touch. I am always happy to discuss ideas and potential collaborations.*
