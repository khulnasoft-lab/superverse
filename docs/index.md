---
template: index.html
comments: true
hide:
  - navigation
  - toc
---

<div class="md-typeset">
  <h1></h1>
</div>

<div align="center" id="logo">
  <a align="center" href="" target="_blank">
      <img width="850"
          src="https://media.khulnasoft.com/open-source/metavision/rf-metavision-banner.png?updatedAt=1678995927529">
  </a>
</div>

## 👋 Hello

We write your reusable computer vision tools. Whether you need to load your dataset from your hard drive, draw detections on an image or video, or count how many detections are in a zone. You can count on us!

<video controls>
    <source
        src="https://media.khulnasoft.com/traffic_analysis_result.mp4"
        type="video/mp4"
    >
</video>

## 💻 Install

You can install `metavision` in a
[**Python>=3.8**](https://www.python.org/) environment.

!!! example "pip install (recommended)"
=== "pip"
[![version](https://badge.fury.io/py/metavision.svg)](https://badge.fury.io/py/metavision)
[![downloads](https://img.shields.io/pypi/dm/metavision)](https://pypistats.org/packages/metavision)
[![license](https://img.shields.io/pypi/l/metavision)](https://github.com/khulnasoft/metavision/blob/main/LICENSE.md)
[![python-version](https://img.shields.io/pypi/pyversions/metavision)](https://badge.fury.io/py/metavision)

        ```bash
        pip install metavision
        ```

!!! example "conda/mamba install"
=== "conda"
[![conda-recipe](https://img.shields.io/badge/recipe-metavision-green.svg)](https://anaconda.org/conda-forge/metavision) [![conda-downloads](https://img.shields.io/conda/dn/conda-forge/metavision.svg)](https://anaconda.org/conda-forge/metavision) [![conda-version](https://img.shields.io/conda/vn/conda-forge/metavision.svg)](https://anaconda.org/conda-forge/metavision) [![conda-platforms](https://img.shields.io/conda/pn/conda-forge/metavision.svg)](https://anaconda.org/conda-forge/metavision)

        ```bash
        conda install -c conda-forge metavision
        ```

    === "mamba"
        [![mamba-recipe](https://img.shields.io/badge/recipe-metavision-green.svg)](https://anaconda.org/conda-forge/metavision) [![mamba-downloads](https://img.shields.io/conda/dn/conda-forge/metavision.svg)](https://anaconda.org/conda-forge/metavision) [![mamba-version](https://img.shields.io/conda/vn/conda-forge/metavision.svg)](https://anaconda.org/conda-forge/metavision) [![mamba-platforms](https://img.shields.io/conda/pn/conda-forge/metavision.svg)](https://anaconda.org/conda-forge/metavision)

        ```bash
        mamba install -c conda-forge metavision
        ```

!!! example "git clone (for development)"
=== "virtualenv"

````bash # clone repository and navigate to root directory
git clone https://github.com/khulnasoft/metavision.git
cd metavision

        # setup python environment and activate it
        python3 -m venv venv
        source venv/bin/activate
        pip install --upgrade pip

        # installation
        pip install -e "."
        ```

    === "poetry"
        ```bash
        # clone repository and navigate to root directory
        git clone https://github.com/khulnasoft/metavision.git
        cd metavision

        # setup python environment and activate it
        poetry env use python3.10
        poetry shell

        # installation
        poetry install
        ```

## 🚀 Quickstart

<div class="grid cards" markdown>

- **Detect and Annotate**

  ***

  Annotate predictions from a range of object detection and segmentation models

  [:octicons-arrow-right-24: Tutorial](how_to/detect_and_annotate.md)

- **Track Objects**

  ***

  Discover how to enhance video analysis by implementing seamless object tracking

  [:octicons-arrow-right-24: Tutorial](how_to/track_objects.md)

- **Detect Small Objects**

  ***

  Learn how to detect small objects in images

  [:octicons-arrow-right-24: Tutorial](how_to/detect_small_objects.md)

- **Count Objects Crossing Line**

  ***

  Explore methods to accurately count and analyze objects crossing a predefined line

  [:octicons-arrow-right-24: Notebook](https://metavision.khulnasoft.com/latest/notebooks/count-objects-crossing-the-line/)

- > **Filter Objects in Zone**

  ***

  Master the techniques to selectively filter and focus on objects within a specific zone

- **Cheatsheet**

  ***

  Access a quick reference guide to the most common `metavision` functions

  [:octicons-arrow-right-24: Cheatsheet](https://khulnasoft.github.io/cheatsheet-metavision/)

</div>
````
