MINIDLNA SUBTITLES CONVERTER

-Conv.exe is a small utility (CLI) to convert subtitles in the minidlna FORCETRANSCODE directory, changing encoding to UTF-8, compatible
with ffmpeg.exe burned subtitles.

-Usage: conv.exe -f cp1252 -y -d c:\FORCETRANSCODE
a)-f cp1252 is the codepage of the input subtitles (cp1252 is European/Latin characters). For a list of codepages run iconv.exe -l
b)-y not create bkp files. If omitted, original subtitles will be renamed to .srt.bkp. Use with caution.
c)-d c:\FORCETRANSCODE is the path to FORCETRANSCODE dir, is the minidlna dir for transcoding. 

-Subtitles with utf-8 or utf-16 (unicode) encoding are not converted (utf-8 and utf-16 are compatible with fffmpeg.exe)

-conv.exe uses iconv.exe (https://www.cygwin.com/packages/x86_64/libiconv/libiconv-1.17-1) and uchardet.exe
(https://github.com/JetDemo/uchardet/blob/master/bin/uchardet.exe) for detection and conversion of srt subtitles.

RUN:
-example of usage: create a .bat (any name) to run conv.exe before minidlna GUI and create a shortcut for .bat file.
init.bat:
C:\dir of minidlna\conv.exe -f cp1252 -d e:\forcetranscode
"C:\dir of minidlna\Minidlna GUI v1.1.exe"  


ERRORS:
-subtitles converted with wrong characters: maybe wrong codepage, for a list of codepages run iconv.exe -l
-msg invalid dir/path: check path/dir of FORCETRANSCODE  folder.
-msg conversion error: maybe wrong codepage, for a list of codepages run iconv.exe -l
