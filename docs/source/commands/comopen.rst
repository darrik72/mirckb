/comopen
========

The **/comopen** command opens a COM connection to specified programmatic identifier with the assigned name. Your script should check **$comerr** after opening the connection to make sure the connection was established successfully.

Synopsis
--------

.. code:: text

    /comopen <name> <progid>

Switches
--------

None

Parameters
----------

.. list-table::
    :widths: 15 85
    :header-rows: 1

    * - Parameter
      - Description
    * - <name>
      - Connection name to be used 
    * - <progid>
      - Programmatic Identifier 

Example
-------

.. code:: text

    Alias Example {
      ;Create a WshShell object 
      comopen Example wscript.shell

      ;Destroy object
      comclose Example
    }

.. code:: text

    ; see more documentation at: https://msdn.microsoft.com/en-us/library/system.windows.forms.sendkeys(v=vs.110).aspx
    ; and be careful about mIRC interpreting % & and other special characters
    //sendkeys {ESC}%o{END}{UP 2}%bText In mIRC Titlebar+{TAB}{ENTER}
    alias sendkeys {
      ; trying to create unique WshShell object
      var %name sendkeys $+ $ticks $+ $rand(111,9999)
      .comopen %name WScript.Shell
      if (!$comerr) {
        var %result $com(%name,SendKeys,3,bstr,$1-)
        ;Destroy object when finished with it
        .comclose %name
        return %result
      }
      return 0
    }

Compatibility
-------------

Added: mIRC v5.9 (26 Apr 2001)

.. note:: Unless otherwise stated, this was the date of original functionality. Further enhancements may have been made in later versions.

See also
--------

.. hlist::
    :columns: 4

    * :doc:`$com </aliases/com>`
    * :doc:`$comcall </aliases/comcall>`
    * :doc:`$comval </aliases/comval>`
    * :doc:`$comerr </aliases/comerr>`
    * :doc:`/comclose <comclose>`
    * :doc:`/comreg <comreg>`
    * :doc:`/comlist <comlist>`