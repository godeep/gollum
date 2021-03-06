Runlength
=========

This formatter prepends the length of the message as "number:" to the message.
Note that "number" is the actual ASCII representation of a number, not a binary representation.
The length stored does not contain the length of the generated prefix.
This formatter allows a nested formatter to modify the message before calculating the length.

Parameters
----------

**RunlengthFormatter**
  Defines an additional formatter applied before calculating the length. :doc:`Format.Forward </formatters/forward>` by default.

Example
-------

.. code-block:: yaml

  - "stream.Broadcast":
    Formatter: "format.Runlength"
    RunlengthFormatter: "format.Forward"
