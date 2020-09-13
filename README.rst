README
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This directory contains the reStructuredText (reST) sources to documentation.
You don't need to build them yourself.


Building the docs
=================

You need to have Python 2.4 or higher installed; the toolset used to build the
docs is written in Python.  It is called *Sphinx*, it is not included in this
tree, but maintained separately.  Also needed are the docutils, supplying the
base markup that Sphinx uses, Jinja, a templating engine, and optionally
Pygments, a code highlighter.


Using make
----------

Luckily, a Makefile has been prepared so that on Unix, provided you have
installed Python and Subversion, you can just run ::

   make html

Available make targets are:

 * "html", which builds standalone HTML files for offline viewing.

 * "htmlhelp", which builds HTML files and a HTML Help project file usable to
   convert them into a single Compiled HTML (.chm) file -- these are popular
   under Microsoft Windows, but very handy on every platform.

   To create the CHM file, you need to run the Microsoft HTML Help Workshop over
   the generated project (.hhp) file.

 * "latex", which builds LaTeX source files as input to "pdflatex" to produce
   PDF documents.

 * "text", which builds a plain text file for each source file.

 * "linkcheck", which checks all external references to see whether they are
   broken, redirected or malformed, and outputs this information to stdout as
   well as a plain-text (.txt) file.

 * "changes", which builds an overview over all versionadded/versionchanged/
   deprecated items in the current version. This is meant as a help for the
   writer of the "What's New" document.

 * "coverage", which builds a coverage overview for standard library modules and
   C API.

 * "pydoc-topics", which builds a Python module containing a dictionary with
   plain text documentation for the labels defined in
   `tools/sphinxext/pyspecific.py` -- pydoc needs these to show topic and
   keyword help.

A "make update" updates the Subversion checkouts in `tools/`.


Contributing
============


Copyright notice
================

Copyright (c) 2020, lucas_hsueh@hotmail.com.
All rights reserved.

See the file "LICENSE" for more information.
