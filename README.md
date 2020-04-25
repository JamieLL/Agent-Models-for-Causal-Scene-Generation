# Object Oriented Models for Causal Scene Generation

## Authors

[Junmei Luo](https://www.linkedin.com/in/junmei-luo/), [Boya Zhang
](https://www.linkedin.com/in/boya-bella-zhang/)

## Abstract

In this course - CS 7290: Causal Machine Learning - we have been learning to reflect on a data generating process and represent it with a causal model. However, if we take a [vision-as-inverse-graphics](https://ps.is.tuebingen.mpg.de/research_fields/inverse-graphics) view of computer vision, we could think of captions as a natural language representation of the data generating process that generated tge accompanying image.

Our project is to take these natural language descriptions and turn them into the basic ingrediates of a probabilistic programs, and then convert it into a picture. In this project, we designed an object-oriented causal effect model which can generate a reasonable image from the model result. The structure of the object-oriented causal effect model is inspired by [Practical Probabilistic Programming](https://dl.acm.org/doi/book/10.5555/3033232) Chapter 7.

In the model, we have 2 agents: a person and an animal. There are some interactions between them and the interaction is conditioned on their position(internal) and the background / environment(external). Condition or intervention on their attributes will affect the final generated image.

Here are the attributes of each class: <br>
Person： position1， haircolor， hairlength， gender， age <br>
Animal： position2, color, size, type <br>
Background： background <br>
Interaction： interaction

The causal model uses `pyro` to generate samples and forms captions like the following;

    A old female with black long hair fights a little black cat in the park.
    A young female with golden short hair holds a little grey cat at home.
    A young male with black long hair calls a little brown dog in the park.
    A young male with golden long hair fights a little black cat in the park.

Then a picture will be generated using some simple elements.

[See video abstract](https://www.youtube.com/watch?v=o3GfnEjTdIQ)

## How to explore this project



### Presentation

### Reproducibility

This project requires the following external packages that need to be installed.

<p><code>
pip install graphviz #conda install Pillow<br>
pip install torch <br>
pip install pyro <br>
pip install numpy <br>
pip install ipython <br>
pip install ipywidgets <br>
pip install pil #pip install Pillow
</code></p>