# XInputDemo
Using XInput APIs for Gamepad Input in twinBASIC

XInput is a very simple API to use, but since I've never seen VBx/twinBASIC code for it before, I thought I'd post a quick demo. This covers all the basic gamepad features, including getting battery info (Win10+) and making the controller vibrate.

![XIDemo](https://github.com/user-attachments/assets/f7064142-7e62-457d-9701-994eb6376efe)

Requires Windows Development Library for twinBASIC.

Windows 7 and Vista are supported even though they use a different DLL for the APIs than our primary defs point to for Win8+; WinDevLib implements this by providing API aliases, e.g. `XInputGetState7`.

Note if using this in your own code, `XInputGetBatteryInformation` has an incorrect `[TypeHint()]` in current WDL versions (9.3.676 and earlier); it will be fixed next update but until then just make sure to use the right constants.
