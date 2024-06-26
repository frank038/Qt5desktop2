# Qt5desktop2
A desktop and panel all in one application for Xorg. Free to use and modify.

Download in the Release page.

This is a single application that integrates a desktop and a panel. It's an union of my SimpleDesktop and Qt5simpledock programs, which are obsolete now (and has the same features, plus others).

Features added:
- can store and manage the notifications (with my program qt5notification, experimental version), if enabled: an icon will appear at the right side of the bar; just click it to show a dialog; the disable button means 'do not disturb mode'; clickable links in the notification body as option to be enabled;
- webcam indicator: an a little grayed out icon appears if a webcam is attached; the icon changes as soon as the webcam turns in a working state (and viceversa);
- battery indicator: the icon shows approximately the remaining power; the tooltip show the percentage of the remaining power and its state;
- empty trashcan sound (to be enabled in the config file);
- the scripts can be enabled/disabled by using the context menu on the bar, using the right mouse button: Reload scripts (no needs to close and launch this program again); after a modification in their parameters, the scripts must be disabled and enabled again in the config file.

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


Desktop:

This program shows the content of the folder "Desktop". The name can be changed in the config file.

To open the recycle bin, the command have to be written in the file trash_command.sh. Make sure to make this file executable. Must be executable also the files qt5desktop.py and qt5desktop.sh. Both can be used to launch this program. qt5desktop.sh is raccomanded.

The recycle bin icon can change to reflect its state, empty or not empty.

Can handle desktop files (programs, directories and files as link) [to be revisited]. Using desktop files for folders and files don't let user manage directly them. Moreover, more files and folders with the same name can coexist at the same time. Actually they can be created with my programs SimpleFM and this one (from the menu). Accept files from my Qt5archiver program.

Wallpaper: just put an image named wallpaper (jpg or png) in the main directory of this program; it can be changed while this program is been executing by the action in the menu "Update wallpaper".

Limitations: only one item at time can change its position on the desktop. The desktop files cannot be copied, they can only be created and deleted.

Panel:
- three layouts: traditional; all elements centered; menu - application launcher - taskbar: centered
- application menu (can add or modify application entries; bookmarks; search functionality; pin to bar)
- clock/calendar (can read an ics file; can launch an external program for adding/modifying events by double clicking in a day cell, or even event)
- virtual desktops (if supported by the window manager)
- application launchers (using the contextual menu, applications can be pinned and unpinned - pinned from the menu, unpinned from the button launcher)
- task list with icon support and application comment while hovering on it
- four slots for periodical custom messagges (just modify the files in the script folder; they accept both plain text or rich text; see the sample files); can execute programs double clicking with the left mouse button or the middle mouse button them.
- two slots for custom widgets in the dock, left and right
- systemtray icons support
- integrated clipboard (text and images)
- closing applications by right mouse clicking on its icon
- closing and restarting this program by right mouse clicking (for special purpose)
- can play sounds when a window opens or closes
- experimental, initial support for audio: the main volume can be changed; left mouse click to show a popup; central mouse click to toggle mute/unmute; if a microphone is enabled, an icon is shown (its name will be shown in the tooltip); these options must be enabled in the config file;
- experimental support for battery
- experimental support for webcams: check the status (only) connected, or in use (the icon changes depending on its status); filters for unwanted webcams to be checked
- customizations in the cfg_dock file.
