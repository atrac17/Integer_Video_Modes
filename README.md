
# Integer Modelines for MiSTer / OSSC DEXX-Pro Lite

<br>

### <p align=center>Please read all information provided in the repository thoroughly.

1. [**Basic Information**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#basic-information)
2. [**Using Non-Standard Video Modes To Produce Hybrid Scaling**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#using-non-standard-video-modes-to-produce-hybrid-scaling)
3. [**MiSTer Provided Scaling Methods**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#mister-provided-scaling-methods)
4. [**MiSTer.ini Information Related To This Repository**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#misterini-information-related-to-this-repository)
5. [**OSSC DEXX-Pro Lite Add-On Provided Scaling Methods**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#ossc-dexx-pro-lite-add-on-provided-scaling-methods)
6. [**OSSC DEXX-Pro Lite Add-On Custom_Scaling.txt Information**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#ossc-dexx-pro-lite-add-on-custom_scalingtxt-information)
7. [**Integer Video Mode Calculation Examples**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#integer-video-mode-calculation-examples)
8. [**Tools Utilized To Create Integer Video Modes**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#tools-utilized-to-create-integer-video-modes)
9. [**Console / Handheld Video Modes & Timings**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/README.md)
10. [**Arcade Video Modes & Timings**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/arcade/README.md)
11. [**Video Modes & Timings Templates**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/arcade/README.md)
12. [**Repository License**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#license)
13. [**Developer Support**](https://github.com/atrac17/MiSTer_Integer_Modelines/tree/Update#support)

<br>

## Basic Information:

  - Video Modes designed for monitors that upscale the provided resolution from the [**DE-10 Nano**](https://www.intel.com/content/www/us/en/developer/topic-technology/edge-5g/hardware/fpga-de10-nano.html). This is known as [**Display Scaling**](https://en.wikipedia.org/wiki/Display_resolution); a hybrid scaling technique. Video Modes designed for LCD displays with a resolution of **1280x1024** and **5:4** aspect ratio; these video modes utilize step-integer scaling.<br><br>
  - Video Modes designed for 120 Hz capable displays; compatible with [**Black Frame Insertion (BFI)**](https://en.wikipedia.org/wiki/Display_motion_blur)  options from the DEXX-Pro or MiSTer framework (**BFI** for the **DE-10 Nano** is currently a **work in progress**).<br><br>
  - Preconfigured MiSTer.ini / custom_scaler.txt files containing sensibly-grouped sets of video modes and timings available for download with all necessary documentation corresponding to the provided video modes.<br><br>

## Using Non-Standard Video Modes To Produce Hybrid Scaling:

  - MiSTer integer-scales the content up to the full height of the provided video mode (defined as a perfect integer size of the original content), the display scales the largest integer image possible by non-integer scaling the provided resolution to the displays native vertical resolution. Thus, filling the entire screen height. Non-integer scaling is minimized utilizing this method; thus, scaling imperfections are drastically reduced, becoming unperceivable to the human eye.<br><br>

### Cavaet:

  - Not all displays are compatible with non-standard video modes. Your display may not accept all or any of them. Displays supporting [**Variable Refresh Rate (VRR)**](https://en.wikipedia.org/wiki/Variable_refresh_rate#:~:text=Variable%20refresh%20rate%20(VRR)%20refers,30%20Hertz%20through%20144%20Hertz), [**Nvidia G-Sync**](https://en.wikipedia.org/wiki/Nvidia_G-Sync), or [**AMD FreeSync**](https://en.wikipedia.org/wiki/FreeSync) are likely to be compatible.<br><br>

## MiSTer Provided Scaling Methods:

  - Integer scaling yields pixel-perfect upscaling, but also means the image is unable to fill the display's full height; known as `vscale_mode=1`. Step-integer scaling is available; scaling is done at 1/2 or 1/4 of the provided resolution; known as `vscale_mode=2` and `vscale_mode=3`.<br><br>
  - Non-integer scaling fills the displays height, but introduces [**scaling artifacts**](https://en.wikipedia.org/wiki/Flicker_(screen)) (uneven scanlines, ["**shimmering" during vertical scrolling**](https://en.wikipedia.org/wiki/Moir%C3%A9_pattern), etc); known as `vscale_mode=0`.<br><br>
  - MiSTer's "auto display scaling" yields similar results; the algorithm used for [**Coordinated Video Timings (CVT)**](https://en.wikipedia.org/wiki/Coordinated_Video_Timings) is calculated different and video modes do not correspond to the native refresh rate from the provided content. The basis for "auto display scaling" sourced from this repository. Visit [**MiSTerFPGA MKDocs**](https://mister-devel.github.io/MkDocs_MiSTer/advanced/videomodes/#presets) for further information.<br><br>

## MiSTer.ini Information Related To This Repository:

  - The default resolution for pre-configured `MiSTer.ini` files is set to `video_mode=0` (**720p**). Each core will utilize `vscale_mode=1` and `vsync_adjust=2` by default. The calculated video modes provided will also function with `vsync_adjust=0` (retaining the native refresh rate of the content) and `vsync_adjust=1`; `vscale_mode=0` and `vsync_adjust=0` require extensive testing. End users will not experience issues when scaling (uneven scanlines, shimmering" during vertical scrolling, etc) using the calculated modelines provided.<br><br>
  - Due to the horizontal limitation of the **DE-10 Nano**'s scaler and [**ADV7513**](https://www.analog.com/media/en/technical-documentation/data-sheets/adv7513.pdf), video modes exceeding the horizontal capability utilize `-1x` for the horizontal scale. This will not affect the aspect ratio on your displays that take advantage of the video mode provided. These are display dependent; nothing is a universal standard.<br><br>
  - Integer-step scaled video modes are available for 1280x1024 LCD displays. Integer step-scaled video modes specify the `vscale_mode` in the pre-configured `MiSTer.ini` file. When utilitzing integer scaled video modes set the `aspect ratio: full screen` or the provided `custom aspect ratio` in the pre-configured `MiSTer.ini` file. The `custom aspect ratio` is set for the contents [**Display Aspect Ratio (DAR)**](https://en.wikipedia.org/wiki/Pixel_aspect_ratio#Introduction); this is the correct aspect ratio for a modern display. When utilizing integer-step scaled video modes set `aspect ratio: full screen` in the MiSTer OSD. This properly displays the provided video mode for a 5:4 aspect ratio display (1280x1024).<br><br>

## OSSC DEXX-Pro Lite Add-On Provided Scaling Methods:

  - **WIP**; OSSC DEXX-Pro Lite Add-On being assembled by [**cyo.the.vile**](https://github.com/cyo-the-vile)

## OSSC DEXX-Pro Lite Add-On Custom_Scaling.txt Information:

  - **WIP**; OSSC DEXX-Pro Lite Add-On being assembled by [**cyo.the.vile**](https://github.com/cyo-the-vile)

<br>

# Integer Video Mode Information

### Integer Video Mode Calculation Examples:

**Integer scaled modelines** based off the vertical refresh rate (calculated pixel clock, horizontal total, and vertical total) and visible resolution. Visible lines plus blanking equal horizontal and vertical total.

<br>

| <p align="center"> Vertical Refresh Rate Formula |
|:---:|
|<table><tr><th><p align=center>Pixel Clock</th><th><p align=center>Horizontal<br>Resolution (Total)</th><th><p align=center>Vertical<br>Resolution (Total)</th><th><p align=center>Refresh Rate Formula</th><th>Refresh Rate</th><th><p align=center>Horizontal<br>Resolution (Visible)</th><th><p align=center>Vertical<br>Resolution (Visible)</th></tr><tr><td>8.00 MHz</td><td><p align=center>512</td><td><p align=center>256 </td><td><p align=center>8 / 512 / 256 =<br>0.00006103515625</td><td><p align=center>61.035 Hz</td><td><p align=center>384</td><td><p align=center>224</td></tr></table>

<br>

[**Coordinated Video Timings-Standard Blanking**](https://en.wikipedia.org/wiki/Coordinated_Video_Timings) (CVT-Standard _VESA-2013-3 v1.2_) based off the vertical refresh rate and **total resolution**. Total resolution is required for accurate modeline calculations based off the pixel clock For this example, the horizontal total is 512 lines and the vertical total is 256 lines.

<br>

| <p align="center">CVT-Standard Modeline Calculation (Manual) |
|:---:|
|<table><tr><th><p align=center>Active Resolution (Visible)<br>`hact / vact`</th><th><p align=center>Front Porch<br>`hfp / vfp`</th><th><p align=center>Sync Width<br>`hs / vs`</th><th><p align=center>Back Porch<br>`hbp / vbp`</th><th><p align=center>Pixel Clock<br>`fpix`</th><th><p align=center>`video_mode=hact,hfp,hs,hbp,vact,vfp,vs,vbp,fpix`</th></tr><tr><td><p align=center>384 / 224</td><td><p align=center>16 / 3</td><td><p align=center>32 / 10</td><td><p align=center>80 / 19</td><td><p align=center>8.000</td><td><p align=center>`video_mode=384,16,32,80,224,3,10,19,8000`</td></table>

<br>

[**Coordinated Video Timings-Reduced Blanking**](https://en.wikipedia.org/wiki/Coordinated_Video_Timings) (CVT-RB; _VESA-2013-3 v1.2_) based off the vertical refresh rate and **visible resolution**. The pixel clock for 4x integer scaling in the example below is exact; in-line with reduced blanking standards **not 1/4 rounded**.

<br>

| <p align="center">CVT-RB Modeline Calculation (4x Integer Scale) |
|:---:|
|<table><tr><th><p align=center>Active Resolution (Visible)<br>`hact / vact`</th><th><p align=center>Front Porch<br>`hfp / vfp`</th><th><p align=center>Sync Width<br>`hs / vs`</th><th><p align=center>Back Porch<br>`hbp / vbp`</th><th><p align=center>Pixel Clock<br>`fpix`</th><th><p align=center>`video_mode=hact,hfp,hs,hbp,vact,vfp,vs,vbp,fpix`</th></tr><tr><td><p align=center>1536 / 896</td><td><p align=center>48 / 3</td><td><p align=center>32 / 10</td><td><p align=center>80 / 13</td><td><p align=center>95.442</td><td><p align=center>`video_mode=1536,48,32,80,896,3,10,13,954429`</td></table>

<br>

### Tools Utilized To Create Integer Video Modes:

  - [**MiSTer modeline to video_mode conversion**](https://morf77.pythonanywhere.com/vm) by [**morf77**](https://github.com/morfeus77/MiSTerTools); this tool can be utilized to create **video_modes** for MiSTer by calculating modlines. There are several modeline tools available. This process is not used in the repository, but worth noting.<br><br>
  - [**MiSTer video_mode to modeline conversion**](https://morf77.pythonanywhere.com/ml) by [**morf77**](https://github.com/morfeus77/MiSTerTools); this tool can be utilized for creating **OSSC** timing parameters based off of modeline information. This tool is invaluable, I cannot thank morf77 enough for implementing this request.<br><br>
  - [**MiSTer aspect ratio calculator**](https://morf77.pythonanywhere.com/ar) by [**morf77**](https://github.com/morfeus77/MiSTerTools) and [**kitrinx**](https://github.com/kitrinx); this tool can be utilized to find **Display Aspect Ratio (DAR)** with information provided in this repository.<br><br>
  - [**Custom Resolution Utility (CRU) 1.5**](https://www.monitortests.com/blog/custom-resolution-utility-cru-1-5/) by [**ToastyX**](https://www.patreon.com/ToastyX/); this tool is the primary resource for creating integer modelines. Many thanks to the developer; consider supporting their endeavors.

#

# <p align=center>[Console / Handheld Video Modes & Timings](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/README.md)<br>For MiSTer cores & the  DEXX-Pro Lite Add-On</p>

#

# <p align=center>[Arcade Video Modes & Timings](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/arcade/README.md)<br>For MiSTer cores & the  DEXX-Pro Lite Add-On</p>

#

# <p align=center>[Video Modes & Timings Templates](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/template/README.md)<br>For MiSTer cores & the  DEXX-Pro Lite Add-On</p>

# License

This repository and project is licensed under the GNU General Public License v3.0. If you utilize the information elsewhere, reference the source repository and provide credit to the author(s).

# Support

Please consider showing support for this and future projects on my **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.
