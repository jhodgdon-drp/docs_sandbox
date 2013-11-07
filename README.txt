INTRODUCTION
------------

This project will eventually hold some AsciiDoc-formatted documentation on
Drupal Core APIs. At the moment, it just has a small amount of the intended
documentation.

There is a style guide in the appendix.txt file (formatted in AsciiDoc).

DISPLAYING
----------

If you have the AsciiDoc and DocBook tools installed, you can make this
documentation into a PDF, HTML, or other types of output by running the
following commands:

mkdir output
a2x -d book -f pdf -D output drupalbook.txt
a2x -d book -f chunked -D output drupalbook.txt

You can install these tools from a Linux command line as follows:

apt-get install asciidoc docbook
yum install asciidoc docbook

For Windows installation instructions and more information, see:

http://asciidoc.org
http://docbook.org

If you would like to display this documentation in a Drupal site, or want to
make nicer output, check out this project:
  https://drupal.org/sandbox/jhodgdon/2127337
(with short name asciidoc_display).
