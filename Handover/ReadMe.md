# TODO rewrite history

### What it does
* Single click automatic handover: start the script during your last song and the handover is automatically handled
* Countdown (3min, 2min, 1min, 30seconds, 15seconds) is automatically put into the DJ channel
* Changes to your normal nick at 30 seconds to go
* Wakes the DJ up by name in the DJ channel if they go to sleep
* Stops the encoder and tells the next DJ to go at the same time
* Syncs to SAM - no need to do any timing or thinking yourself
* Copes when SAM fast forwards time randomly
* Did I mention it's fully automatic? :)

### What you'll need
* SAM Broadcaster (Tested on v4.2.2)  Coming soon: testing on Pro 2020.5
* ADI IRC (Tested on 3.9) (there's a 5% chance it will work on mIrc) running on the same PC as SAM

### Download SAM PAL script
* Right click the link and save as...
* https://raw.githubusercontent.com/Mat1971/IRCScripts/main/Handover/Handover.PAL
* Put it with your other PAL scripts in SAM, for example C:\Program Files (x86)\SpacialAudio\SAMBC\PAL
* (If you don't want to follow the link you can click the files above and copy/paste into a file manually)

### Download ADI script + config
* https://raw.githubusercontent.com/Mat1971/IRCScripts/main/Handover/AdiSamLink.ini
* https://raw.githubusercontent.com/Mat1971/IRCScripts/main/Handover/AdiSamConfig.ini
* Right click the above links and save as...


### TODO
Use a hashcode to avoid config of server/channel
   go through servers
   hash channel name [to lower, acc += (char-64) * n;]
   return server+channel
version [mention version in countdown/handover!) [combine sam + irc version)
self test should show version
testing
instructions

### Installation
* Load into SAM
** In SAM:
** Menu -> Window -> Pal Scripts (this should be ticked to bring up the PAL Scripts box)
** In the PAL Scripts window, click the "+" and select the file (do NOT select "Automatically Start Script")
* Load into ADI
** This will give a script warning about initialization commands, click "OK"
** (The initialisation sets up the listener itself, will not work without this!)
* DO THE CONFIGURATION STEP BELOW

### Configuration
* You need to tell the script your nickname, the server and DJ channel (Ask Mat for details if you can't figure this out yourself)
* Edit ...... Alt-R......* 
* MyNick : change this to your usual nick
* MyNetwork: change this to the single word descriptor of the server (eg efnet, undernet, whatever the server is)
* MyChannel: this is the name of the DJ channel.  If you don't know this, you shouldn't be using this script :)
* Save........

### Testing in ADI
* Make sure you're in the DJ server and DJ channel
* Type this into any window in ADI /test......
* If this prints a message in the DJ channel, the ADI end of this script is working

### Limitations
* You can stop the countdown by stopping the script in SAM, but (at least in v4.2.2) you can't restart it without restarting SAM

### Usage

You have to be on the DJ server for the script to work
Starting the SAM script:

At the start of the final song: Click Sam->Window->Pal Scipts

Select AutoCountdown.PAL

Click the |> play button above the script

;Testing the IRC end
;     This script automatically starts and Should Just Work.
;     Testing the IRC end:
;            Make sure you are in the DJ channel
;            if using Mat's RMD Script there is a Test Sam Listener button
;                 or use /TestSamListener
;                 or test with a webbrowser on same machine:   http://127.0.0.1:50501/message?time=999&data=This+is+a+test+message+from+browser
;            if all is working, you will see a test message to the DJ channel
