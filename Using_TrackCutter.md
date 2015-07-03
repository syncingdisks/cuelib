# Using TrackCutter #

This page will help you to get started with TrackCutter.

## What can I do with TrackCutter? ##

You can use TrackCutter to create files containing individual tracks based on the information in a cue sheet. It can also do some audio format conversions and it has powerful post-processing functionality.

To give an example: I decided that I wanted high quality ([lossless](http://en.wikipedia.org/wiki/Lossless_data_compression)) digital copies of my audio CDs, so I ripped my collection with [Exact Audio Copy](http://www.exactaudiocopy.de/) to an uncompressed WAVE file with a cue sheet. (You can do this with EAC shortcut ALT-F7). This produces a single wav file per CD. The cue sheet tells my [music player](http://www.foobar2000.org/) where each track starts, what its title is, what its track number is, etc. This information can't be included in the wav file itself; we really need the combination of both wav file and cue file.

Unfortunately, my iPod doesn't support cue files. Besides, it doesn't have enough disk space for my complete CD collection in wav format. I need to turn these wav and cue files into mp3 files, such that each track of each CD becomes a single mp3 file with the correct title, track number, artist, album name, etc.

My music player can do these conversions for me, but I need to open each cue sheet, start the conversion, wait for it to finish, and then go to the next cue sheet. That's too much work, especially since I'll have to do it all over again if I later decide that I want to convert to mp3's with a higher bitrate, or to a different format such as [ogg vorbis](http://www.vorbis.com/). I want to script this conversion action, so the computer can do the boring work for me. TrackCutter allows me to do this.

## How do I use TrackCutter? ##

There are two ways to use TrackCutter. We will discuss these in the next sections.

### Using TrackCutter in java code ###

You can use the `TrackCutter` class in your java code. If you want to do this, you will probably want to take a look at the javadocs of the `jwbroek.cuelib.tools.trackcutter` package. If you want sample code, then you can take a look at the source code of the `TrackCutterCommand` class. Both javadocs and source code can be found in the [Downloads](http://code.google.com/p/cuelib/downloads/list) section. The source code can also be found in our [svn repository](http://code.google.com/p/cuelib/source/browse).

### Using TrackCutter from the command line ###

You can also use TrackCutter from the command line. The entry point for this is the `TrackCutterCommand` class. To call this class, use the following command from the directory containing the cuelib jar file. (In this example we use `cuelib-1.1.1-2008-04-13.jar`, but any version from 1.1.0 onward should work.)

`java` `-cp` `cuelib-1.1.1-2008-04-13.jar` `jwbroek.cuelib.tools.trackcutter.TrackCutterCommand`

This command will tell you that you didn't provide the correct command line arguments, and will tell you what arguments are available.

The most basic use case is to create wav files for all tracks in the cue sheet. To do this for the cue sheet `c:\rips\Skunk Anansie - Stoosh.cue`, use this command:

`java` `-cp` `cuelib-1.1.1-2008-04-13.jar` `jwbroek.cuelib.tools.trackcutter.TrackCutterCommand` `"c:\rips\Skunk Anansie - Stoosh.cue"`

You can process multiple cue sheets at once. Just list each one in succession. For instance:

`java` `-cp` `cuelib-1.1.1-2008-04-13.jar` `jwbroek.cuelib.tools.trackcutter.TrackCutterCommand` `"c:\rips\Skunk Anansie - Stoosh.cue"` `"c:\rips\Apocalyptica - Apocalyptica.cue"`