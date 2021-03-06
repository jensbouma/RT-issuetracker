# RT Training App Beta

This public repository is intended to keep track of bugs and issues for the RT app.<br>
'Watch' this repository to get updates when something changed.

<a href="https://github.com/jensbouma/RT-issuetracker/issues" target="_blank">Here</a> you can find know issues.<br>
Submit new issues about the beta version <a href="https://github.com/jensbouma/RT-issuetracker/issues/new" target="_blank">here</a>.
# Changes 6-1-2021 (Actual version)
- Double login detection and automatic disconnect on first device.
- better connection making, automatic reconnect after connection drop and try loop when connection is not working in the first time.

# Changes 5-1-2021
- Removed clubname in statusbar
- Force student login with url add-on
- Small layout updates
- Connected usercounter much better
- Entering registration isnt a loop anymore

# Changes 4-1-2021
- Loading Userdetails from moodleAPI now
- Groupselector when user is in multiple groups
- Default registration for first login
- Only login from moodle (no manual login anymore)
- Videoresolution limited to 640*360 with 20 frames/s
- Fancier inputboxes.


# Changes 16-12-2020 
- Better count for connected stations.
- Improvements for video request from trainer pannel.
- Windows closes autoomaticly after request.
- Button only shows when video not connected yet.
- Removing videoelement when client disconnects.

# 14-12-2020
- Trainer can now request videocamera from the student for exams.
- The 'Request video' button is hidden until audio is connected and can be found by clicking the user-row.
- Student gets a pop-up to accept the video request.
- when accepted by the student a dragable and scalable (right border) videoelement opens on trainer panel.

# 26-11-2020
- Better signaling and status light indicators for trainer and users.
- Data channel gets initalised directy on load.
- WebRTC gets initalised after starting audio.
- Stream gets requested now by connecting party.
- Delay on giving stream after channel opening (iOS audio problem fix?).
- Better logging
- RX end delay removed as it breaks more than it fixes
- Automaticly retry to connect if data channel is open

# 23-11-2020
- Bugfix RTC socket > Better connection stability.
- Connection status indicators in userlist and trainerpanel.
- Mic = audio to other station, Speaker = Audio from other station, Plane = Data connection. Green = Established Red = No connection
- RX status trainerspannel goes off 0,5s after transmitting.

# 21-11-2020 
- RX status per user stays on while transmitting
- Freq. and Squawk switch now stays highlighted longer
- Rows can be cliked for useroptions: Temporaly hide user, Delete user from database and make a note attached to a user.
- Datachannel now initalise directly on load instead after pressing connect button
- Loading screen for nicer page load.
- Trainerpannel doesnt use XML anymore, updates with Websocket data and first initalization direct form DB
- User updates doesn't do a XML refresh, because its not needed anymore
- PHP servertime added instead of XML time.
- Bugfix: Freezing PTT button after clicking away userscreen.
- Simpler code to make usertable in trainerpanel
- A lowercase registration gets converted to upercase now.
- When changeing te registration frequency, squawk and status doesn't get resetted anymore.

# 19-11-2020
- PTT button function, only releases on mouseup
- PTT button got default selected after releasing another button to prevent frequency switching while transmitting with key
- Audio level meter has function now
- Activate Mic text changed to "Connect"

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
