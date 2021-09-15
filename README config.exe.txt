This config.exe is a graphical interface (GUI) for Minidlna Dlna Server, Windows (cygwin) version, for basic settings of
minidlna.conf file.

Compatible only with https://sourceforge.net/projects/minidlna-win/

At first run, a ffmpeg.ini is created with default values. To adjust settings, edit ffmpeg lines with "edit ffmpeg options" button,
click save. For desktop streaming,  adjust the name of video capture filter (ffmpeg -list_devices true -f dshow -i dummy > output.txt 2>&1, 
check output.txt for the alternative name of the filter).
Click "save".

A config.ini is created with default values for start of minidlnad.exe (minidlnad.exe -R -f minidlna.conf, edit if necessary).

Click "save" button to create a  minidlna.conf with new settings, clik "start" to run minidlnad.exe.

Save button:
-minidlna.conf (minidlna configuration file) is renamed to minidlna.conf.bkp (if an old minidlna.conf.bkp exist will be deleted).
-a new minidlna.conf is created.         
============================================