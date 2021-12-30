# Huion Kamvas Pro 24

This EDID fixes the scaling issues you might notice in graphic design programs on Windows (only tried on 10 so far) for the Huion Kamvas Pro 24. 

## How to use

To install, simply download [`huion-kamvas-pro-24.reg`](huion-kamvas-pro-24.reg) and right-click -> **Merge**. Feel free to look at the .reg (or .txt) before merging to verify that this will be installed at the correct location (`HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Enum\DISPLAY\HAT2380\5&44f2e74&0&UID4354\Device Parameters` on my machine).

Once you've merged it, you can press Ctrl+Win+Shift+B to restart the graphics driver (you'll hear a beep), at which point, when you re-open your programs, the scaling will be correct.

## Additional details

This was created using [the generic process I outline here](https://github.com/jackhumbert/massdrop-vast#generic-edid-replacement-instructions), but it should be noted that the EDID I initially exported from the registry had an incorrect extension count, but replacing the `01` with a `00` fixes this without affecting the functionality as far as I can tell.
