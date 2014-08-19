Basic System Administration Commands
---

###System info
- `uname` Print OS name
- `uname -a` Print OS name with all options (-mrsvn)
- `uname -r` Show kernal version
- `uname -m` Show architecture of machine
- `arch` Show architecture of machine
- `uptime` Show how long system has been running
- `cat /proc/cpuinfo` Show CPU info


###List Devices
- `lspci -tv` List PCI devices - *ls* for List, *pci* for PCI devices. `-t` for Tree view, and `-v` for Verbose.
- `lsusb -tv` List USB devices 


###Disk Space
- `df -h` Show list of partitions mounted with used and available space.
- `du -hs` Show disk space used in a human readable (-h) and summarized (-s) form.
- `du -hs dir1` Show disk space used by directory *dir1*.
- `du -ha` Show disk space used by all files in the current directory.
- `du -sk * | sort -rn` Show size of files and directories sorted by size

###Shutdown, Restart, Logout
- `logout` Logout
- `reboot` Reboot / Restart
- `init 0` Shutdown
- `telinit 0` Shutdown
- `shutdown -h now` Shutdown system. `now` means do it right away. `-h` is for halt i presume.
- `shutdown -h 16:30 &` Planned shutdown of system at 2:30pm.
- `shutdown -c` Cancel a planned shutdown
- `shutdown -r now` Reboot now


###Calendar, Date and Time
- `date` Show system date
- `date 041217002007.00` Set system date - Month*Day*Hours*Minutes*Year.Seconds
- `cal` Show calendar for the current month
- `cal 2014` Show calendar for the year 2014
- `cal june 2090` Show calendar for June 2090


Notes
---
- Getting help is as simple as adding the `--help` flag after the command.