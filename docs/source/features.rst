Features
========

List
----

* Draw an empty 88 or 24 keys piano keyboard - eventually with a title - SVG output format
* Draw any chord you can imagine (on a full sized keyboard) by giving note names. The chord is represented by round marks on the keys
* Print a title above the keyboard, whether chord notes are provided or not
* Print note names below the marked keys
* Export to bitmap (PNG) file (by default, resulting is stored in SVG files)
* Force output filename prefix
* Provide zoom value to change the drawing size
* Generate many chords at once from informations taken from a stream.

  * Stream from musicxml file or simple specific csv-like file.

Motivation
----------

As you play keyboard by auto-learning and do not have enough music theory skills to read scores, you may need to draw chord as marks on a keyboard to see how to play it. As I once was talking to a friend about piano chord positions, I could not find any program to help me generate these little piano chord pictures to make a quick document as chord reminder. This is the reason why I wrote showchord. Showchord is a program that renders chord drawings as SVG and PNG images. As an example of use, I made this trivial triads.pdf_ document to help my friend visualize and memorize very basic chords.

.. _triads.pdf: _static/examples/triads.pdf

The idea behind showchord is to be able to automate piano chord drawings from few informations: the notes of the chords. I hope showchord could be useful to others. You can use it to write a piano method for example. Please let me know if you use it and tell me if you find it easy (or not) to use. Do not hesitate to ask me features you may need, I would be happy to make showchord to be a useful tool.

Developpement
-------------

Showchord was first written in shell (bash) but I found very difficult to describe note structure clearly with shell. This is the main reason why I decided to switch to python as it provides rich types.

I also choosed python among other languages to learn it. Because of the learning process, the program code changes a lot from one release to the other. However, the fonctionnalities either stay unchanged or grow, depending on the ideas I have. Sometime options change. If you get use to showchord in a given version please read the doc carefully to check if the options are still the same before you switch to the next release. This "big changes" process should progressively disappear as I get to know python better.

My ultimate goal is to make showchord a usable tool in Linux CLI point of view, to make it possible to write scripts generating documents with chord representations. I also want to keep programing style as clear as possible to make code evolutions easy.

Dependencies
------------

#. Python modules (mandatory)

   - os
   - sys
   - subprocess
   - argparse
   - xml.etree.ElementTree
   - collections (namedtuple)

#. External programs (optional, only required for bitmap export)

   - Inkscape_ is needed to transform SVG to PNG with --export option
   - If you are running Linux and do not want to install Inkscape, then consider using librsvg_ instead, for exporting (rsvg-export command line tool)

.. _Inkscape: https://inkscape.org/

.. _librsvg: https://wiki.gnome.org/Projects/LibRsvg

