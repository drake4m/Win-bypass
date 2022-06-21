

RunWithoutElevation v1.00
Copyright (c) 2019 Nir Sofer
Web site: http://www.nirsoft.net



Description
===========

RunWithoutElevation is very simple command-line tool that runs a program
requires elevation (run as Administrator) without elevation.
For example, you can run the RegEdit tool of Windows without elevation:
RunWithoutElevation.exe regedit.exe

RegEdit in this mode still works properly, but you can only modify the
Registry keys of HKEY_CURRENT_USER.

You can also import .reg files with HKEY_CURRENT_USER keys, for example:
RunWithoutElevation.exe regedit.exe c:\temp\myreg.reg

There are also some NirSoft tools that require elevation, but you can
still use them without elevation in read-only mode.
For example, you can use DevManView to export the devices list without
running it as Administrator:
RunWithoutElevation.exe DevManView.exe /scomma "c:\temp\devices.txt"



Using RunWithoutElevation in shortcuts
======================================

If you want to create a shortcut that runs a program without elevation,
simply create the shortcut to the program, and then insert the full path
of RunWithoutElevation.exe into the 'Target' field, preceding the path of
the program you want to run.



How it's done ?
===============

This tool simply set the __COMPAT_LAYER environment variable to
RunAsInvoker (Only for the running process).



Feedback
========

If you have any problem, suggestion, comment, or you found a bug in my
utility, you can send a message to support@nirsoft.net
