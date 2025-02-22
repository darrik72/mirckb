/background
===========

The **/background** command is used to change the background picture setting for a specific window including a channel window. This is the same as changing the background via the system window (to access the system menu simply right click the small window icon located on the upper left corner of the window).

Synopsis
--------

.. code:: text

	/background -abemsgdluhcfnrtpx [window] [filename]

Switches
--------

.. list-table::
	:widths: 15 85
	:header-rows: 1

	* - Switch
	  - Description
	* - -e
	  - set as default
	* - -x
	  - no background picture

Window Switches
~~~~~~~~~~~~~~~

.. list-table::
	:widths: 15 85
	:header-rows: 1

	* - Switch
	  - Description
	* - -a
	  - active window
	* - -m
	  - main mIRC window
	* - -s
	  - status window
	* - -g
	  - finger window
	* - -d
	  - single message window

Picture Switches
~~~~~~~~~~~~~~~~

.. list-table::
	:widths: 15 85
	:header-rows: 1

	* - Switch
	  - Description
	* - -c
	  - center
	* - -f
	  - fill
	* - -n
	  - normal
	* - -r
	  - stretch
	* - -t
	  - tile
	* - -p
	  - photo

Bars Switches
~~~~~~~~~~~~~

.. list-table::
	:widths: 15 85
	:header-rows: 1

	* - Switch
	  - Description
	* - -l
	  - toolbar
	* - -u
	  - toolbar buttons
	* - -h
	  - switchbar
	* - -b
	  - treebar

Parameters
----------

.. list-table::
	:widths: 15 85
	:header-rows: 1

	* - Parameter
	  - Description
	* - [window]
	  - A window name should only used if no window switches were specified.
	* - [filename]
	  - The filename of the picture to be used (The filename must be enclosed by a pair of double quotes if it contains spaces).

Example
-------


.. code:: text

	;Setting one of window vista's sample pictures as the background for the active window
	;Since the filename's path contain spaces it must be enclosed by a pair of double quotes
	/background -a "C:\Users\Public\Pictures\Sample Pictures\Desert Landscape.jpg\"

	;Remove the background picture from the active window
	/background -xa

Compatibility
-------------

Added: mIRC v5.4 (23 Jun 1998)

.. note:: Unless otherwise stated, this was the date of original functionality. Further enhancements may have been made in later versions.

See also
--------

.. hlist::
	:columns: 4

	* :doc:`$toolbar </aliases/toolbar>`
	* :doc:`$color </aliases/color>`
	* :doc:`$treebar </aliases/treebar>`
	* :doc:`$menubar </aliases/menubar>`
	* :doc:`$switchbar </aliases/switchbar>`
	* :doc:`/color <color>`
	* :doc:`/menubar <menubar>`
	* :doc:`/switchbar <switchbar>`
	* :doc:`/toolbar <toolbar>`
	* :doc:`/treebar <treebar>`