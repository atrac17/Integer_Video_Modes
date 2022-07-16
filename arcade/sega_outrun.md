
# Custom Video Mode Information for Sega Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Sega Super Scaler Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**jtoutrun**] | Sega OutRun Based | 6.2937 MHz | 60.054 Hz | 320x224 |

<br>

## Sega OutRun Hardware<br><br>OutRun<br>Super Hang-On<br>Turbo OutRun

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtoutrun**] | **6.2937 MHz** | **60.054 Hz** | **320x224** | **10:7** | **400:287** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79733`**    | **4x** | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,121761`**  | **5x** | **1600x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,172754`**  | **6x** | **1920x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89678`** | **4.5x** | **1280x1008** | **4x** | **2** |

<br>
