
# Custom Video Mode Information for Mitchell Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Mitchell Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**jtpang**] | Mitchell Z80 Based | 8.00 MHz | 56.338 Hz | 384x240 |

<br>

## Mitchell Z80 Based<br><br>Pang!<br>Super Pang!<br>Block Block

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtpang**] | **8.00 MHz** | **56.338 Hz** | **384x240** | **8:5** | **512:417** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,6,17,94212`**    | **4x** | **1536x960**  | **4x** |
**`video_mode=1920,48,32,80,1200,3,6,23,144370`**  | **5x** | **1920x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,32,173314`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1248,48,32,80,1008,3,10,15,83132`** | **4.25x** | **1248x1020** | **3.25x** | **3** |

<br>
