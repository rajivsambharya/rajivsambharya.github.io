---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
.button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 8px 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 5px;
}

.button2 {background-color: #008CBA;} /* Blue */
.button4 {background-color: #7B241C;} /* Red */ 
.button3 {background-color: #9B59B6 ;} /* Purple */ 
.button5 {background-color:#EB984E;} /* Orange-brown */
.button6 {background-color:#58D68D;} /* Green */
.button7 {background-color:#1F77B4;} /* Blue */
.button8 {background-color:#FF7F0E;} /* Orange */
.button9 {background-color:#2CA02C;} /* Green */
.button10 {background-color:black;} /* Black */
.button11 {background-color:#BF00BF;} /* Magenta */


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


{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

## Preprints
**End-to-End Learning to Warm-Start for Real-Time Quadratic Optimization**\
Rajiv Sambharya, Georgina Hall, Brandon Amos, Bartolomeo Stellato\
Arxiv Preprint, 2022\
<a href="https://arxiv.org/pdf/2212.08260.pdf">
<button class="button button2">
 Download
</button>
</a>
<a href='javascript:;'
onclick='$("#abs_e2e_qp").toggle()'>
<button class="button button4">
Abstract
</button>
</a>
<a href='javascript:;'
onclick='$("#bib_e2e_qp").toggle()'>
<button class="button button5">
Bibtex
</button>
</a>
<a href="https://github.com/stellatogrp/l2ws">
<button class="button button3">
Code
</button>
</a>
<a href='javascript:;'
onclick='$("#synopsis_e2e_qp").toggle()'>
<button class="button button6">
Synopsis
</button>
</a>


<div id="abs_e2e_qp" style="text-align: justify; display: none; color: white; background-color: #7B241C" markdown="1">
First-order methods are widely used to solve convex quadratic 
programs (QPs) in real-time applications because of their low
 per-iteration cost. However, they can suffer from slow convergence 
 to accurate solutions. In this paper, we present a framework which 
 learns an effective warm-start for a popular first-order method in 
 real-time applications, Douglas-Rachford (DR) splitting, across a family
 of parametric QPs. This framework consists of two modules: a 
 feedforward neural network block, which takes as input the parameters of the QP and outputs a warm-start, and a block which performs a 
fixed number of iterations of DR splitting from this warm-start and outputs a candidate solution. A key feature of our framework is its ability to do end-to-end
learning as we differentiate through the DR iterations. To illustrate the effectiveness
of our method, we provide generalization bounds (based on Rademacher complexity)
that improve with the number of training problems and number of iterations simultaneously. We further apply our method to three real-time applications and observe that, by learning good warm-starts, we are able to significantly reduce the number of
iterations required to obtain high-quality solutions.
</div>
    
<div id="bib_e2e_qp" style="text-align: justify; display: none; color: white; background-color: #EB984E" markdown="1">
<pre>@misc{sambharya_2022_endtoend,
      title={End-to-End Learning to Warm-Start for Real-Time Quadratic Optimization}, 
      author={Rajiv Sambharya and Georgina Hall and Brandon Amos and Bartolomeo Stellato},
      year={2022},
      eprint={2212.08260},
      archivePrefix={arXiv},
      primaryClass={math.OC}
}
</pre>
</div>


<div id="synopsis_e2e_qp" style="text-align: justify; display: none; color: black; background-color: white" markdown="1">
<img src="https://www.do-mpc.com/en/latest/_images/oscillating_masses.png" width="500" 
     height="600" />
     
Consider a system of many masses and springs where the masses have actuators that we can control. The goal is to control the system so that it tracks a reference trajectory. Specifically, we aim to solve the convex optimization problem,

<img src="{{rajivsambharya.github.io}}/images/osc_mass_prob.jpg" width="400" 
     height="500"/>

where the $x_t$'s are the states and the $u_t$'s are the controls.

In the model predictive control paradigm, we solve this problem for some horizon length and implement the first control, $u_0$. After this, we resolve the problem where only the initial state parameter, $\theta = x_\{\rm{init}\}$ changes. Since we need to solve this problem many times, we will have an abundance of data to use. Standard optimization techniques don't capitalize on this data. In our work, we learn a good warm-start for Douglas-Rachford (DR) splitting from this data.

<img src="{{rajivsambharya.github.io}}/images/learning_framework_diagram.jpg" width="500" 
     height="600"/>
     
Left: standard DR splitting which maps parameter $\theta$ and initialization $z^0$ to an approximate solution $z^k(\theta)$. 
Right: Proposed learning framework consisting of two modules.
The first module is the NN block which maps the parameter $\theta$ to a warm-start $z^k_{\mathcal{W}}(\theta)$. 
The weights of the NN, denoted by $\mathcal{W}$, are the only variables we optimize over. 
The second module runs $k$ iterations of DR splitting (which also depend on $\theta$) starting with the warm-start $z^k_{\mathcal{W}}(\theta)$ and returning a candidate solution $z^k_{\mathcal{W}}(\theta)$. 
We backpropagate from the loss $\ell_{\theta}(z^k_{\mathcal{W}}(\theta))$ through the DR iterates to learn the optimal weights $\mathcal{W}$.


<img src="{{rajivsambharya.github.io}}/images/osc_mass_eval.jpg" width="500" 
     height="600"/>
     
<button class="button button10">  </button> no warm-start

<button class="button button11">  </button>  nearest neighbor warm-start 

<button class="button button7">  </button> learned warm-start with $k=5$

<button class="button button8">  </button> learned warm-start with $k=15$

<button class="button button9">  </button> learned warm-start with $k=50$
        
We plot the test fixed point residuals for different warm-starts of DR splitting.
We train our architecture with $k=5,15,$ and $50$ DR iterations.
We compare our results against a random initialization (black) and against warm-starting DR splitting with the nearest neighbor from the train set (magenta).

</div>


**Lifted Neural Networks**\
Armin Askari, Geoffrey Negiar, Rajiv Sambharya, Laurent El Ghaoui\
Arxiv Preprint, 2018\
<a href="https://arxiv.org/pdf/1805.01532.pdf">
<button class="button button2">
Download
</button>
</a>
<a href='javascript:;'
onclick='$("#abs_lifted_nn").toggle()'>
<button class="button button4">
Abstract
</button>
</a>
<a href='javascript:;'
onclick='$("#bib_lifted_nn").toggle()'>
<button class="button button5">
Bibtex
</button>
</a>

<div id="abs_lifted_nn" style="text-align: justify; display: none; color: white; background-color: #7B241C" markdown="1">
We describe a novel family of models of multi- layer feedforward neural networks in which the activation functions are encoded via penalties in the training problem. Our approach is based on representing a non-decreasing activation function as the argmin of an appropriate convex optimization problem. The new framework allows for algorithms such as block-coordinate descent methods to be applied, in which each step is composed of a simple (no hidden layer) supervised learning problem that is parallelizable across data points and/or layers. Experiments indicate that the pro- posed models provide excellent initial guesses for weights for standard neural networks. In addition, the model provides avenues for interesting extensions, such as robustness against noisy in- puts and optimizing over parameters in activation functions.
</div>

<div id="bib_lifted_nn" style="text-align: justify; display: none; color: white; background-color: #EB984E" markdown="1">
<pre>@misc{askari_lifted_nn,
  doi = {10.48550/ARXIV.1805.01532},
  url = {https://arxiv.org/abs/1805.01532},
  author = {Askari, Armin and Negiar, Geoffrey and Sambharya, Rajiv and Ghaoui, Laurent El},
  keywords = {Machine Learning (cs.LG), Machine Learning (stat.ML), FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Lifted Neural Networks},
  publisher = {arXiv},
  year = {2018},
  copyright = {Creative Commons Attribution Share Alike 4.0 International}
}</pre>
</div>



