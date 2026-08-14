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

.research-timeline {
  position: relative;
  padding-left: 48px;
  margin: 1.5em 0;
}
.research-timeline::before {
  content: "";
  position: absolute;
  left: 19px;
  top: 8px;
  bottom: 8px;
  width: 2px;
  background: #d7d7d7;
}
.research-row {
  position: relative;
  display: flex;
  align-items: center;
  gap: 2em;
  margin: 1.6em 0;
  padding: 1.4em 1.6em;
  border: 1px solid #e3e3e3;
  border-radius: 10px;
  background: #fff;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.05);
}
.research-row::before {
  content: "";
  position: absolute;
  left: -35px;
  top: 50%;
  transform: translateY(-50%);
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: #008CBA;
  border: 3px solid #fff;
  box-shadow: 0 0 0 2px #008CBA;
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

.image-box {
  display: block;
  width: fit-content;
  max-width: 100%;
  margin: 1.5em auto;
  padding: 1.2em;
  border: 1px solid #e3e3e3;
  border-radius: 10px;
  background: #fff;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.05);
}
.image-box img {
  display: block;
  width: 100%;
  max-width: 420px;
  height: auto;
  margin: 0;
}
</style>

## AI for Optimization: Fast and Reliable Data-Driven Decision-Making

In many high-stakes domains such as autonomous systems, power grids, and signal processing, we must repeatedly solve similar optimization problem instances in real time as conditions change. Mathematically, this means solving the same parametric optimization problem

<div class="image-box"><img src="{{rajivsambharya.github.io}}/images/research/parametric.png" alt="Parametric optimization"/></div>

for a different problem parameter $x$ each time. For example, in control we re-solve for the optimal inputs as the initial state changes. In power systems, we re-solve for network power flows as demand and renewable generation shift.

Classical algorithms solve each instance from scratch, ignoring the structure shared across the family. Data offers a way to exploit that structure: to build faster algorithms, derive tighter performance guarantees, and characterize complex systems in which optimization one part among many. This motivates my overarching research question:

<div class="image-box" style="max-width: 100%;"><img src="{{rajivsambharya.github.io}}/images/research/research_question.png" alt="Research question" style="max-width: 100%;"/></div>

### Research agenda

I am currently organizing my work around three connected directions.

<div class="research-timeline">

<div class="research-row">
  <div class="research-text"><strong>Learning to accelerate optimization algorithms.</strong><br>I develop learned optimizers that warm-start or accelerate classical iterative algorithms, while preserving the convergence and correctness guarantees that make those algorithms trustworthy.</div>
  <div class="research-image"><img src="{{rajivsambharya.github.io}}/images/research/l2o.png" alt="Learning to optimize"/></div>
</div>

<div class="research-row">
  <div class="research-text"><strong>Data-driven algorithm analysis.</strong><br>I use data to derive sharper, instance-specific performance bounds for optimization algorithms, going beyond the loose worst-case guarantees given by classical analysis.</div>
  <div class="research-image"><img src="{{rajivsambharya.github.io}}/images/research/data_driven_guarantees.png" alt="Data-driven guarantees"/></div>
</div>

<div class="research-row">
  <div class="research-text"><strong>Control: parametric optimization in a loop.</strong><br>I study how these learned and data-driven optimization tools behave when embedded inside a feedback loop with dynamics, as in model predictive control.</div>
  <div class="research-image"><img src="{{rajivsambharya.github.io}}/images/research/control.png" alt="Control" style="max-height: 110px;"/></div>
</div>

</div>


### Tools I rely on
Throughout my research, I rely on a wide variety of tools: first-order methods, convex optimization, bilevel optimization, deep learning, statistical learning theory, online learning, and model predictive control to name a few.