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
* ADI IRC (there's a 5% chance it will work on mIrc)

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
version
testing
instructions

### Installation



;Starting the SAM script:
;     At the start of the final song:  Click Sam->Window->Pal Scipts
;                                   Select AutoCountdown.PAL
;                                   Click the |> play button above the script
;     There will be a message giving the starting time remaining (eg "4:33 to go before handover");
;     After that messages happen at 3:00   2:00   1:00   0:30   0:15  and  Go Go Go
;     Change to normal nick happens at 0:30
;     Encoders automatically stopped
;
;Testing the IRC end
;     This script automatically starts and Should Just Work.
;     Testing the IRC end:
;            Make sure you are in the DJ channel
;            if using Mat's RMD Script there is a Test Sam Listener button
;                 or use /TestSamListener
;                 or test with a webbrowser on same machine:   http://127.0.0.1:50501/message?time=999&data=This+is+a+test+message+from+browser
;            if all is working, you will see a test message to the DJ channel
;
;Testing the SAM end
;     TRICKY!
;     Stop button is horrible (at least in Sam 4.2.2) - if you use the stop button it will not start again! (at least in 4.2.2)
;     Can I run script twice?
;




### Usage
