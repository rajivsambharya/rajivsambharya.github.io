---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<style>
a:link {
  color: #008CBA;
  background-color: white;
  text-decoration: none;
}
a:visited {
  color: #008CBA;
  background-color: white;
  text-decoration: none;
}
a:hover {
  color: #008CBA;
  background-color: white;
  text-decoration: none;
}
a:active {
  color: #008CBA;
  background-color: white;
  text-decoration: none;
}

.research-row {
  display: flex;
  align-items: center;
  gap: 2em;
  margin: 1.5em 0;
}
.research-row .research-text {
  flex: 1 1 50%;
}
.research-row .research-image {
  flex: 1 1 50%;
  text-align: center;
}
.research-row .research-image img {
  width: auto;
  max-width: 100%;
  height: auto;
  max-height: 130px;
}
@media (max-width: 600px) {
  .research-row {
    flex-direction: column;
  }
}
</style>

## AI for Optimization: Fast and Reliable Data-Driven Decision-Making

My research sits at the intersection of optimization, machine learning, and control, spanning applications from robotics and power grids to finance and autonomous systems.

### Parametric optimization

Many decision-making problems can be cast as a *parametric optimization problem*: given a problem parameter $x$ (e.g., a sensor reading, a market price, or a system's current state), we must repeatedly solve an optimization problem to compute an optimal solution $z^\star(x)$. Doing this reliably, and fast enough to run online, is at the core of my research.

<img src="{{rajivsambharya.github.io}}/images/research/parametric.png" alt="Parametric optimization" style="width: 100%; max-width: 420px; height: auto; display: block; margin: 0 auto;"/>

### Research question

<img src="{{rajivsambharya.github.io}}/images/research/research_question.png" alt="Research question" style="width: 100%; height: auto;"/>

### Research outline

I organize my work around three connected themes.

<div class="research-row">
  <div class="research-text"><strong>Learning to optimize (L2O): accelerating algorithms with guarantees.</strong> I develop learned optimizers that warm-start or accelerate classical iterative algorithms, while preserving the convergence and correctness guarantees that make those algorithms trustworthy.</div>
  <div class="research-image"><img src="{{rajivsambharya.github.io}}/images/research/l2o.png" alt="Learning to optimize"/></div>
</div>

<div class="research-row">
  <div class="research-text"><strong>Data-driven guarantees for parametric optimization.</strong> I use data to derive sharper, instance-specific performance bounds for optimization algorithms, going beyond the loose worst-case guarantees given by classical analysis.</div>
  <div class="research-image"><img src="{{rajivsambharya.github.io}}/images/research/data_driven_guarantees.png" alt="Data-driven guarantees"/></div>
</div>

<div class="research-row">
  <div class="research-text"><strong>Control: parametric optimization in a loop.</strong> I study how these learned and data-driven optimization tools behave when embedded inside a feedback loop with dynamics, as in model predictive control.</div>
  <div class="research-image"><img src="{{rajivsambharya.github.io}}/images/research/control.png" alt="Control" style="max-height: 110px;"/></div>
</div>
