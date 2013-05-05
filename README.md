qotd-viewer
===========

A GUI application that can view the quote of the day from quote of the day servers

Building The QOTD-VIEWER UNIX Executable Using The Standalone Makefile
======================================================================

To build a UNIX executable that does not require python to execute, we use Freeze. On Ubuntu, you can obtain Freeze by installing the package 'python-2.7-examples'.

If you want to find the path of freeze.py on Ubuntu (or Debian), run:

$ dpkg -S freeze.py

On my system, this outputs:

	python2.7-examples: /usr/share/doc/python2.7/examples/Tools/freeze/makefreeze.py
	python2.7-examples: /usr/share/doc/python2.7/examples/Tools/freeze/freeze.py

In this case, the path to freeze.py is the second option (/usr/share/doc/python2.7/examples/Tools/freeze/freeze.py). 


1. Change into the directory of the qotd-viewer sources.
2. Run the command: make -f Standalone FREEZE=/path/to/freeze.py
3. When all that is finished change into the 'standalone' directory. There should be a file called 'qotdinterface' among all the c and object files. That is the standalone executable.
4. Should you want to clean out this directory for another build, just run make -f Standalone clean