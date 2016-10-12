Dictionaryconverter
===================

This ``python3`` script turns ``dictionaries/<somename>.definition.json`` and
``dictionaries/<somename>.translation.json`` into gettext(1) .po-files, one per
language. By default, it operates on the dictionaries in the base system. To
convert and merge the dictionaries in a module, use the ``-m <modulename>``
flag.

Copy the script into the same directory that houses the ``dictionaries`` and
``modules`` directories and run it from there.

The default filename for the .po-file in base is ``messages.po``, while the
default for a module is ``modulename.po``. This can be overridden with the
``-D <domainname>`` flag.

The command ``merge`` merges all dictionaries in a directory into one .po-file,
while the command ``convert`` converts a single dictionary. The command
``extract`` can copy out one or more tags from a dictionary into a file
``extracted.po`` if you need to move some tags from one domain to another.

Also included is a makefile that will convert all the dictionaries included
with the SimpleSAMLphp source. One for all base dictionaries, one each for all
modules.

If there already exists a .po-file with the same name at the same location, the
file will be updated, not overwritten.

Run it with the ``-h`` flag for more options.
