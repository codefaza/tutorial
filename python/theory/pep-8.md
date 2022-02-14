# PEP-8

PEP 8, sometimes spelled PEP8 or PEP-8, is a document that provides guidelines and best practices on how to write Python code. 
It was written in 2001 by Guido van Rossum, Barry Warsaw, and Nick Coghlan. The primary focus of PEP 8 is to improve the readability and consistency of Python code.

PEP stands for Python Enhancement Proposal, and there are several of them. 
A PEP is a document that describes new features proposed for Python and documents aspects of Python, like design and style, for the community.

**Quote:**

**“Explicit is better than implicit.”**

**— The Zen of Python**

## Links:

1. https://realpython.com/python-pep8/


## Questions:

1. Why does PEP8 recommend leaving a blank line at the end of a .py file?

They assume that every line ends with a line terminator (\n). A text file is a collection of lines, a line is a series of characters followed by a \n. A file that does not end with a \n is a file that has a last line that is incomplete.

For example, if you concatenate two files, and the first file is not properly terminated, then the last line of the first file and the first line of the second file will end up forming a single line in the result.

2. I have 2 modules into the same dir and I want to import one into another. I can run the script and use the imported module,
but the IDE doesn't seem to see the module ('no module named ..message') and the autocomplete can't see the funcs inside it?

In PyCharm's Project tool window, right-click on the directory and select Mark Directory As -> Sources Root.