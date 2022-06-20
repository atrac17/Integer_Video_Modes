
# Integer Modelines for MiSTer / OSSC DEXX-Pro Lite

<br>

### <p align=center>Please read all information provided in the repository thoroughly.

<br>
<br>

## Video Mode Information:

  • Modes designed for monitors that upscale the provided resolution from the DE-10 Nano. This is known as "display scaling".<br><br>
  • Modes designed for LCD displays and common VGA CRT monitors with a resolution of 1280x1024. LCD displays of this nature have a 5:4 aspect ratio.<br><br>
  • Modes designed for 120 Hz capable displays to include VGA CRT monitors with BFI options from the DEXX-Pro or MiSTer framework running on the DE-10 Nano.<br><br>
  • Preconfigured MiSTer.ini / custom_scaler.txt files containing sensibly-grouped sets of video modes and timings.<br><br>
  • The `releases` directory houses pre-configured `.ini` / `.txt` files, ranging from 4x to 6x (or equivelant integer scaled resolutions).<br><br>

<br>

## Using a non-standard video modes to produce hybrid scaling:

  • MiSTer integer-scales the content up to the full height of the provided video mode (defined as a perfect integer size of the original content), to feed the display the largest perfect image possible. The display non-integer-scales that image the rest of the way up to fill the entire screen height.<br><br>
  • The amount of non-integer scaling is minimized, the scaling imperfections are drastically reduced, to the point of being unnoticeable.<br><br>

### Cavaet:

  • Not all displays are compatible with all non-standard video modes.  Your display may not accept all or any of them.<br><br>
  • Displays that support Variable Refresh Rate (VRR), G-Sync, or FreeSync are more likely to be compatible.<br><br>

## MiSTer provided scaling methods:

  • Integer scaling yields pixel-perfect upscaling, but it also means the image can't fill your display's full height. This is known as `vscale_mode=1`. You can also step integer scale at 1/2 or 1/4. This is known as `vscale_mode=2` and `vscale_mode=3`.<br><br>
  • Non-integer scaling fills the screen height, but it introduces very annoying artifacts (uneven scanlines, "shimmering" during vertical scrolling, etc). This is known as `vscale_mode=0`.<br><br>
  • MiSTer "auto display scaling" yields similar results; you will be required to use `vscale_mode=4`, `vscale_mode=5`, `vscale_mode=6` and `vsync_adjust=1` or the native refresh rate will not be aligned. Visit the [**MiSTerFPGA wiki**](https://github.com/MiSTer-devel/Main_MiSTer/wiki) for further information on `vscale_mode=4` to `vscale_mode=6`.<br><br>

## OSSC DEXX-Pro Lite Add-On provided scaling methods:

  • **WIP**; OSSC DEXX-Pro Lite Add-On being assembled by [**cyo**](https://github.com/cyo-the-vile)

<br>

# MiSTer.ini Information

  • The default display resolution for the MiSTer.ini is set to 720p (`video_mode=0`) when utilizing  pre-defined video modes. Each core will be `vscale_mode=1` and `vsync_adjust=0` by default. You will not experience uneven scanlines, "shimmering" during vertical scrolling, etc. if using a calculated modeline provided.

  • Due to the horizontal limitation of 2048 within cores, some video modes will utilize -1x for the horizontal scale. This will not affect the aspect ratio on your display if it's scaler takes advantage of the video mode provided. These are display dependent; nothing is a universal standard.

  • Integer-Step Scaled video modes are available for 1280x1024 LCD displays and common VGA CRT monitors with the same resolution; different video modes provided. Integer Step-Scaled Video Modes will specify the `vscale_mode` in the pre-configured `.ini` file. Video modes for VGA CRT monitors will utilize `vga_scaler=1`.

  • When utilitzing Integer Scaled video modes set the `aspect ratio: full screen` or the provided `custom aspect ratio` in the pre-configured `.ini` file. The `custom aspect ratio` is set to `DAR` (Display Aspect Ratio); this is the correct aspect ratio for a modern display.

  • When utilizing Integer-Step Scaled video modes set `aspect ratio: full screen` in the MiSTer OSD. This properly displays the provided video mode. If you are using a common VGA CRT monitor, you can stretch the horizontal and vertical to fill the screen in the displays OSD in the monitors settings (end user preference).

  • If a core has `Dual Mode=Yes`, then there will only be one primary video mode available as the core supports multiple systems for one video mode. For custom aspect ratios, the first will be for the primary hardware and the other for the secondary hardware.

<br>

# OSSC DEXX-Pro Lite Add-On .txt Information

<br>

• **WIP**; OSSC DEXX-Pro Lite Add-On being assembled by [**cyo**](https://github.com/cyo-the-vile)

<br>

# Integer Video Mode Information

# <p align=center>[Console / Handheld Video Modes & Timings](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/README.md)<br>For MiSTer cores & the  DEXX-Pro Lite Add-On</p>

#

# <p align=center>[Arcade Video Modes & Timings](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/arcade/README.md)<br>For MiSTer cores & the  DEXX-Pro Lite Add-On</p>

#

# <p align=center>[Video Modes & Timings Templates](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/template/README.md)<br>For MiSTer cores & the  DEXX-Pro Lite Add-On</p>

### Integer Video Mode Calculation Example:

**Integer scaled modelines** based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution. Visible lines plus blanking equal h/v total.

| <p align="center">Formula For Vertical Refresh Rate |
|:---:|
|<table><tr><th><p align=center>Pixel Clock</th><th><p align=center>Horizontal<br>Resolution (Total)</th><th><p align=center>Vertical<br>Resolution (Total)</th><th><p align=center>Refresh Rate Formula</th><th>Refresh Rate</th><th><p align=center>Horizontal<br>Resolution (Visible)</th><th><p align=center>Vertical<br>Resolution (Visible)</th></tr><tr><td>8.00 MHz</td><td><p align=center>512</td><td><p align=center>256 </td><td><p align=center>8 / 512 / 256 =<br>0.00006103515625</td><td><p align=center>61.035 Hz</td><td><p align=center>384</td><td><p align=center>224</td></tr></table>

<br>

**Coordinated Video Timings-Standard** (CVT-Standard _VESA-2013-3 v1.2_) based off the vertical refresh rate and **total resolution**. Total resolution is required for accurate modeline calculations based off the pxlclk.

| <p align="center">CVT-Standard Modeline Calculation (Native) [CRT] |
|:---:|
|<table><tr><th><p align=center>Visible Resolution</th><th><p align=center>Front Porch</th><th><p align=center>Sync Width</th><th><p align=center>Back Porch</th><th><p align=center>Pixel Clock</th><th><p align=center>`video_mode=`</th></tr><tr><td><p align=center>384 / 224</td><td><p align=center>16 / 3</td><td><p align=center>32 / 10</td><td><p align=center>80 / 19</td><td><p align=center>8.000</td><td><p align=center>`384,16,32,80,224,3,10,19,8000`</td></table>

**Coordinated Video Timings-Reduced Blanking** (CVT-RB; _VESA-2013-3 v1.2_) based off the vertical refresh rate and visible resolution. The pxlclk for 4x integer in this example is exact; **not 1/4 rounded** and falls in-line with reduced blanking standards.

| <p align="center">CVT-RB Modeline Calculation (4x Integer Scale) [HDMI] |
|:---:|
|<table><tr><th><p align=center>Visible Resolution</th><th><p align=center>Front Porch</th><th><p align=center>Sync Width</th><th><p align=center>Back Porch</th><th><p align=center>Pixel Clock</th><th><p align=center>`video_mode=`</th></tr><tr><td><p align=center>1536 / 896</td><td><p align=center>48 / 3</td><td><p align=center>32 / 10</td><td><p align=center>80 / 13</td><td><p align=center>95.442</td><td><p align=center>`1536,48,32,80,896,3,10,13,954429`</td></table>

<br>

# License

This repository and project is licensed under the GNU General Public License v3.0. If you utilize the information elsewhere, reference the source repository and provide credit to the author(s).

# Support

Please consider showing support for this and future projects on my **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.
