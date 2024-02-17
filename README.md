# SetThreadExecutionState-for-Reaper
DONT go to sleep and/or turn off the display while reaper is playing/recording.


This script for Reaper calls SetThreadExecutionState(ES_DISPLAY_REQUIRED), repeatedly if reaper is in either 

-Playback
-Pause 
-Recording

This is, as far as i understand, the same way mediaplayers and browsers do it when the pc shouldnt go to sleep.  

# Installation is a bit hacky: 

- first you need to install reapy-boost
- https://github.com/Levitanus/reapy-boost
- 

- now activate reapy-boost by calling reapy-boost.configure_reaper() from inside reaper (just use a dummy .py file and import as action)
- this only needs to be done once per installation and never again after that
- 

- you also need to install SWS extension for reaper from here:
- https://www.sws-extension.org/
- SWS extension can run scripts on reaper startup
- 

- finally save my script to a .py file and import it with reapers action list as a new action.
- copy the command/action ID and paste it into SWS -> startup actions -> global startup actions
- the script should now run on reaper startup


