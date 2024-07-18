# Conky-Automatik-Nvidia-and-AMD-Radeon
This is a copy from https://www.gnome-look.org/p/1170490 I try to correct problems with ***Beta version for AutomatiK_nvidia_beta. *** 
I tried to install Automatik, and it didn't work, I downloaded the .taz file and unzipped it but I also found problems to use it besides warnings and errors in the sh, so I will try to correct them to be able to use it.

![image](https://github.com/user-attachments/assets/3ddc1343-5c24-47a7-a804-0fadd9cbbe38)

Here are some of the errors I found
~/conky-themes/conky_start.sh
conky: no process found
Process Successfully terminated
Process Successfully terminated
/AutomatiK/clock.py:28: DeprecationWarning: 'locale.getdefaultlocale' is deprecated and slated for removal in Python 3.15. Use setlocale(), getencoding() and getlocale() instead.
  locale.setlocale(locale.LC_TIME, locale=locale.getdefaultlocale())
/home/gabemdelc/conky-themes/AutomatiK/cpu.py:17: SyntaxWarning: invalid escape sequence '\+'
  TemperatureSensor="sensors | grep -E 'Package id 0|Physical id 0|Tctl|temp1' | sed -e 's/([^()]*)//g' |  grep -oP '\+(\d+\.\d+)°C' | sort -n | tail -n 1"
Traceback (most recent call last):
  File "/usr/bin/lsb_release", line 25, in <module>
    import lsb_release
ModuleNotFoundError: No module named 'lsb_release'
docker0   no wireless extensions.

eno1      no wireless extensions.

/AutomatiK/display.py:75: SyntaxWarning: invalid escape sequence '\:'
  Monitors_Detected=os.popen("cat /var/log/Xorg.0.log | grep -E -i -w connected | tail -10 |  cut -c 19- | sort | uniq | grep -oP '^[^\:]*\: \K[^\:]+' | sed 's/[(][^)]*[)]//g'").read().lstrip().rstrip().split('\n')
/AutomatiK/display.py:142: SyntaxWarning: invalid escape sequence '\|'
  GPU_maker=os.popen("lspci | grep -i 'vga\|3d\|2d'").read().rstrip().split('\n')[0]
/bin/sh: 1: inxi: not found
Traceback (most recent call last):
  File "/AutomatiK/display.py", line 51, in <module>
    Graphic_server_installed = Inxi_Search("Display:",Total_Clean)[0]
                               ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^
IndexError: list index out of range

