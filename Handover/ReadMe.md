### What it does
* Single click automatic handover: start the script during your last song and the handover is automatically handled
* Countdown (3min, 2min, 1min, 30seconds, 15seconds) is automatically put into the DJ channel, synced to time remaining in SAM
* Changes to your normal nick at 30 seconds to go
* Wakes the DJ up by name in the DJ channel (so it highlights on their screen)
* Stops the encoder and tells the next DJ to go
* Syncs to SAM - no need to do any timing or thinking yourself
* Copes when SAM fast forwards time randomly
* Did I mention it's fully automatic? :)

### What you'll need
* SAM Broadcaster (Tested on SAM Version 4.2.2 and SAM Pro Version 2020.5)
* ADI IRC (Tested on 3.9) running on the same PC as SAM  (It definitely won't fully work with mIrc)

### Download SAM PAL script
* In SAM: go to Help->About and make a note of your SAM version number
* SAM Version eg 4.2.2
* * https://raw.githubusercontent.com/Mat1971/IRCScripts/main/Handover/Handover.PAL
* * Right click the link ^^ and Save Link As...
* * Put it with your other PAL scripts in SAM, for example C:\Program Files (x86)\SpacialAudio\SAMBC\PAL
* * If you can't save it there, save to eg Documents and copy it over to C:\Program Files (x86)\SpacialAudio\SAMBC\PAL
* SAM Version eg 2020.5
* * Right click the link ^^ and Save Link As... to C:\Users\YourWindowsName\AppData\Local\SpacialAudio\SAMBC\PAL
* (If you don't want to follow these links you can put on your tinfoil hat and open the files above and copy/paste them to the files manually)

### Download ADI script + config
* https://raw.githubusercontent.com/Mat1971/IRCScripts/main/Handover/AdiSamLink.ini
* Right click the above link ^^ and Save Link As... to eg C:\Users\YourWindowsName\AppData\Local\AdiIRC\Scripts

### Installation
* Load into SAM
* * In SAM:
* * Menu -> Window -> Pal Scripts (this should be ticked to bring up the PAL Scripts box)
* * In the PAL Scripts window, click the "+" and select Handover.PAL from the folder you downloaded it to
* * DO NO SELECT "Automatically Start Script" !
* Load into ADI
* * In ADIIrc: ALT-R      (or menu bar, Tools -> Edit Scripts)
* * File->Load and load AdiSamkLink.ini
* * This will give a script warning about initialization commands, click "OK"

### Configuration
* There is no configuration, everything is automated for you.
* At 30 seconds it will change back to your default nick, this can be changed in ADIIrc: ALT-O (for options) => QuickConnect => Nick

### Testing
* Make sure you're connected to the DJ server and are in the DJ channel
* Type into any window in ADI:  /TestSamLink 
* If this prints a message in the DJ channel, the ADI end of this script is working and ready to receive the countdown from SAM

### Limitations
* You can stop the countdown by stopping the script in SAM, but (at least in v4.2.2) you can't restart it without restarting SAM

### Usage
* Obviously you have to in the DJ channel for the script to work, but you'll be there anyway
* * Optional: Test the script works by typing /TestSamLink into any ADI IRC window
* When your final song starts
* * Find your PalScripts window in SAM
* * Find Handover.PAL and left-click to select it
* * Click the play ( ![Play](https://github.com/Mat1971/IRCScripts/blob/main/Handover/ScriptPlayV4.png?raw=true) or ![Play](https://github.com/Mat1971/IRCScripts/blob/main/Handover/ScriptPlayV2020.png?raw=true) ) button in the PAL scripts window to start the selected script

This will print a message in the DJ channel with the remaining song time left.  If this works everything else will be done for you: countdown, nick change, encoder stop, etc.

### Upgrading to a new version
* Close ADI and SAM
* Download the scripts, replacing the existing versions
* Reload ADI and SAM and you're good to go

### TODO
* add in make it turn requests off?
