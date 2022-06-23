
# Custom Video Mode Information for DataEast Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# DataEast Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**jtninja**]<br>[**jtcop**] | DataEast MEC-M1 Based | 6.00 MHz | 57.407 Hz | 256x240 |
[**jtmidres**]<br>[**jtslyspy**] | DataEast MEC-M1<br>(Midnight Resistance Based) | 6.00 MHz | 57.407 Hz | 256x240 |

<br>

## DataEast MEC-M1 Based Hardware (All Variants)

### Dragon Ninja / Bad Dudes vs Dragon Ninja<br>Birdie Try<br>Hippodrome / Fighting Fantasy<br>Heavy Barrel<br>Midnight Resistance<br>RoboCop<br>Secret Agent / Sly Spy<br>Stadium Hero

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtninja**]<br>[**jtcop**]<br>[**jtmidres**]<br>[**jtslyspy**] | **6.00 MHz** | **57.407 Hz** | **256x240** | **16:15** | **1024:939** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,960,3,10,14,67087`**    | **4x** | **1024x960**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,20,101928`**  | **5x** | **1280x1200** | **5x** |
**`video_mode=1536,48,32,80,1344,3,10,27,144097`**  | **6x** | **1536x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1260,48,32,80,1020,3,7,18,85431`** | **4.25x** | **1260x1020** | **4.5x** | **3** |

<br>
