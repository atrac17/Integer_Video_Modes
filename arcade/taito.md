
# Custom Video Mode Information for Taito Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Taito Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**a.arkanoid**] | Taito Z80 Based | 6.00 MHz | 59.185 Hz | 256x225 |
[**jtbubl**] | Taito Z80 Based | 6.00 MHz | 59.185 Hz | 256x225 |
[**jtrastan**] | Taito M68000 Based | 6.677 MHz | 59.876 Hz | 256x224 |

<br>

## Taito Z80 Based

### Arkanoid<br>Bubble Bobble<br> Tokio

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**a.arkanoid**]<br>[**jtbubl**] | **6.00 MHz** | **59.185 Hz** | **256x224 (Hardware)<br>256x225 (FPGA Core)** | **8:7** | **2560:2191** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (224) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,64610`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,98181`**   | **5x** | **1280x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,25,170131`**  | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (225) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,900,3,10,13,64890`**    | **4x** | **1024x900**  | **4x** |
**`video_mode=1280,48,32,80,1125,3,10,19,98607`**   | **5x** | **1280x1125** | **5x** |
**`video_mode=1920,48,32,80,1350,3,10,25,170870`**  | **6x** | **1536x1350** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution (224) | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,88380`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution (225) | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1012,3,7,19,88721`** | **4.5x** | **1280x1012** | **5x** | **2** |

<br>

## Taito M68000 Based

### Rastan<br>Operation Wolf<br>Rainbow Islands: The Story of Bubble Bobble 2

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtrastan**] | **6.677 MHz** | **59.876 Hz** | **320x240** | **4:3** | **320:261** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85187`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,27,130042`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,34,184447`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1020,3,7,19,90447`** | **4.25x** | **1280x1020** | **4x** | **2** |

<br>
