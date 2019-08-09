# snips
Stuff I'd like to log for later. Terminal commands, code snippets etc.

## Restart the Wacom driver on MacOS without rebooting
HUP is the HANGUP signal and by convention, daemons and drivers reload themselves.
Open terminal and enter the following command
``` 
kill -s HUP "`pgrep WacomTabletDriver`"
```
