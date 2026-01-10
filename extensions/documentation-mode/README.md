# What do I want to make out of documentation-mode?

every extension/major mode in Lem should have some sort of README.md or otherwise standardized documentation format.

I would like documentation-mode to work like GNU texinfo.  Perhaps what I want is a GNU texinfo for every mode, and a 
way to automatically generate texinfo from the source code.  I would also like the source code to be linked in the info pages.
That may not be entirely necessary though, because you could just use describe-symbol on the text in the info page.

I wonder how easily markdown can be converted to texinfo.  I also wonder if we even need texinfo, could Lem instead use markdown for all documentation?
Documentation could be generated for every mode from:

1. README.md
2. function/symbol documentation

There could also be a notes facility to ease creating documentation.  Whenever documentation for a symbol is requested, in the documenation popup there
could be a button that opens a markdown buffer for documenting the symbol.

It could even be a requirement at some point that all functions have a doc-string as part of the github CI process.

# Desired behavior
Whenever `C-h i` is pressed, a read-only buffer is opened with links to all the major modes, minor modes, and also lem-core.
following these links will bring up respective documentation.

Markdown buffers could generated on the fly and include links/buttons for traveling through the hierarchy (as in texinfo mode)

# TODO

- [ ] index all major modes, all minor modes
- [ ] index all symbols within modes
- [ ] create function to generate documentation buffers for modes
- [ ] ability to export buffers to markdown file (potential for caching? creating a manual?)