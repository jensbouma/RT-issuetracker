# RT Training App Beta

This public repository is to keep track of bugs and issues for the RT app.

The main version can be found on https://rt.knvvl.nl
The beta version can be fount on https://dev.jensbouma.com/beta

# New in the beta version (03-11-2020:
Transponder:
- Squawk code input is optimalised, its now only posible to enter 0000 to 7777
- A Squawk input of 17 for example automaticly turns into 0017
- Transponder turns 'off' with a input value of '-1'

Radio:
- Microphone levelmeter microphone (No funtional yet)
- A key can be assined to the PTT button by holding down the key and simultaneously pressing the PTT button with the mouse.
- Freqency input is optimalised. 1225 for example automaticly turns into 122.500

Chat:
- RX/TX data communication is implemented (no audio carrier yet)
- SFX added to simulate PTT press and release.
- Radio shows User Name of transmitter (not sure this is a wanted feature in the student panel)

Functionality:
- Cookie is now a unique hash
- Cookie version for safe upgrading to newer versions
- DB hash as unique ID and JS optimalisation
- Implementation of JSON instead of XML
- Removed XML for UserLoad
- WebKit Audio API Optimalisation
- Major JavaScript code cleanup and written to seperate modules
- Add online/offline status to database (with write to db on shutdown)
- Pop-up instructions what to do, when user blocked audio permission.

Trainer Pannel:
- Added user status in trainer pannel (buggy: offline status doesn't work yet with disconnecting users on iOS devices)
