# Minidlna-For-Windows-with-Transcoding
This Minidlna For Windows with Transcoding is a clone of Minidlna cygwin version (https://github.com/Portisch/minidlna-compile)  
with following changes, the main goal is on the fly transcoding with resume when
transcoding is stopped (crashes, TV power off or other situations), and a transcoding
fully configurable (resize filter, subtitles burning and others ffmpeg commands).

This mod version is the only dlna server compatible with my Samsung F8000 TV for on the fly transcoded movies, with subtitles, pause and seek.
  

binaries at:https://mega.nz/file/dEEVjCwJ#1sEw2_C7B_L5FOYqHy6nAaxitJ0cfS6hiR4UMx2JvAA
(read included README.txt for instructions).Download ffmpeg.exe from https://www.gyan.dev/ffmpeg/builds/ or  https://github.com/BtbN/FFmpeg-Builds/releases (full build).



Changes:
-added transcoding with seek to simulate fast forward and rewind (ff/rw) when transcoding.
 A directory named Seek with icons "Play To" at a configurable interval in minutes is created
 (Seek directory includes subfolders with movie name).

-enabled pause button in some devices like Samsung F8000 (fixed value for DLNA_ORG flags).
 
-subtitles burning (mandatory when using Seek functions with subtitles) with font color and font size settings.

-only ffmpeg.exe is used for transcoding, encoding with hardware acceleration for AMD VCE, Intel QSV an Nvidia Nvenc is supported. 

-resize filter, solves incompatibility with somes devices not accepting vertical resolution not multiple of 24 (modulus 24)
like Samsung F8000 (movies with resolution of 1900x784 display "invalid file").

-a very simple windows gui to start/stop minidlna (minigui.exe).
-------------------

-this version include patches:
transcode patch:
https://sourceforge.net/p/minidlna/patches/32/
https://bitbucket.org/stativ/readymedia-transcode/src/transcode/

samsung mta patch:
https://sourceforge.net/p/minidlna/patches/14/

subtitles patch.
https://sourceforge.net/p/minidlna/patches/155/

----------------------------------------------
To compile:

-Install cygwin 32 bits.
 Follow instructions at https://github.com/Portisch/minidlna-compile.
 
  
    
