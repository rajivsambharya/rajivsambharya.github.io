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

.button2 {background-color: #008CBA; onclick='$("#bib_e2e_qp").toggle()';} /* Blue */
.button3 {background-color: #f44336;} /* Red */ 
.button4 {background-color: #e7e7e7; color: black;} /* Gray */ 
.button5 {background-color: orange;} /* Orange */
</style>

<button id="myButton" class="float-left submit-button" >Home</button>

<script type="text/javascript">
    document.getElementById("myButton").onclick = function () {
        location.href = "www.nytimes.com";
    };
</script>

<a href="http://www.stackoverflow.com/">
    <button>Click me</button>
</a>





{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

## Preprints
**Lifted Neural Networks**\
Armin Askari, Geoffrey Negiar, Rajiv Sambharya, Laurent El Ghaoui\
Arxiv Preprint, 2018\
<a href="https://arxiv.org/pdf/1805.01532.pdf">
<button class="button button2">
bibtex
</button>
</a>
<a href='javascript:;'
onclick='$("#bib_lifted_nn").toggle()'>
<button class="button button5">
bibtex
</button>
</a>

<div id="bib_lifted_nn" style="text-align: justify; display: none" markdown="1">
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

**End-to-End Learning to Warm-Start for Real-Time Quadratic Optimization**\
Rajiv Sambharya, Georgina Hall, Brandon Amos, Bartolomeo Stellato\
Arxiv Preprint, 2018\
[Link](https://arxiv.org/pdf/2212.08260.pdf){: .btn .btn--info}
<a href='javascript:;'
onclick='$("#bib_e2e_qp").toggle()'>
<button class="button button5">
bibtex
</button>
</a>
    
<div id="bib_e2e_qp" style="text-align: justify; display: none" markdown="1">
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


