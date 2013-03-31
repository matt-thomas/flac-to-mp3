flac-to-mp3
===========

I wanted a simple utility that takes a directory that contains flac
files and converts them to mp3s in that same directory. I borrowed
heavily from [shentonfreude's utility](https://github.com/shentonfreude/flac-to-mp3/)
in creating this tool.

Usage
=====

Specify source and destination directories and optional bitrate::

  ./flac-to-mp3.py /PATH/TO/FILES BITRATE

For example:

  ./flac-to-mp3.py ~/music/artist/album 64

The default bitrate is 320 Kbps.

Requirements
============

The script is in Python and it uses the binaries:

 * `flac`: decode flac files
 * `lame`: encode mp3 file
 * `mutagen`: used for pulling metadata from flac file like Artist, Album, Title
 * `id3v2`: save metadata to mp3 file