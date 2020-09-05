# <u>BIOS Configuration</u>

BIOS version: `F11`

- Enter BIOS → Press F12 → Enter Setup
- Save & Exit → Load Optimized Defaults
 
- Boot -> Windows 8/10 Features -> Win 8/10WHQL
- Boot -> CSM Support -> Disabled (Can be set to Enabled if need be but try to have it set to Disabled first)
- Favourites -> Extreme Memory Profile (X.M.P.) -> Profile1
- Favourites -> VT-d -> Disabled (Can be set to Enabled or Disabled, Your choice)
- Settings -> IO Ports -> Internal Display Output -> PCIe 1 Slot
- Settings -> IO Ports -> Internal Graphics -> Enabled (Set to Disabled if using SMBios iMacPro1,1)
- Settings -> IO Ports -> DVMT Pre-Allocated -> 64M
- Settings -> IO Ports -> DVMT Total GFX0-Allocated -> 256M
- Settings -> IO Ports -> Aperture Size -> 256MB
- Settings -> IO Ports -> Audio Controller -> Enabled
- Settings -> IO Ports -> Above 4G Decoding -> Enabled
- Settings -> IO Ports -> USB Configuration -> Legacy USB Support -> Auto
- Settings -> IO Ports -> USB Configuration ->  XHCI Hand-off -> Enabled
- Settings -> Miscellaneous -> Software Guard Extensions (SGX) -> Disabled﻿
- Settings -> Platform Power -> Platform Power Management -> Enabled
- Settings -> Platform Power -> ErP -> Enabled
- Settings -> Platform Power -> RC6(Render Standby) -> Enabled
 
- Save & Exit → Save & Exit Setup

## <u> Hidden BIOS setting </u>

Very Clear Guide to disable [CFG Lock](https://www.youtube.com/watch?v=W4JXVNJsK98)<br>

⚠️: These offset are only valid for the specific firmware version! <br>
Do not try to execute these commands on different firmware or motherboard to the one used in this guide!<br>
You have been warned.<p> 
NOTE: The modified variables will reset itself when you restore / revert to optimised defaults with BIOS.<br> 

### <u>Required setting</u>
- Disable CFG Lock

| Firmware Version | Command              |
|------------------|----------------------|
| F9, F10, F11 & F12c         |`setup_var 0x5C1 0x00`|

<p>
<p>

#### <u>Optional Setting - not tested/verified by me </u>
- Turn off motherboard LED

| Firmware Version | Command               |
|------------------|-----------------------|
| 11               |`setup_var 0x16FE 0x00`|
|                  |`setup_var 0x16FF 0x00`|
|                  |`setup_var 0x1700 0x00`|
|                  |`setup_var 0x1701 0x00`|
