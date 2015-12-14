==========================
 highlight-leading-spaces
==========================

Overview
========

|screenshot|

This minor-mode highlights leading spaces with a face and replaces them with a
special character so they can easily be counted (this can be disabled).

The `whitespace.el`_ package that is built-in to Emacs can be used to
accomplish the same effect, but for *all* spaces, including non-leading spaces
between words. This minor-mode only highlights leading spaces that are part of
the indentation.

The face to highlight leading spaces with can be customised by changing the
``highlight-leading-spaces`` face. The character to replace leading spaces
with can be customised by changing ``highlight-leading-spaces-char``. If you
do not wish to them to be replaced with a special character, set it to a
space.


Installation
============

.. code:: emacs-lisp

   (add-to-list 'load-path "/path/to/highlight-leading-spaces")
   (require 'highlight-leading-spaces)
   (add-hook 'prog-mode-hook 'highlight-leading-spaces-mode)


Licence
=======

Distributed under the `GNU General Public License <LICENSE>`__.


.. _whitespace.el: http://www.emacswiki.org/emacs/WhiteSpace
.. |screenshot| image:: https://raw.githubusercontent.com/mrBliss/highlight-leading-spaces/master/screenshot.png
