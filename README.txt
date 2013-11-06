INTRODUCTION
------------

This project will eventually hold some AsciiDoc-formatted documentation on
Drupal Core APIs. At the moment, it just has a small amount of the intended
documentation.

See also project:
  https://drupal.org/sandbox/jhodgdon/2127337
(with short name asciidoc_display) which is for displaying AsciiDoc in Drupal.
It also has help on installing the AsciiDoc tool chain, making PDFs, etc.

FORMATTING AND STYLE GUIDE
--------------------------

Documentation here should be formatted using AsciiDoc: http://asciidoc.org
The AsciiDoc user guide at http://asciidoc.org/userguide.html explains the
markup syntax.

A few notes on syntax that are specific to Drupal Core documentation follow.

Chapters and Sections:

  We are using the alternate syntax for chapters/sections, and we strongly
  suggest each chapter and section be given an identifier. So:

  = Overall Book Title

  [[first_chapter_id]]
  == Chapter Title One

  [[first_section_id]]
  === Section Title Sub 1
  etc.

  You can then make a link to a different chapter or section by putting
  <<the_id>>
  into your text.

  Each chapter should be in a separate file; sections can be in the same file or
  separate files. Chapters are things like "Configuration API" and sections
  roughly correspond to drupal.org book pages within each chapter. On
  api.drupal.org, each section will be displayed on its own page.

Code:

  To include PHP code:

  [source,php]
  ----
  $x = foo();
  ----

Versions:

  This repository will be branched for new versions of Drupal. So, do not
  specifically use the version number in your writing, except in the top-level
  title, and in specific sections about updating from one version to another.
  The hope is that when we branch to the next version, we should just be able
  to delete the version-specific updating sections, change the main title in
  one place, and be done.

Literals:

  File names and directories in text should be formatted with _ like:
    _core/modules/system/system.module_
  Function and class names in text should be formatted with + like:
    +my_function_name()+

DISPLAYING
----------

Use project asciidoc_display to display this documentation within a Drupal site.

To compile the documentation book into a PDF file, if you have the AsciiDoc tool
chain installed (see project asciidoc_display for how to do that):
  a2x -d book -f pdf drupalbook.txt
This will result in a drupalbook.pdf file containing the entire book. However,
you will get better results if you convert to DocBook first and then PDF:
  asciidoc -d book -b docbook -o output/drupalbook.docbook drupalbook.txt
  xmlto -o output --with-fop pdf output/drupalbook.docbook

The asciidoc_display project has some style sheets that you may find useful.
