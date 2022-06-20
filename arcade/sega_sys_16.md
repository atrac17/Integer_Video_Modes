
# Custom Video Mode Information for Sega Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Sega Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**jts16**]<br>[**jts16b**]<br>[**jts16b3**] | Sega System16A / 16B Based | 6.2937 MHz | 60.284 Hz | 320x224 |

<br>

## Sega System 16A / 16B

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jts16**]<br>[**jts16b**]<br>[**jts16b3**] | **6.2937 MHz** | **60.284 Hz** | **320x224** | **10:7** | **400:287** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,80038`**    | **4x** | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,122228`**  | **5x** | **1600x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,173416`**  | **6x** | **1920x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,90021`** | **4.5x** | **1280x1008** | **4x** | **2** |

<br>
