# RT Training App Beta

This public repository is intended to keep track of bugs and issues for the RT app.  
Click the "Watch" button above to receive updates whenever there are any changes.

👉 [Click here](https://github.com/jensbouma/RT-issuetracker/issues) to view known issues.  
👉 [Submit new issues](https://github.com/jensbouma/RT-issuetracker/issues/new) about the beta version.

## Changes 6-1-2021 (Actual version)
- Implemented double login detection and automatic disconnect on the first device.
- Improved connection establishment, with automatic reconnection after connection drop and retry loop for unsuccessful connections.

## Changes 5-1-2021
- Removed club name from the status bar.
- Forced student login with URL add-on.
- Made small layout updates.
- Improved connected user counter.
- Fixed the registration loop issue.

## Changes 4-1-2021
- Implemented loading user details from the Moodle API.
- Added a group selector when the user is in multiple groups.
- Enabled default registration for first login.
- Restricted video resolution to 640x360 with 20 frames/s.
- Enhanced input boxes with a modern look.

## Changes 16-12-2020 
- Improved count for connected stations.
- Made improvements for video requests from the trainer panel.
- Automatically closed windows after request.
- Showed the "Request video" button only when the video is not yet connected.
- Removed the video element when the client disconnects.

## 14-12-2020
- Enabled trainers to request video camera access from students for exams.
- The "Request video" button is hidden until audio is connected and can be found by clicking the user row.
- Students receive a pop-up to accept the video request.
- Once accepted, a draggable and scalable video element opens on the trainer panel.

## 26-11-2020
- Implemented better signaling and status light indicators for trainers and users.
- Initialized the data channel directly on load.
- Initialized WebRTC after starting audio.
- Changed the party that requests the stream.
- Added a delay in giving the stream after channel opening (possibly fixing an iOS audio problem).
- Improved logging.
- Removed RX end delay, as it caused more issues than it solved.
- Automatically retry connecting if the data channel is open.

## 23-11-2020
- Bugfix for RTC socket, resulting in better connection stability.
- Added connection status indicators in the user list and trainer panel.
- Mic indicates audio to other stations, Speaker indicates audio from other stations, Plane indicates data connection. Green color indicates an established connection, while Red indicates no connection.
- The RX status in the trainer panel turns off 0.5s after transmitting.

## 21-11-2020 
- The RX status per user remains on while transmitting.
- Made the Frequency and Squawk switch stay highlighted longer.
- Enabled clicking rows for user options: temporary hide user, delete user from the database, and make notes attached to a user.
- Initialized the data channel directly on load instead of after pressing the connect button.
- Added a loading screen for a smoother page load.
- The trainer panel no longer uses XML but updates with WebSocket data and initializes directly from the database.
- User updates no longer require an XML refresh.
- Added PHP server time instead of XML time.
- Bugfix: Prevented freezing of the PTT button after clicking away from the user screen.
- Simplified code for creating the user table in the trainer panel.
- Converted lowercase registrations to uppercase.
- Fixed the issue where changing the registration frequency, squawk, or status would reset other values.

##

 19-11-2020
- Implemented a push-to-talk (PTT) button that only releases on mouseup.
- Set the PTT button as the default selected button after releasing another button to prevent frequency switching while transmitting with a key.
- Added functionality to the audio level meter.
- Changed the "Activate Mic" text to "Connect".

## 16-11-2020
- Added Moodle Connector.
- Introduced group support (one group per trainer, with later support for base group channels).
- Integrated instructor panel with audio support.
- Loaded the instructor panel using JSON instead of XML (XML removal in later versions).
- Added more dynamics to the hash for loading different user roles.

## 06-11-2020:
- Implemented WebRTC data channel using a public server.
- Enabled peer-to-peer audio chat over WebRTC data channel.
- WebRTC Statistics: chrome://webrtc-internals/
- Tested in Chrome, iOS, and Android (Chrome).
- Checked and started the Node server when offline.

## 03-11-2020:
Transponder:
- Optimized the Squawk code input to allow only values from 0000 to 7777.
- Automatically converted input values like 17 to 0017.
- Turned off the transponder with an input value of -1.

Radio:
- Added a microphone level meter (non-functional yet).
- Assigned a key to the PTT button by holding down the key and simultaneously pressing the PTT button with the mouse.
- Optimized the frequency input, automatically converting values like 1225 to 122.500.

Chat:
- Implemented RX/TX data communication.
- Added sound effects (SFX) to simulate PTT press and release.
- Displayed a list of actual connected users.
- Showed the user name of the transmitter in the radio (student) panel (note: please confirm if this is a desired feature).

Functionality:
- Implemented a unique hash as a cookie.
- Added a cookie version for safe upgrading to newer versions.
- Enhanced security in the database, using the hash as a unique ID and optimizing JavaScript.
- Implemented JSON instead of XML.
- Removed XML for user load.
- Optimized the WebKit Audio API.
- Performed major code cleanup, separating code into modules.
- Added online/offline status to the database, with write to the database on shutdown.
- Provided pop-up instructions on what to do when the user blocks audio permission.

Trainer Panel (/trainer):
- Added user status in the trainer panel (note: offline status may not yet work with disconnecting users on iOS devices).
