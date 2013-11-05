INTRODUCTION
------------

This project will eventually hold some AsciiDoc-formatted documentation on
Drupal Core APIs. At the moment, it just has a small amount of the intended
documentation.

See also project:
  https://drupal.org/sandbox/jhodgdon/2127337
(with short name asciidoc_display) which is for displaying AsciiDoc in Drupal.
It also has help on installing the AsciiDoc tool chain, making PDFs, etc.

MAKING A PDF
------------

To compile the documentation book into a PDF file, if you have the AsciiDoc tool
chain installed (see the AsciiDoc Display project for how to do that):

a2x -d book -f pdf drupalbook.txt

This will result in a drupalbook.pdf file containing the entire book.
