
![logo](https://user-images.githubusercontent.com/32810066/128452226-e23e1552-abb7-434b-92e1-b4b35a23a5af.png)

# Pre-Configured .ini File Information

<details>

_<summary><b>1280x1024 VGA Monitors</b></summary>_

<blockquote>

This pre-configured ini file is only set for 1280x1024 VGA Monitors.

The default display resolution for the MiSTer.ini should always be 720p when utilizing custom video modes.

The defualt setting for this .ini file is vga_scaler=1.

_<b>When utilizing Integer-Step Scaled video modes set Aspect Ratio: Full Screen in the MiSTer OSD. This is the proper way to utilize these custom video modes.</b>_

_<b>For Nintendo Famicom / Nintendo Entertainment System plese do the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

### Notes:

If a custom video mode is not applied to an Arcade core, I have no control over this. I do not maintain the MiSTerFPGA framework repository or core repositories available in mister-devel or jtbin. 

The common name in the core is dictated by the core author. Occasionally, a change may occur that breaks this feature. You should report the issue to that authors core repository. 

In the interim, you can utilize the setname provided in the .mra file if necessary.

- Example: 
[jt1942] would become [1942] per the setname provided in the .mra file.

</blockquote>

</details>

<details>

_<summary><b>1280x1024 LCD Displays</b></summary>_

<blockquote>

This pre-configured ini file is only set for 1280x1024 LCD displays. If utilizing the vga output to a CRT display, you will need to adjust the ini file accordingly.

The default display resolution for the MiSTer.ini should always be 720p when utilizing custom video modes.

You have two options for this ini file, you can utilize dvi_mode=1 and use a HDMI to DVI adapter or vga_scaler=1. Neither is set in the pre-configured .ini file. Please specify this yourself, I cannot assume how you will utilize this .ini file with your display.

_<b>When utilizing Integer-Step Scaled video modes set Aspect Ratio: Full Screen in the MiSTer OSD. This is the proper way to utilize these custom video modes.</b>_

_<b>For Nintendo Famicom / Nintendo Entertainment System plese do the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

### Notes:

If a custom video mode is not applied to an Arcade core, I have no control over this. I do not maintain the MiSTerFPGA framework repository or core repositories available in mister-devel or jtbin. 

The common name in the core is dictated by the core author. Occasionally, a change may occur that breaks this feature. You should report the issue to that authors core repository. 

In the interim, you can utilize the setname provided in the .mra file if necessary.

- Example: 
[jt1942] would become [1942] per the setname provided in the .mra file.

</blockquote>

</details>

# License

This repository and project is licensed under the GNU General Public License v3.0. If you utilize the information elsewhere, you must reference this source repository and provide credit to the author(s).

# Support

Please consider showing support for this and future projects on my **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
