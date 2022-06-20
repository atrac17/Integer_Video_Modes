
# Custom Video Mode Information for Nichibutsu Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Nichibutsu Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**terracresta**] | Nichibutsu M68000 Terra Cresta Based       | 6.00 MHz | 59.410 Hz | 256x224 |
[**armedf**]      | Nichibutsu M68000 Terra Force Based        | 6.00 MHz | 59.175 Hz | 320x240 |
[**armedf**]      | Nichibutsu M68000 Legion Spinner-87 Based  | 6.00 MHz | 59.175 Hz | 288x224 |

<br>

## Nichibutsu M68000 Terra Cresta Based

### Terra Cresta<br>Sei Senshi Amatelass<br>Kid no Hore Hore Daisakusen

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**terracresta**] | **6.00 MHz** | **59.410 Hz** | **256x224** | **8:7** | **2560:2191** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,64855`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,98555`**   | **5x** | **1280x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,25,170778`**  | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,88716`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

## Nichibutsu M68000 Terra Cresta Based

### Terra Force<br>Kozure Ōkami<br>Armed F<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**armed f**] | **6.00 MHz** | **58.950 Hz** | **320x240** | **4:3** | **1280:939** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,20,83785`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,27,128030`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,34,181595`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1020,3,7,19,89048`** | **4.25x** | **1280x1020** | **4x** | **2** |

<br>

## Nichibutsu M68000 Legion Spinner-87 Based

### Chouji Meikyuu Legion<br>Crazy Climber 2

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**armed f**] | **6.00 MHz** | **58.950 Hz** | **288x224** | **9:7** | **2880:2191** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1152,48,32,80,896,3,10,12,71233`**    | **4x** | **1152x896**  | **4x** |
**`video_mode=1440,48,32,80,1120,3,10,19,108657`**  | **5x** | **1440x1120** | **5x** |
**`video_mode=1728,48,32,80,1344,3,10,25,153814`**  | **6x** | **1728x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1224,48,32,80,1008,3,10,16,84606`** | **4.5x** | **1224x1008** | **5x** | **2** |

<br>
