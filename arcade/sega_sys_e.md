
# Custom Video Mode Information for Sega Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Sega Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**sms**] | Sega System E Based | 5.37 MHz | 59.930 Hz | 256x192 |

<br>

## Sega System I / II

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**sms**] | **5.37 MHz** | **59.930 Hz** | **256x192** | **4:3** | **35:24** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal | Dual Mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85264`**   | **5x** | **1280x960**  | **5x** | **No**  |
**`video_mode=1536,48,32,80,1152,3,4,26,120445`** | **6x** | **1536x1152** | **6x** | **Yes** |
**`video_mode=1792,48,32,80,1344,3,4,32,161788`** | **7x** | **1792x1344** | **7x** | **No**  |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89493`** | **5.25x** | **1008p** | **5x** | **3** |

<br>
