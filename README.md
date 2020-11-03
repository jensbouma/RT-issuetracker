# RT Training App Beta

This public repository is intended to keep track of bugs and issues for the RT app.<br>
'Watch' this repository to get updates when something changed.

<a href="https://github.com/jensbouma/RT-issuetracker/issues" target="_blank">Here</a> you can find the know issues.<br>
Submit new issues about the beta version <a href="https://github.com/jensbouma/RT-issuetracker/issues/new" target="_blank">here</a>

The old version can be found on https://rt.knvvl.nl<br>
The newer beta version can be found on https://dev.jensbouma.com/beta<br>

# New in the beta version (03-11-2020):
Transponder:
- Squawk code input is optimised, its now only possible to enter 0000 to 7777
- A Squawk input of 17 for example automatically turns into 0017
- Transponder turns 'off' with a input value of '-1'

Radio:
- Microphone level meter microphone (No functional yet)
- A key can be assigned to the PTT button by holding down the key and simultaneously pressing the PTT button with the mouse.
- Frequency input is optimised. 1225 for example automatically turns into 122.500

Chat:
- RX/TX data communication is implemented (no audio carrier yet)
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
