Documentation
=============

.. HINT::
   Most of the documentation is present in the :doc:`examples` page. Here are technical specificities that are not trivial to understand with examples.



Input
-----

Showchord is a command line tool to produce piano chord representations.

The input is one or more lists of notes (forming a chord) and an optional title. The separator between the note list and the title is the semicolon character: ``;``

::

    showchord 'C E G' 'C E G;C major chord'

Refere to :ref:`examples-basic` for basic examples.

There are typically two ways to input chords.

* Directly as arguments, you can provide as many chords as you like
* From an input stream

    * from a file using system redirection

    ::

        showchord < chordlist.csv

    * from a pipe if your system provides this functionnality

    ::

        cat chordlist.csv | showchord

Note that it is possible to produce the picture of an empty 2 scales keyboard by providing an empty string as chord input (see the first basic example in :ref:`examples-basic`).


Options
-------

keyprint
''''''''

The ``--keyprint`` (short: ``-k``) switches the printing of the notes below the keyboard.


fileprefix
''''''''''

zoom
''''

export
''''''
