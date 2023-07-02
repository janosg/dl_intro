# Lecture 10

## Topic

In this lecture we look at Recurrent Neural Networks (RNNs). RNNs are sequence to
sequence models, i.e. models that can take text and return text. Nowadays, RNNs have
been replaced by transformer models in almost all applications. However, we need to
understand them on our way to understanding transformers.

## Lecture Slides

```{raw} html
<iframe src="_static/bld/pdfs/lecture_10.pdf" width="700" height="415"></iframe>
```

```{eval-rst}
:download:`Download the slides <_static/bld/pdfs/lecture_10.pdf>`
```

## Exercises


```{toctree}
---
maxdepth: 1
---
bld/notebooks/exercises/exercise_10.ipynb
bld/notebooks/solutions/exercise_10.ipynb
```

## Suggested Homework

- Finish all exercises you did not solve in class
- Go over the additional materials


## Additional materials

### Karpathy's blogpost

This [blogpost](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) is how everyone learns RNNs. It is really good and very accessible.


### RNNs from scratch

This [blogpost](https://victorzhou.com/blog/intro-to-rnns/) implements RNNs from scratch
in Python and goes deeper than we went. For example, it also implements a back-propagation
from scratch.


### Videos from cs224n at Stanford

I can recommend the whole lecture series if you want to go much deeper than what we
did in this course. For RNNs, one and a half videos are relevant:

<iframe width="560" height="315" src="https://www.youtube.com/embed/PLryWeHPcBs?start=3000" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


<iframe width="560" height="315" src="https://www.youtube.com/embed/0LixFSa7yts" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

You can skip everything on LSTMs. LSTMs are a variety of RNNs that alleviate some of
the problems but now have been replaced by transformers.
