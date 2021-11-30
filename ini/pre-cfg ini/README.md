

![logo](https://user-images.githubusercontent.com/32810066/128452226-e23e1552-abb7-434b-92e1-b4b35a23a5af.png)

# Pre-configured .ini files

# Important notes

- The default display resolution for the MiSTer.ini should always be 720p when utilizing custom video modes.

- Custom video modes are applied by the MiSTerFPGA framework, by matching the loaded core's common name against an .ini section name.

- I do not maintain the MiSTerFPGA framework, so do not report problems with it to me.  Instead, open an issue here: https://github.com/MiSTer-devel/Template_MiSTer/issues

- I do not maintain the MiSTer cores, so do not report problems with them to me.  Instead, find the core's GitHub repository and open an issue against it there.

- If an arcade core refuses to match up against its .ini section, you can try a workaround:
   - Change the .ini section name to match the ROM setname provided by a specific game's .mra file.
   - For example, `[jt1942]` (the core name) would become `[1942]` (the ROM set name).


# Detailed information

<details>

_<summary><b>3x Rotated Integer Scaled</b></summary>_

<blockquote>

This pre-configured .ini file contains modelines that perform 3x integer scaling for arcade games requiring 90-degree rotation (such as vertical shooters, like 1941).  Ensure the display utilizing custom video modes is set to 4:3 or original to display the proper aspect ratio.

This pre-configured .ini file **is not setup to do dual display** for an analog IO board. You must configure the .ini for dual display yourself. I cannot assume everyone's settings (i.e. YPbPr, RGBS, RGBHV, RGsB) for their CRT monitor.

The default setting for this .ini file is `vscale_mode=0` (because the scaler chooses the wrong integer scale factor for rotated content, and the modelines inherently work out to integer scaling anyway) and `vsync_adjust=2`.

</blockquote>

</details>

<details>

_<summary><b>4x (or equivalent) Integer Scaled</b></summary>_

<blockquote>

This pre-configured .ini file is only set for 4x or equivalent custom video modes. Ensure the display utilizing custom video modes is set to 4:3 or original to display the proper aspect ratio.

This pre-configured .ini file **is not setup to do dual display** for an analog IO board. You must configure the .ini for dual display yourself. I cannot assume everyone's settings (i.e. YPbPr, RGBS, RGBHV, RGsB) for their CRT monitor.

The default setting for this .ini file are `vscale_mode=1` and `vsync_adjust=2`.

_<b>For Nintendo Famicom / Nintendo Entertainment System set the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

_<b>Sega Mark III / Master System see the following:</b>_

- Sega Mark III / Master System are shared with GameGear hardware in the FPGA core. You will need to ssh into your device and set the custom video mode per hardware selection.

</blockquote>

</details>

<details>

_<summary><b>5x (or equivalent) Integer Scaled</b></summary>_

<blockquote>

This pre-configured .ini file is only set for 5x or equivalent custom video modes. Ensure the display utilizing custom video modes is set to 4:3 or original to display the proper aspect ratio.

This pre-configured .ini file **is not setup to do dual display** for an analog IO board. You must configure the .ini for dual display yourself. I cannot assume everyone's settings (i.e. YPbPr, RGBS, RGBHV, RGsB) for their CRT monitor.

The default setting for this .ini file are `vscale_mode=1` and `vsync_adjust=2`.

_<b>For Nintendo Famicom / Nintendo Entertainment System set the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

_<b>Sega Mark III / Master System see the following:</b>_

- Sega Mark III / Master System are shared with GameGear hardware in the FPGA core. For this pre-configured .ini file a **Dual Mode** custom video mode has been utilized. This does not require switching the custom video mode when switching between Mark II/ Master System titles.

</blockquote>

</details>

<details>

_<summary><b>6x (or equivalent) Integer Scaled</b></summary>_

<blockquote>

This pre-configured .ini file is only set for 6x or equivalent custom video modes. Ensure the display utilizing custom video modes is set to 4:3 or original to display the proper aspect ratio.

This pre-configured .ini file **is not setup to do dual display** for an analog IO board. You must configure the .ini for dual display yourself. I cannot assume everyone's settings (i.e. YPbPr, RGBS, RGBHV, RGsB) for their CRT monitor.

The default setting for this .ini file are `vscale_mode=1` and `vsync_adjust=2`.

_<b>For Nintendo Famicom / Nintendo Entertainment System set the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

_<b>Sega Mark III / Master System see the following:</b>_

- Sega Mark III / Master System are shared with GameGear hardware in the FPGA core. You will need to ssh into your device and set the custom video mode per hardware selection.

</blockquote>

</details>

<details>

_<summary><b>1280x1024 VGA Monitors</b></summary>_

<blockquote>

This pre-configured .ini file is only set for 1280x1024 VGA monitors. Ensure you use this .ini file with a VGA monitor only

The default setting for this .ini file is `vga_scaler=1`.

_<b>When utilizing Integer-Step Scaled video modes, set `Aspect Ratio: Full Screen` in the MiSTer OSD. This properly displays the provided custom video modes.</b>_

_<b>For Nintendo Famicom / Nintendo Entertainment System set the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

</blockquote>

</details>

<details>

_<summary><b>1280x1024 LCD Displays</b></summary>_

<blockquote>

This pre-configured .ini file is only set for 1280x1024 LCD displays. If utilizing the vga output to a CRT display, you will need to adjust the .ini file accordingly.

You have two options for this .ini file, you can utilize `dvi_mode=1` and use a HDMI to DVI adapter or `vga_scaler=1`. Neither is set in the pre-configured .ini file. Please specify this yourself, I cannot assume how you will utilize this .ini file with your display.

_<b>When utilizing Integer-Step Scaled video modes, set `Aspect Ratio: Full Screen` in the MiSTer OSD. This properly displays the provided custom video modes.</b>_

_<b>For Nintendo Famicom / Nintendo Entertainment System set the following:</b>_

- Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.

</blockquote>

</details>

# License

This repository and project is licensed under the GNU General Public License v3.0. If you utilize the information elsewhere, you must reference this source repository and provide credit to the author(s).

# Support

Please consider showing support for this and future projects on my **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
