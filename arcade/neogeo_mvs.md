
# Custom Video Mode Information for SNK NeoGeo MVS Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# SNK Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**neogeo**] | NeoGeo MVS Based | 6.00 MHz | 59.185 Hz | 320x224 |

<br>

## Neo Geo Multi Video System

| Core | Pixel Clock | Refresh Rate |Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio | 
|:--:|:--:|:--:|:--:|:--:|:--:|
[**neogeo**] | **6.00 MHz** | **59.185 Hz** | **320x224** | **10:7** | **3200:2191** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,78579`**    | **4x** | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,119999`**  | **5x** | **1536x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,25,170131`**  | **6x** | **1920x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,88380`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>
