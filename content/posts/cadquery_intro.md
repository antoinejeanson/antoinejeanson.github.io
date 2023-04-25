---
title: "CAD for developpers: an introduction to CadQuery"
date: 2023-04-25T18:00:00+02:00
draft: true
---

# What is CadQuery ?

In essence, CadQuery is a Python Computer Aided Design (CAD) library that allows designing mechanical parts using code.

It might remind you of [OpenSCAD](https://openscad.org), except it leverages the power of Python and OpenCASCADE to
extend your design capabilities.

It aims at being the most direct way to transform a description of a mechanical part to a CAD model using clear,
human-readable instructions.
In fact, it is much, _much_ more powerful.

As an example, here's CadQuery code to create a 20mm calibration cube with a 10mm hole in it, and export it to an STL
file for 3D printing:

```python
import cadquery as cq
result = cq.Workplane("front").box(20, 20, 20).faces(">Z").hole(10)
cq.exporters.export(result, "test.stl")
```

Even without deep knowledge of Python, this is readable and very close to how you would describe it using plain words.

# Why is CADQuery so cool ?

Ever wanted to serve parameteric CAD parts from FastAPI ?
To integrate the power of Git versioning to your CAD projects ?
To use CI/CD tools with mechanical engineering workflows ?

Maybe. Maybe not. Anyways CadQuery is one more open-source tool to consider when building stuff that require mechanical
parts. The fact your part is code and the integration of Python capabilities is the icing on the cake.

# Trying it out

Here are some instructions on how to get started.
This assumes some basic knowledge of Python.

If you prefer to dive right into it, here are the [Official docs](https://cadquery.readthedocs.io/en/latest/index.html)


## Installation

The simplest way to get started is simply installing the `cadquery` package.

```bash
pip install cadquery
```

And that's basically it.
At the time of writing, CadQuery only supports Python up to 3.10.

There are more methods you can use to install the `cadquery` package.
For now, it all comes down to personal preference.
See the [official documentation](https://cadquery.readthedocs.io/en/latest/installation.html) for more installation
instructions.

## Your first part

Start by importing `cadquery`:

```python
import cadquery as cq
```

# Going further
