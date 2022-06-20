
# Custom Video Mode Information for Cave Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Cave 68000 Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**cave**] | Cave 68000 240p (Visible) | 7.00 MHz | 57.400 Hz | 320x240 |
[**cave**] | Cave 68000 224p (Visible) | 7.00 MHz | 57.400 Hz | 320x224 |

<br>

## Cave 68000

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**cave**] | **7.00 MHz** | **57.400 Hz** | **320x240** | **4:3**  | **256:219** |
[**cave**] | **7.00 MHz** | **57.400 Hz** | **320x224** | **10:7** | **640:511** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (240p) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,20,81582`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,26,124563`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,33,176701`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (224p) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,12,76127`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,18,116279`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,24,164881`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1020,3,7,18,86624`** | **4.25x** | **1280x1020** | **4x** | **3** |
**`video_mode=1280,48,32,80,1008,3,7,18,85632`** | **4.5x**  | **1280x1008** | **4x** | **2** |

<br>
