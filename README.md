# snips
Stuff I'd like to log for later. Terminal commands, code snippets etc.

## Restart the Wacom driver on MacOS without rebooting
HUP is the HANGUP signal and by convention, daemons and drivers reload themselves.  
Open terminal and enter the following command
``` 
kill -s HUP "`pgrep WacomTabletDriver`"
```

You can also do it manually with Activity Monitor.  
Search for 'Wacom' and quit it. It will restart.

If it doesn't, you'll find the driver in /Library/Application\ Support/Tablet/WacomTabletDriver.app/Contents/MacOS.
