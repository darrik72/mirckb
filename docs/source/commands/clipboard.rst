/clipboard
==========

The **/clipboard** command copies text to the clipboard.

Synopsis
--------

.. code:: text

    /clipboard [-an] [text]

Switches
--------

.. list-table::
    :widths: 15 85
    :header-rows: 1

    * - Switch
      - Description
    * - -a
      - Appends text to the end of the current clipboard's contents
    * - -n
      - Appends a $crlf to the end of the text

.. note:: Presence or absence of a single trailing $crlf does not affect the lines count of $cb(0)

Parameters
----------

.. list-table::
    :widths: 15 85
    :header-rows: 1

    * - Parameter
      - Description
    * - [text]
      - Text to be placed in clipboard. If no text parameter used, the clipboard is cleared.

Example
-------

.. code:: text

    ;Clear the clipboard and put \"Hello world!\" in it
    /clipboard Hello World!

    ;Put 'abcd' into clipboard then append efgh and carriage return:
    //clipboard abcd | clipboard -an efgh | echo -a $cb(0).len / $cb(1).len / $cb(1)
    ;returns: 10 / 8 / abcdefgh
    ;(The difference between length of $cb(0) and $cb(1) is the $crlf.

    ;Clear clipboard contents:
    /clipboard

    ;Append $crlf to end of current clipboard contents:
    /clipboard -an

Compatibility
-------------

Added: mIRC v5.1 (28 Aug 1997)

.. note:: Unless otherwise stated, this was the date of original functionality. Further enhancements may have been made in later versions.

See also
--------

.. hlist::
    :columns: 4

    * :doc:`$cb </aliases/cb>`
    * :doc:`$inpaste </aliases/inpaste>`
