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
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}

.button2 {background-color: #008CBA;} /* Blue */
.button3 {background-color: #f44336;} /* Red */ 
.button4 {background-color: #e7e7e7; color: black;} /* Gray */ 
.button5 {background-color: #555555;} /* Black */
</style>

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

## Preprints
**Lifted Neural Networks**\
Armin Askari, Geoffrey Negiar, Rajiv Sambharya, Laurent El Ghaoui\
Arxiv Preprint, 2018\
[Link](https://arxiv.org/pdf/1805.01532.pdf){: .btn .btn--info}
[Bibtex](https://dblp.uni-trier.de/rec/journals/corr/abs-1805-01532.html?view=bibtex){: .btn .btn--warning}

**End-to-End Learning to Warm-Start for Real-Time Quadratic Optimization**\
Rajiv Sambharya, Georgina Hall, Brandon Amos, Bartolomeo Stellato\
Arxiv Preprint, 2018\
[Link](https://arxiv.org/pdf/2212.08260.pdf){: .btn .btn--info}
<a><button class="button button2>
[<a href='javascript:;'
    onclick='$("#abs_e2e_qp").toggle()'>bibtex</a>]
</button></a>
    
<div id="abs_e2e_qp" style="text-align: justify; display: none" markdown="1">
<pre>@misc{sambharya2022endtoend,
      title={End-to-End Learning to Warm-Start for Real-Time Quadratic Optimization}, 
      author={Rajiv Sambharya and Georgina Hall and Brandon Amos and Bartolomeo Stellato},
      year={2022},
      eprint={2212.08260},
      archivePrefix={arXiv},
      primaryClass={math.OC}
}
</div>

<button class="button">Green</button>
<button class="button button2">Blue</button>
<button class="button button3">Red</button>
<button class="button button4">Gray</button>
<button class="button button5">Black</button>

