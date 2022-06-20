
# Custom Video Mode Information for Sega Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Sega Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**a.segasys1**]<br>[**a.segasys1+2**] | Sega System 1 / 2 Based | 5.00 MHz | 60.096 Hz | 256x224 |

<br>

## Sega System I / II

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**a.segasys1**]<br>[**a.segasys1+2**] | **5.00 MHz** | **60.096 Hz** | **256x224** | **4:3** | **2560:1827** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,65604`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,99693`**   | **5x** | **1280x1120** | **5x** |
**`video_mode=1536,48,32,80,1344,3,10,26,140960`**  | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89741`** | **4.5x** | **1280x1008** | **4x** | **2** |

<br>
