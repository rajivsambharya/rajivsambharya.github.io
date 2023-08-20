---
layout: archive
title: "Animations"
permalink: /animations/
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
</style>

## Learning to Warm-Start Fixed-Point Optimization Algorithms
Many applications in robotics and control require real-time solutions.
We consider the problem of flying a quadcopter to follow a reference trajectory.
Model predictive control is a popular technique which requires solving a new optimization problem
at each time step.
To fly a quadcopter, we impose a budget of $5$ fixed-point steps to solve each problem.
With our learned approach, we can solve the QPs more accurately than the other initialization techniques: using the nearest neighbor and previous solution.
<!-- <a href="{{rajivsambharya.github.io}}/animations/rollout_2_flight_learned.gif" download>
  Slides
</a>\ -->

<!-- <div style="display: flex; justify-content: space-between;">
  <div style="flex: 1;">
    <img src="{{rajivsambharya.github.io}}/animations/rollout_2_flight_nn_endless.gif" alt="Alt Text">
    <p style="text-align: center;">Nearest neighbor</p>
  </div>
  
  <div style="flex: 1;">
    <img src="{{rajivsambharya.github.io}}/animations/rollout_2_flight_ps_endless.gif" alt="Alt Text">
    <p style="text-align: center;">Previous solution</p>
  </div>
  
  <div style="flex: 1;">
    <img src="{{rajivsambharya.github.io}}/animations/rollout_2_flight_learned_endless.gif" alt="Alt Text">
    <p style="text-align: center;">Learned</p>
  </div> -->
<!-- </div> -->
<div style="display: flex; justify-content: space-around;">
  <div style="flex: 1; margin-right: 0px;">
    <img src="{{rajivsambharya.github.io}}/animations/rollout_2_flight_nn_endless.gif" alt="Alt Text">
    <p style="text-align: center;">Nearest neighbor</p>
  </div>
  
  <div style="flex: 1; margin-right: 0px;">
    <img src="{{rajivsambharya.github.io}}/animations/rollout_2_flight_ps_endless.gif" alt="Alt Text">
    <p style="text-align: center;">Previous solution</p>
  </div>
  
  <div style="flex: 1;">
    <img src="{{rajivsambharya.github.io}}/animations/rollout_2_flight_learned_endless.gif" alt="Alt Text">
    <p style="text-align: center; color: blue">Learned</p>
  </div>
</div>