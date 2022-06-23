
# Custom Video Mode Information for Toaplan V1 Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Toaplan Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**toaplan v1**] | Toaplan V1 | 7.00 MHz | 57.613 Hz | 320x240 |
[**toaplan v1**] | Toaplan V1 | 7.00 MHz | 55.161 Hz | 320x240 |

<br>

## Toaplan V1 Hardware

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**toaplan v1**] | **7.00 MHz** | **57.613 Hz** | **320x240** | **4:3**  | **256:219** |
[**toaplan v1**] | **7.00 MHz** | **55.161 Hz** | **320x240** | **4:3**  | **256:219** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV 57.613 Hz) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,20,81885`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,26,125025`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,33,177356`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV 55.161 Hz) | Integer | Resolution (240p) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,18,78241`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,25,119607`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,31,169579`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1020,3,7,18,86945`** | **4.25x** | **1280x1020** | **4x** | **3** |
**`video_mode=1280,48,32,80,1020,3,7,18,83166`** | **4.25x** | **1280x1020** | **4x** | **3** |

<br>
