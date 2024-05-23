# Qt5desktop2
A desktop and panel all in one application for Xorg. Free to use and modify.

This is a single application that integrates a desktop and a panel. It's an union of my SimpleDesktop and Qt5simpledock programs (and has the same features).

Added feature: can store and manage the notifications (with my program qt5notification, experimental version), if enabled: a gray icon will appear at the right of the bar, and just click on it to show a dialog; the disable button means 'do not disturb'. 

Personalizations in the config files, mainly:
- cfg_qt5desktop.py
- cfg_dock.py

Configured for Openbox (just for the logout command).

Required:
- python3
- pyqt5
- python3-xdg

For mass storage devices (option):
- udisk2
- dbus
- pyudev
- notify-send (optional for desktop notification after a device has been inserted and/or ejected)

For custom actions (option):
- 7z
- tar
- zip
- md5sum - sha256sum
- xterm

For thumbnailers (option):
- pdftocairo
- ffmpegthumbnailer

For webcam:
- pyudev
- lsof (command line program)
- pyinotify

Features:

Desktop:

This program shows the content of the folder "Desktop". The name can be changed in the config file.

To open the recycle bin, the command have to be written in the file trash_command.sh. Make sure to make this file executable. Must be executable also the files qt5desktop.py and qt5desktop.sh. Both can be used to launch this program. qt5desktop.sh is raccomanded.

The recycle bin icon can change to reflect its state, empty or not empty.

Can handle desktop files (programs, directories and files as link) [to be revisited]. Using desktop files for folders and files don't let user manage directly them. Moreover, more files and folders with the same name can coexist at the same time. Actually they can be created with my programs SimpleFM and qt5simplebar. Actually only programs. Accept files from my Qt5archiver program.

Wallpaper: just put an image named wallpaper (jpg or png) in the main directory of this program; it can be changed while this program is been executing by an action in the menu.

Limitations: only one item at time can change its position on the desktop. The desktop files cannot be copied, they can only be created and deleted.

Panel:
- three layouts: traditional; all element centered; menu - application launcher - taskbar: centered;
- application menu (can add or modify application entries; bookmarks; search functionality)
- clock/calendar (can read an ics file; can launch an external program for adding/modifying events by double clicking in a day cell, or even event)
- virtual desktops (if supported by the window manager)
- application launchers (using the contextual menu, applications can be pinned and unpinned - a valid desktop file is required; the file delete_me in the folder 'applications' needs to be deleted before using this program)
- task list with icon support and application comment while hovering on it
- four slots for periodical custom messagges (just modify the files in the script folder; they accept both plain text or rich text; see the sample files); can execute programs double clicking with the left mouse button or the middle mouse button.
- two slots for custom widgets in the dock, left and right
- systemtray icons support
- integrated clipboard (text and images)
- closing applications by right mouse clicking on its icon
- closing and restarting this program by right mouse clicking
- can play sounds when a window opens or closes
- experimental, initial support for audio: the main volume can be changed; left mouse click to show a popup; central mouse click to toggle mute/unmute; if a microphone is enabled, an icon is shown (its name will be shown in the tooltip); these options must be enabled in the config file;
- experimental support for battery
- experimental support for webcams: check the status (only) connected, or in use (the icon changes depending on its status); filters for unwanted webcams to be checked
- customizations in the cfg_dock file.
