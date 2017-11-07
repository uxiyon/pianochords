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

The format is ``N .. N;Chord title`` where ``N`` is a note, and ``Chord title`` is a string.

A note is: 

* a pitch step noted in german style, so it must be one of {A, B, C, D, E, F G}
* followed by an optional *accidental*, one of {``#``, ``b``, ``x``, ``bb``}
* followed by an optional *octave* value, one of {0 .. 8}

.. topic:: Accidentals

    ``#``: sharp (dièze)

    ``b``: flat (bémol)

    ``x``: double # (x <=> ##)

    ``bb``: double flat


* From an input stream

    * from a file using system redirection

    ::

        showchord < chordlist.csv

    ::

        showchord < musicxml_partition.xml


    * from a pipe if your system provides this functionnality

    ::

        cat chordlist.csv | showchord

.. note:: It is possible to produce the picture of an empty 2 scales keyboard by providing an empty string as chord input (see the first basic example in :ref:`examples-basic`).




Options
-------

keyprint
''''''''

The ``--keyprint`` (short: ``-k``) switches the printing of the notes below the keyboard.


fileprefix
''''''''''

The ``--fileprefix`` (short: ``-f``) option is used to set the begining of generated SVG file names. The default prefix is ``chord_``, thus without ``-f`` option, all output files are named ``chord_<somename>_N.svg`` where ``<somename>`` depends on the chord title and where ``N`` is an integer to disinguish two similar named files.

zoom
''''

The ``--zoom`` (short: ``-z``) option set the zoom factor of the output image. The value is a float number (e.g 2.45), but an integer is allowed (e.g 5)


export
''''''

The ``--export`` (short: ``-e``) switches the generation of bitmap PNG images. This option requires that either ``inkscape`` or ``rsvg-convert`` is installed the system that runs showchord.

.. warning:: This option may overload your system if many chords are provided (ex. from a large musicxlm partition)

