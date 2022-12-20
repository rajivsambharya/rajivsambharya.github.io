---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

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
[Bibtex](https://dblp.uni-trier.de/rec/journals/corr/abs-1805-01532.html?view=bibtex){: .btn .btn--warning}

<a href='javascript:;'
    onclick='$("#abs_amos2022tutorial").toggle()'>abs</a>] [<a href='https://github.com/facebookresearch/amortized-optimization-tutorial' target='_blank'>code</a>]
    
    <div id="abs_amos2022tutorial" style="text-align: justify; display: none" markdown="1">
Optimization is a ubiquitous modeling tool that is often deployed in
settings that repeatedly solve similar instances of
the same problem. Amortized optimization methods use
learning to predict the solutions to problems in
these settings. This leverages the shared structure
between similar problem instances. In this tutorial, we will discuss the key design choices behind
amortized optimization, roughly categorizing 1)
models into fully-amortized and semi-amortized
approaches, and 2) learning methods into
regression-based and objective-based. We then view
existing applications through these foundations to
draw connections between them, including for
manifold optimization, variational inference, sparse
coding, meta-learning, control, reinforcement
learning, convex optimization, and deep equilibrium
networks. This framing enables us easily see, for
example, that the amortized inference in variational
autoencoders is conceptually identical to value
gradients in control and reinforcement learning as
they both use fully-amortized models with a
objective-based loss.
</div>

</td>
</tr>
