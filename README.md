# RT Training App Beta

This public repository is intended to keep track of bugs and issues for the RT app.<br>
'Watch' this repository to get updates when something changed.

<a href="https://github.com/jensbouma/RT-issuetracker/issues" target="_blank">Here</a> you can find know issues.<br>
Submit new issues about the beta version <a href="https://github.com/jensbouma/RT-issuetracker/issues/new" target="_blank">here</a>.

The old version can be found on https://rt.knvvl.nl.<br>
The newer beta version can be found on https://dev.jensbouma.com/beta.<br>
# Changes 19-11-2020
- PTT button function, only releases on mouseup
- PTT button got default selected after releasing another button to prevent frequency switching while transmitting
- Audio level meter has function now (not on ios yet)
- Activate Mic text changed to Connect to Group

# 16-11-2020
- Moodle Connector
- Group support (1 group per trainer, later also basegroup channel)
- Integrated instructor panel with audio support
- XML > JSON > Load instructor pannel (XML remove in later version)
- Added more dynamics to hash for loading different user roles

# 06-11-2020:
- WebRTC data channel implemented (using public server)
- Peer to Peer audio chat over WebRTC datachannel
- WebRTC Statistics: chrome://webrtc-internals/
- Tested in Chrome, iOS, Android (Chrome)
- Node server check and start when offline.

# 03-11-2020:
Transponder:
- Squawk code input is optimised, its now only possible to enter 0000 to 7777
- A Squawk input of 17 for example automatically turns into 0017
- Transponder turns 'off' with a input value of '-1'

Radio:
- Microphone level meter microphone (No functional yet)
- A key can be assigned to the PTT button by holding down the key and simultaneously pressing the PTT button with the mouse.
- Frequency input is optimised. 1225 for example automatically turns into 122.500

Chat:
- RX/TX data communication is implemented
- SFX added to simulate PTT press and release
- List of actual users connected to
- Radio shows User Name of transmitter (not sure this is a wanted feature in the student panel)

Functionality:
- Cookie is now a unique hash
- Cookie version for safe upgrading to newer versions
- DB: security added, hash as unique ID and JS optimisation
- Implementation of JSON instead of XML
- Removed XML for UserLoad
- WebKit Audio API Optimalisation
- Major JavaScript code cleanup and written to separate modules
- Add online/offline status to database (with write to db on shutdown)
- Pop-up instructions what to do, when user blocked audio permission.

Trainer Panel (/trainer):
- Added user status in trainer pannel (buggy: offline status doesn't work yet with disconnecting users on iOS devices)
