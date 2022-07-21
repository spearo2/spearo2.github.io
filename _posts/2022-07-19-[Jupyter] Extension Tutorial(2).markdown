---
layout: post
category: research
---

# JupyterLab Extension Tutorial
# 2. Developing an Extention.

## 2-1. Cookie Cutter

In this post, the extention creation is done by the cokkiecutter.

If you do not have it installed yet, use the following command to install.

`$ pip install cookiecutter`

This cookiecutter is a tool to create an extention.

Let's try to create an extention from an existing repository.


This method below is out dated. I am keeping this alive just in case. Please, skip this part.

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Move to your working directory and run the following command.
`$ cookiecutter https://github.com/jupyterlab/extension-cookiecutter-ts`

Then, you will see below questions about the extension configuration.

<img src="{{site.url}}/assets/images/research/cookie1.png" width="auto" height="auto" alt="cookie1">

Values within the brackets are the default values. I just setted author name and email address for now.

Then a repo will be cloned with your configuration as below

<img src="{{site.url}}/assets/images/research/cookie2.png" width="auto" height="auto" alt="cookie2">
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

For JupyterLab 3.0 and above, I found this another tutorial repo.
<a href="https://github.com/marthacryan/developing-extensions-tutorial">https://github.com/marthacryan/developing-extensions-tutorial</a>

In the new version, installing an extension that is distributed is done by
`pip install <extension name>`
And uninstalling by 
`pip uninstall <extension name>`

To develop, we have to first go to the working directory and run following commands.

```
# Install package in development mode
pip install -e .
# Link your development version of the extension with JupyterLab
jupyter labextension develop . --overwrite
# Server extension must be manually installed in develop mode
jupyter server extension enable tutorial_extension
# Rebuild extension Typescript source after making changes
jlpm build
```

jlpm is a JupyterLab wrapper over the yarn.
so this could be a command equivalent to `npm install` compared to the normal web development process.
