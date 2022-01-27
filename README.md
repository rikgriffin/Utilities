# Utilities
Utilities required for other builds

This repo contains a few minor utility programs that are required to build stuff in other repos,
namely the Tabs and TreeView gadget modules.

rm : A very simple BASIC program that emulates the Unix/Linux rm command

trim : Another simple BASIC program that snips the tail end of Makefiles.

Bin2C : A utility written in C that produces a C array definition based on the contents of a binary file.
This is used in the build process of Tabs and TreeView, to embed a Sprite area in the modules' data.

Size: Another tiny utility that simply prints a file's size to stdout. Used in the process of embedding a
sprite file into a compiled program, as the Sprite file doesn't contain its own size.
