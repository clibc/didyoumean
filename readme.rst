How about ___
=============

.. image:: https://travis-ci.org/chrlie/howabout.png?branch=master
   :alt: Build status
   :target: https://travis-ci.org/chrlie/howabout

.. image:: https://img.shields.io/pypi/v/howabout.svg
    :target: https://pypi.python.org/pypi/howabout


Howabout is a Python library to suggest similar strings. Use it in a command-line project or anywhere where simple misspellings occur.

.. code:: python

   from howabout import best_match

   choices = ['sat', 'sot']

   # returns 'sat', since 
   #   'sat' -> 'sate'
   #   'sot' -> 'sat' -> 'sate'
   best_match('sate', choices) 

Examples can be found under ``examples/``.

Argparse
--------

Python's ``argparse`` library is not supported out of the box as it cannot be extended or patched.

Installation
------------

Install with pip:

.. code:: sh

   $ pip install howabout

Testing
-------

Use ``tox`` to run the tests.

.. code:: sh

   $ virtualenv --no-site-packages .python && source .python/bin/activate
   $ pip install -r requirements.txt
   $ tox
