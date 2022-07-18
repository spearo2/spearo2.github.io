---
layout: post
category: research
---

# Jupyter Notebook Extension Tutorial

As I was assigned to develop a code suggestion tool for JupyterLab by Korea Institute of Science and Technology (KISTI), this post summarizes the tutorial for building an extention.

Details can be found at <a herf="https://www.youtube.com/watch?v=_ZexgrCGttU">https://www.youtube.com/watch?v=_ZexgrCGttU</a>.

## What is JupyterLab?


JupyterLab is the next generation UI for Jupyter Notebook.
It is developed to replace Jupyter Notebook with more modular and extensible architecture.

<img src="{{site.url}}/assets/images/research/notebook.png" width="20%" height="20%" alt="notebook">
Original Notebook
<img src="{{site.url}}/assets/images/research/lab.png" width="20%" height="20%" alt="lab">
JupyterLab

JupyterLab provides more interactive features such as npm based typescript support.

For the original Notebook, it is based on kernel that includes various compilers and interpreters supporting various programmin languages. However, reading this, I assume that you are already familiar with the Notebook environment. The notebook could have internal extensions but had a lot of compatibility issues.

Here, we deal with JupyterLab because it allows various custom extensions.

<a herf="https://github.com/jupyterlab/jupyterlab">This is the repo for the jupyterlab</a>

## How to Install Extensions

Before installing, let's check out two terms.

labextension - front end extensions.
serverextension - back end extensions.

### Let's start with the labextension.

Start JupyterLab with the following command.

```$ jupyter lab```

If Jupyter packages are not installed, you can do it by the following command

```$ pip install jupyterlab```


Then you will see the red "Enable" button for searching and adding extensions.

<img src="{{site.url}}/assets/images/research/searchEX1.png" width="20%" height="20%" alt="lab">

Here, you can install various extensions.
Once you are done with the installation, it will ask you to reload the page. Once the page is reloaded, you can use the extenstions depending on the usage(mostly, there will be an added tab on the left side of the window).

If an implemented extension is published, it can be viewed in this search bar.

So, the labextension can be installed through the UI.
On the other hand, the serverextensions are installed through CLI and also require restarting the JupyterLab.


### How do we deal with both labextensions and serverextensions

