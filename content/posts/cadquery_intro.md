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

# Why am I so exited ?

I really like building stuff _as_ code.
Not necessarly developping stuff, but I like the idea of defining things using code.
It allows you to use tools such as Git and Continuous Integration / Continuous Delivery (CI/CD) to improve your
workflow.
A text editor you like is much more usable than an un-ergonomic graphical user interface.

CAD is integral to maker culture, and CadQuery is one more open-source tool to consider when building mechanical stuff.

To me, the fact your part is code and the integration of Python capabilities is the icing on the cake.

Integrating code to design opens the door to workflows that have the potential to revolutionize plenty of fields.

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
