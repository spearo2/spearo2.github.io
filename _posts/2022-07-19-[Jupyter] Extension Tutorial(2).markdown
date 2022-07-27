---
layout: post
category: research
---

# JupyterLab Extension Tutorial
# 2. Create a new Extention.


In this post, the extention creation is done by the cokkiecutter.

If you do not have it installed yet, use the following command to install.

`$ pip install cookiecutter`

This cookiecutter is a tool to create an extention.

Let's try to create an extention from an existing repository.




Move to your working directory and run the following command.
`$ cookiecutter https://github.com/jupyterlab/extension-cookiecutter-ts`

Then, you will see below questions about the extension configuration.

<img src="{{site.url}}/assets/images/research/cookie1.png" width="auto" height="auto" alt="cookie1">

Values within the brackets are the default values. I just setted author name and email address for now.

Then a repo will be cloned with your configuration as below

<img src="{{site.url}}/assets/images/research/cookie2.png" width="auto" height="auto" alt="cookie2">



You can create a new github repo based on the created directory.

To develop, we have to first go to the working directory and run following commands.

```
# Install package in development mode
$ pip install -ev .
# Link your development version of the extension with JupyterLab
$ jupyter labextension develop . --overwrite
# Server extension must be manually installed in develop mode
$ jupyter server extension enable tutorial_extension
# Rebuild extension Typescript source after making changes
$ jlpm build
```

Otherwise, you can just run the command `jupyter lab` after the overwite.

jlpm is a JupyterLab wrapper over the yarn.
so this could be a command equivalent to `npm install` compared to the normal web development process.


