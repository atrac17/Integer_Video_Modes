
# Custom Video Mode Information for Capcom Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Capcom Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**jt1942**]<br>[**jt1943**]<br>[**jtbtiger**]<br>[**jtcom**]<br>[**jtgun**]<br>[**jthige**]<br>[**jtvulgus**]<br>[**jtexed**] | Capcom Z80 | 6.00 MHz | 59.637 Hz | 256x224 |
[**jtsarms**] | Capcom Z80<br>(Side Arms Based) | 8.00 MHz | 60.096 Hz | 384x224 |
[**jtsz**]<br>[**jttrojan**] | Capcom Z80<br>(Section Z Based) | 6.00 MHz | 55.407 Hz<br>56.003 Hz | 256x240 |
[**jtgng**] | Capcom M6809 Based | 6.00 MHz | 59.637 Hz | 256x224 |
[**jtrumble**] | Capcom M6809 Based | 8.00 MHz | 57.444 Hz | 353x240 |
[**jtbiocom**]<br>[**jtf1drm**]<br>[**jttora**] | Capcom M68000 Based | 6.00 MHz | 59.637 Hz | 256x224 |
[**jtsf**] | Capcom M68000 Based | 8.00 MHz | 61.035 Hz | 384x224 |
[**jtcps1**]<br>[**jtcps15**]<br>[**jtcps2**] | Capcom System / Dash / II | 8.00 MHz | 59.629 Hz | 384x224 |

<br>

## Capcom Z80 Hardware

### 1942<br>1943<br>Black Dragon / Black Tiger<br>Commando<br>Gun.Smoke<br>ひげ丸 / Pirate Ship Higemaru<br>Vulgus<br>超浮遊要塞エグゼドエグゼス (Exed Exes) / Savage Bees

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jt1942**]<br>[**jt1943**]<br>[**jtbtiger**]<br>[**jtcom**]<br>[**jtgun**]<br>[**jthige**]<br>[**jtvulgus**]<br>[**jtexes**] | **6.00 MHz** | **59.637 Hz** | **256x224** | **8:7** | **2560:2191** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,65103`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,98931`**   | **5x** | **1280x1120** | **5x** |
**`video_mode=1860,48,32,80,1344,3,10,25,139782`**  | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89055`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

### サイドアーム / Hyper Dyne: Side Arms (Capcom Z80 Side Arms Based)

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtsarms**] | **8.00 MHz** | **60.096 Hz** | **384x224** | **12:7** | **1280:973**|

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1536,48,32,80,896,3,10,13,93973`**    | **4x** | **1536x896**  | **4x** |
**`video_mode=1920,48,32,80,1120,3,10,19,144000`**  | **5x** | **1920x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,172875`**  | **6x** | **1920x1344** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1248,48,32,80,1008,3,7,19,87746`** | **4.5x** | **1248x1008** | **3.25x** | **3** |

<br>

### Capcom Z80 Section Z Based<br><br>Aresu no Tsubasa / Legendary Wings<br>セクションZ / Section Z

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtsz**] | **6.00 MHz** | **55.407 Hz** | **256x240** | **16:15** | **1024:939** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,960,3,10,13,64684`**    | **4x** | **1024x960**  | **4x** |
**`video_mode=1280,48,32,80,1200,3,10,19,98297`**   | **5x** | **1280x1200** | **5x** |
**`video_mode=1860,48,32,80,1440,3,10,25,138889`**  | **6x** | **1536x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,17,82579`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

### Tatakai no Banka / Trojan (Capcom Z80 Section Z Based)

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jttrojan**] | **6.00 MHz** | **56.003 Hz** | **256x240** | **16:15** | **1024:939** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,960,3,10,13,65380`**    | **4x** | **1024x960**  | **4x** |
**`video_mode=1280,48,32,80,1200,3,10,19,99354`**   | **5x** | **1280x1200** | **5x** |
**`video_mode=1860,48,32,80,1440,3,10,25,140478`**  | **6x** | **1536x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,17,83467`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

### Makaimura / Ghosts 'n Goblins (Capcom M6809 Based)

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtgng**] | **6.00 MHz** | **59.637 Hz** | **256x224** | **8:7** | **2560:2191** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,65103`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,98931`**   | **5x** | **1280x1120** | **5x** |
**`video_mode=1536,48,32,80,1344,3,10,25,13978`**  | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89055`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

### Rush & Crash / The Speed Rumbler (Capcom M6809 Based)

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtrumble**] | **8.00 MHz** | **57.444Hz** | **353x240** | **22:15** | **1412:1251** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1412,48,32,80,960,3,10,14,89129`**    | **4x** | **1412x960**  | **4x** |
**`video_mode=1765,48,32,80,1200,3,10,20,136345`**  | **5x** | **1765x1200** | **5x** |
**`video_mode=1765,48,32,80,1440,3,7,30,163658`**   | **6x** | **1765x1440** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1236,48,32,80,1020,3,10,15,84042`** | **4.25x** | **1236x1020** | **3.5x** | **3** |

<br>

### Capcom M68000 Based<br><br>Top Secret / Bionic Commando<br>F-1 Dream<br>Tora e no Michi / Tiger Road

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtbiocom**]<br>[**jtf1drm**]<br>[**jttora**] | **6.00 MHz** | **59.637 Hz** | **256x224** | **8:7** | **2560:2191** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,65103`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,98931`**   | **5x** | **1280x1120** | **5x** |
**`video_mode=1536,48,32,80,1344,3,10,25,13978`**   | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89055`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

### Street Fighter (Capcom M68000 Based)

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtsf**] | **8.00 MHz** | **61.035 Hz** | **384x224** | **12:7** | **1280:973** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1536,48,32,80,896,3,10,13,95442`**    | **4x** | **1536x896**  | **4x** |
**`video_mode=1920,48,32,80,1120,3,10,20,146377`**  | **5x** | **1920x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,175576`**  | **6x** | **1920x1344** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1248,48,32,80,1008,3,7,20,89203`** | **4.5x** | **1248x1008** | **3.25x** | **3** |

<br>

### Capcom CP System Hardware (CPS-1, CPS-Dash, CPS-2)

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtcps1**]<br>[**jtcps15**]<br>[**jtcps2**] | **8.00 MHz** | **59.629 Hz** | **384x224** | **12:7** | **1280:973** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1536,48,32,80,896,3,10,13,93243`**    | **4x** | **1536x896**  | **4x** |
**`video_mode=1920,48,32,80,1120,3,10,19,142881`**  | **5x** | **1920x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,25,171408`**  | **6x** | **1920x1344** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1248,48,32,80,1008,3,7,19,87065`** | **4.5x** | **1248x1008** | **3.25x** | **3** |

<br>
