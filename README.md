# DuckKeyhook Reloaded
# All credit goes to Cosmodium for making the [original version of this software](https://github.com/CosmodiumCS/payloads/tree/main/rubberducky/DucKeyhook).
**Please follow his tutorial on that, most of the code is the same, just a few things are updated:**
- Fixed webhook encoding error ("empty message") with some additional headers.
- Fixed webhook message scheduling (before, it was only running at the start of a system - at least for me - because the `c.cmd` file was starting the `p.ps1` script and then blocking at recording keystrokes, so it couldn't run the `l.ps1` script which was responsible for scheduling. Now it doesn't start the `p.ps1` itself, but the `l.ps1` which then starts `p.ps1`).
- Optimised delays in DuckyScript file, so it doesn't type too fast and miss some characters.
- Added "code highlighting" to webhook messages, just to make it easier to read.
- Added IP display in the name of the webhook using [Ipify API](https://api.ipify.org/)
# To-Do:
- Add Windows 11/Windows Terminal App support, now `c.cmd` file runs in the terminal app, which minimises instead of hiding completely, then a user can just close the terminal app window and interrupt keylogger processes.
