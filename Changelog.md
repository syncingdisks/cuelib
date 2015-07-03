# Cuelib changelog and roadmap #

## 1.2.1 ##
_2008-06-13_
  * Cuelib is Java 5 compatible again. ([Issue 19](https://code.google.com/p/cuelib/issues/detail?id=19).)

## 1.2.0 ##
_2008-05-21_
  * Documentation comes with an XML Schema for the output of CueSheetToXmlSerializer. ([Issue 1](https://code.google.com/p/cuelib/issues/detail?id=1).)
  * The documentation comes with an XSLT stylesheet that can convert the output of CueSheetToXmlSerializer back into a regular cue sheet. ([Issue 3](https://code.google.com/p/cuelib/issues/detail?id=3).) This effectively means that you can use all your XML tooling to edit cue sheets, by using cuelib to turn your cue sheets into XML, editing this XML and then using the cuelib XSLT to turn the XML back into a cue sheet.
  * TrackCutterCommand has greatly improved file selection. Can now recurse though subdirectories up to a specified depth (which may be infinite), select files using a regular expression, and use configurable base directories. ([Issue 2](https://code.google.com/p/cuelib/issues/detail?id=2).)
  * TrackCutterCommand will now print progress information to stderr. It has options to customize this behaviour. ([Issue 5](https://code.google.com/p/cuelib/issues/detail?id=5).)
  * Cuelib now comes with JDK 1.4 logging facilities. ([Issue 7](https://code.google.com/p/cuelib/issues/detail?id=7).)
  * TrackCutterCommand can now read a cue sheet from standard input. ([Issue 4](https://code.google.com/p/cuelib/issues/detail?id=4).)
  * The documentation has been improved. ([Issue 15](https://code.google.com/p/cuelib/issues/detail?id=15).)

## 1.1.1 ##
_2008-04-13_
  * TrackCutter tool now has an option to disregard pregaps with length below some threshold.
  * Minor correction in TrackCutterCommand help message.
  * TrackCutterCommand now has an explicit "help" option.
#### Links ####
  * [Binaries](http://cuelib.googlecode.com/files/cuelib-1.1.1-2008-04-13.jar)
  * [Documentation](http://cuelib.googlecode.com/files/cuelib-docs-1.1.1-2008-04-13.zip)
  * [Source](http://cuelib.googlecode.com/files/cuelib-src-1.1.1-2008-04-13.zip)
  * [SVN](http://cuelib.googlecode.com/svn/tags/1.1.1/)

## 1.1.0 ##
_2008-04-12_
  * Added a TrackCutter command line tool that can create individual tracks based on the information in a cue sheet. Includes support for post-processing (for instance, by encoding with LAME), tracks hidden in pregaps, basic audio format conversions.
  * Added a serializer that writes to XML.
  * Added a convenient method for getting various metadata from cue sheets.
**Note: cue sheet data structure is slightly incompatible with 1.0.0, due to different constructors.**
#### Links ####
  * [Binaries](http://cuelib.googlecode.com/files/cuelib-1.1.0-2008-04-12.jar)
  * [Documentation](http://cuelib.googlecode.com/files/cuelib-docs-1.1.0-2008-04-12.zip)
  * [Source](http://cuelib.googlecode.com/files/cuelib-src-1.1.0-2008-04-12.zip)
  * [SVN](http://cuelib.googlecode.com/svn/tags/1.1.0/)

## 1.0.0 ##
_2008-02-11_
  * Initial release. Includes data structures for an internal representation of cue sheets, a parser, and a serializer.
#### Links ####
  * [Binaries](http://cuelib.googlecode.com/files/cuelib-1.0-2008-02-11.jar)
  * [Documentation](http://cuelib.googlecode.com/files/cuelib-docs-1.0.0-2008-02-12.zip)
  * [Source](http://cuelib.googlecode.com/files/cuelib-src-1.0.0-2008-02-12.zip)
  * [SVN](http://cuelib.googlecode.com/svn/tags/1.0.0/)