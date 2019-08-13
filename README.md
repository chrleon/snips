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

For extra ease, make an alias in bash profile.
1. Open Terminal, type 
```nano  ~/.bash_profile```
1. Add a line like so
```alias restartwacom="kill -s HUP '`pgrep WacomTabletDriver`'"```
1. Restart the terminal and type ```restartwacom``` to restart the Wacom Drivers.
1. Swing that pen
