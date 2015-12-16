==================================
 highlight-leading-spaces |melpa|
==================================

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

This minor-mode is quite efficient because it doesn't use overlays but text
properties for the leading spaces. Furthermore, the highlights are correctly
and efficiently kept up-to-date by plugging in to font-lock, not by adding
various hooks.


Installation
============

MELPA_
------

1. Install_ the ``highlight-leading-spaces`` package.

2. Use the ``highlight-leading-spaces-mode`` hook to enable this minor-mode:

   .. code:: emacs-lisp

      (add-hook 'prog-mode-hook 'highlight-leading-spaces-mode)


use-package_
------------

Users of `use-package`_ can add the following lines to their config:

.. code:: emacs-lisp

   (use-package highlight-leading-spaces
     :ensure t
     :defer t
     :init (add-hook 'prog-mode-hook 'highlight-leading-spaces-mode))

Manual
------

Download this package and add the following lines to your config.

.. code:: emacs-lisp

   (add-to-list 'load-path "/path/to/highlight-leading-spaces")
   (require 'highlight-leading-spaces)
   (add-hook 'prog-mode-hook 'highlight-leading-spaces-mode)


Licence
=======

Distributed under the `GNU General Public License <LICENSE>`__.


.. _whitespace.el: http://www.emacswiki.org/emacs/WhiteSpace
.. |screenshot| image:: https://raw.githubusercontent.com/mrBliss/highlight-leading-spaces/master/screenshot.png
.. _MELPA: http://melpa.org/
.. _Install: http://melpa.org/#/getting-started
.. _use-package: https://github.com/jwiegley/use-package
.. |melpa| image:: http://melpa.org/packages/highlight-leading-spaces-badge.svg
           :target: http://melpa.org/#/highlight-leading-spaces
