.. title: String completion as you move to Python 3 (OR, how curly braces became important)
.. slug: string-completion-as-you-move-to-python-3-or-how-curly-braces-became-important
.. date: 2017-02-03 22:00:23 UTC-05:00
.. tags: Python
.. category: Blog
.. link: 
.. description: 
.. type: text

I am currently in the midst of (**FINALLY!!**) making the shift from trusted Python 2.7 to Python 3.x (while recovering from an extended holiday thanks to a somewhat lengthy visa renewal process). Making the shift itself is pretty simple, thanks to a nifty, command line tool built within the Python standard library itself (at least on Linux) called, very simply, `2to3`_.

Its always a good idea to keep backups of legacy code (of course!), and to actually write changes to file, so the command goes something like::

    2to3 -w *.py

I am in the habit of using % as a placeholder for string completion in Python 2.x. That behavior doesn't go out of use entirely in Python 3.x, but using the str.format() method is recommended instead - see more `details`_.

Most of string completion code worked out of the box in Python 3 - I only realized that the norm had changed when I had curly braces "**{}**" in my strings. It turns out that curly braces have a special meaning in Python 3 strings - they are placeholders, in addition to the % sign. The format goes something like this:

.. code-block:: python

    In [4]: "my string {:d}".format(1)
    Out[4]: 'my string 1'

However, the braces themselves need to be encapsulated in a second set of braces to be printed. So, for example:

.. code-block:: python

    In [5]: "my string {{{:d}}}".format(1)
    Out[5]: 'my string {1}'

In brief, the braces outside the number placeholder :code:`{:d}` have to be encapsulated in a second (or third, depending on how you look at it) set of braces :)

.. _2to3: https://docs.python.org/2/library/2to3.html

.. _details: https://docs.python.org/2/library/string.html#format-string-syntax
