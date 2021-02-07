Pandoc Man
==========

Creating Linux Man pages using Pandoc.

Install Pandoc
::

	sudo apt install pandoc

Create and empty file named program_name.1.md and add the header.

testproj.1.md
::

	%TESTPROJ(1) Test Project Man Page
	%John Doe
	%Feburary 7, 2021


Sections start with # and end with a blank line.

Conventional section names include NAME, SYNOPSIS,  CONFIGURATION,
DESCRIPTION,  OPTIONS, EXIT STATUS,  RETURN VALUE,  ERRORS,
ENVIRONMENT,  FILES, VERSIONS, CONFORMING TO, NOTES, BUGS, EXAMPLE,
AUTHORS, and SEE ALSO.

Adding to our man page a couple of sections.

testproj.1.md
::

	%TESTPROJ(1) Test Project Man Page
	%John Doe
	%Feburary 7, 2021
	
	# NAME
	Test Project - Man page test
	
	# DESCRIPTION
	How to create a man page using Pandoc Man
	
	# BUGS
	None
	
	#AUTHORS
	John Doe and Jane Doe


To create the man file from the markdown file use the following syntax
::

	pandoc name.md --standalone --write FORMAT --output FILE

This can be shorten to
::

	pandoc name.md -s -w FORMAT -o FILE

So our example we will use
::

	pandoc testproj.1.md -s -w man -o testproj.1
