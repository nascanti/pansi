=====
Pansi
=====

Pansi is a clean and simple ANSI escape code library for Python.

The library provides an object called ``ansi`` through which all escape codes can be selected.
This object exposes the codes as both attributes (e.g. ``ansi.red``) and items (e.g. ``ansi['red']``),
and is most easily used with `f-strings <https://peps.python.org/pep-0498/>`_:

.. image :: art/hello-rainbow.png


Colours
=======

For foreground text, the standard set of colours can be selected using the lower case name for normal brightness
and the upper case name for high intensity.
To select as the background colour instead, simply prefix with ``bg.``, e.g. ``bg.blue``.

=====================  ===========  ==============
Colour                 Foreground   Background
=====================  ===========  ==============
|K0| Black             ``black``    ``bg.black``
|R0| Red               ``red``      ``bg.red``
|G0| Green             ``green``    ``bg.green``
|Y0| Yellow            ``yellow``   ``bg.yellow``
|B0| Blue              ``blue``     ``bg.yellow``
|M0| Magenta           ``magenta``  ``bg.magenta``
|C0| Cyan              ``cyan``     ``bg.cyan``
|W0| White             ``white``    ``bg.white``
|K1| Bright black      ``BLACK``    ``bg.BLACK``
|R1| Bright red        ``RED``      ``bg.RED``
|G1| Bright green      ``GREEN``    ``bg.GREEN``
|Y1| Bright yellow     ``YELLOW``   ``bg.YELLOW``
|B1| Bright blue       ``BLUE``     ``bg.YELLOW``
|M1| Bright magenta    ``MAGENTA``  ``bg.MAGENTA``
|C1| Bright cyan       ``CYAN``     ``bg.CYAN``
|W1| Bright white      ``WHITE``    ``bg.WHITE``
=====================  ===========  ==============

.. |K0| image:: https://via.placeholder.com/12.png/000/000
.. |R0| image:: https://via.placeholder.com/12.png/a00/a00
.. |G0| image:: https://via.placeholder.com/12.png/0a0/0a0
.. |Y0| image:: https://via.placeholder.com/12.png/a50/a50
.. |B0| image:: https://via.placeholder.com/12.png/00a/00a
.. |M0| image:: https://via.placeholder.com/12.png/a0a/a0a
.. |C0| image:: https://via.placeholder.com/12.png/0aa/0aa
.. |W0| image:: https://via.placeholder.com/12.png/aaa/aaa
.. |K1| image:: https://via.placeholder.com/12.png/555/555
.. |R1| image:: https://via.placeholder.com/12.png/f55/f55
.. |G1| image:: https://via.placeholder.com/12.png/5f5/5f5
.. |Y1| image:: https://via.placeholder.com/12.png/ff5/ff5
.. |B1| image:: https://via.placeholder.com/12.png/55f/55f
.. |M1| image:: https://via.placeholder.com/12.png/f5f/f5f
.. |C1| image:: https://via.placeholder.com/12.png/5ff/5ff
.. |W1| image:: https://via.placeholder.com/12.png/fff/fff

Full 24-bit colour support is also available (on those terminals that support it) by using the ``rgb`` selector.

.. image :: art/rgb-orange.png

Foreground and background colours can be inverted and then set back to normal using the ``rev`` and ``_rev`` tags respectively.

To reset foreground and background back to their defaults, use ``fg.reset`` and ``bg.reset``.


Text Weight
===========
- ``weight.normal``
- ``weight.bold``
- ``weight.light``
- ``b`` (alias for ``weight.bold``)
- ``_b`` (alias for ``weight.normal``)


Text Style
==========
- ``style.normal``
- ``style.italic``
- ``style.fraktur``
- ``i`` (alias for ``style.italic``)
- ``_i`` (alias for ``style.normal``)


Text decoration
===============
- ``u`` (underline)
- ``uu`` (double underline)
- ``_u`` (no underline)
- ``o`` (overline)
- ``_o`` (no overline)
- ``s`` (strike through)
- ``_s`` (no strike through)


Blinking
========
- ``blink`` (blink)
- ``BLINK`` (blink fast)
- ``_blink`` (no blink)


Hide & show
===========
- ``hide``
- ``show``
