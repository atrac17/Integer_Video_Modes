
# Console & Handheld Core Video Modes

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|
[Atari 7800](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#atari-7800) | 7.159090 MHz | 59.965 Hz | 372x224 |
[Atari Lynx](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#atari-lynx) | 7.11 MHz | 59.176 Hz | 160x102 |
[Bandai WonderSwan](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#bandai-wonderswan--wonderswan-color) | 7.37 MHz | 75.371 Hz | 224x144 |
[NEC PC Engine Duo](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#pc-engine-duo--turbo-duo) | 5.37 MHz<br>7.16 MHz<br>10.74 MHz | 60.106 Hz | 360x231 |
[Nintendo Famicom](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#nintendo-famicom--nintendo-entertainment-system) | 5.369318 MHz | 60.098 Hz | 256x224<br>256x240 |
[Nintendo Gameboy](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#game-boy--game-boy-color) | 4.194805 MHz | 59.723 Hz | 160x144 |
[Nintendo Super Famicom](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#super-famicom--super-nintendo) | 5.369318 MHz<br>10.738636 MHz | 60.098 Hz | 256x224 / 256x240<br>512x224 / 512x240 |
[Nintendo Gameboy Advance](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#game-boy-advance) | 6.293706 MHz | 59.713 Hz | 240x160 |
[Sega SG-1000](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-sg-1000)<br>[**Sega Mark III**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mark-iii--sega-master-system-sega-sg-1000-compatible) | 5.3693175 MHz | 59.922 Hz | 256x192 |
[**Sega Mega Drive**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mega-drive--sega-genesis)<br>[Sega Mega CD](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mega-drive--sega-genesis)<br>[Sega Super 32x](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mega-drive--sega-genesis) | 6.711647 MHz | 59.852 Hz | 320x224<br>256x224 |
[**Sega GameGear**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-game-gear) | 5.3693175 MHz | 59.922 Hz | 160x144 | 342x262 |
[**Sega Saturn**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-saturn) | 7.15909 MHz (lo-res)<br><br><br>14.31818 MHz (hi-res) | 59.826 Hz | 320x224 / 240<br>352x224 / 240<br><br>640x448i / 480i<br>704x448i / 480i | 455x263 / 910x263 |
[**SNK NeoGeo AES**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#neo-geo-advanced-entertainment-system) | 6.041957 MHz | 59.599 Hz | 320x224 | 384x264 |
[**Sony PlayStation**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sony-playstation) | 5.369318 MHz (lo-res)<br>6.711647 MHz (lo-res)<br>7.670454 MHz (lo-res)<br><br>10.738636 MHz (hi-res)<br>13.423295 MHz (hi-res) | 59.826 Hz | 256x224<br>320x224<br>384x224<br>512x224<br><br>256x240<br>320x240<br>384x240<br>512x240<br><br>640x480i<br>704x480i | 487.5x263 for 7.670454 MHz |

<br>

# Atari Hardware

## Atari 7800

### Notes:<br>
The Atari 7800 hardware utilizes a low-res pixel clock (3.58 MHz) as well. The timings provided below cover all the resolution switching for an HDMI display. 

The visible resolution in this core does not correspond with the actual hardware due to resolution switching and backwards compatibility with Atari 2600.

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**atari7800**] | **7.159090 MHz** | **59.965 Hz** | **372x224** | **93:56** | **3720:2611** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1488,48,32,80,896,3,7,16,91115`**    | **4x** | **1488x896**  | **4x** |
**`video_mode=1860,48,32,80,1120,3,7,22,139541`**  | **5x** | **1860x1120** | **5x** |
**`video_mode=1860,48,32,80,1344,3,10,26,167522`** | **6x** | **1860x1344** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1208,48,32,80,1008,3,10,16,85068`** | **4.5x** | **1280x1008** | **3.25x** | **3** |

## Atari Lynx

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**atarilynx**] | **7.11 MHz** | **59.176 Hz** | **160x102** | **80:51** | **4519:3340** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1440,48,32,80,918,3,6,18,89380`**    | **9x**  | **1440x918**  | **9x**  |
**`video_mode=1600,48,32,80,1020,3,6,20,109254`**  | **10x** | **1600x1020** | **10x** |
**`video_mode=1760,48,32,80,1122,3,10,19,131116`** | **11x** | **1760x1122** | **11x** |
**`video_mode=1920,48,32,80,1224,3,10,22,154966`** | **12x** | **1920x1224** | **12x** |
**`video_mode=1920,48,32,80,1326,3,10,25,167890`** | **13x** | **1920x1326** | **12x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1020,3,7,19,89389`** | **10x** | **1280x1020** | **8x** |**1** |

<br>
<br>
<br>

# Bandai Hardware

## Bandai WonderSwan / WonderSwan Color

### Notes:<br>
The WonderSwan hardware utilizes a refresh rate of 75 Hz. The video modes below have a pixel clock that corresponds to 75Hz and the video modes below may be out of range for your display. Ensure to check compatibility.

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**wonderswan**] | **7.37 MHz** | **75.371 Hz** | **224x144** | **14:9** | **35:27**|

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1568,48,32,80,1008,3,10,24,136102`** | **7x**  | **1568x1008** | **7x** |
**`video_mode=1792,48,32,80,1152,3,10,29,175667`** | **8x**  | **1792x1152** | **8x** |
**`video_mode=2016,48,32,80,1296,3,10,34,220262`** | **9x**  | **2016x1296** | **9x** |
**`video_mode=2016,48,32,80,1440,3,10,39,244699`** | **10x** | **2016x1440** | **9x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1232,48,32,80,1008,3,10,24,109638`** | **5.5x** | **1232x1008** | **7x** | **2** |

<br>
<br>
<br>

# NEC Hardware

## PC Engine Duo / Turbo Duo

### Notes:<br>
The NEC PC Engine Duo hardware utilizes multiple pixel clocks and resolutions. The timings provided below cover all the resolution switching for an HDMI display. 

The visible resolution in this core does not correspond with the actual hardware due to resolution switching which can vary from 256×224 to 512×242 and pixel clock changes on the VDC. 

The Display Aspect Ratio is calculated off resolutions 256x239 (5.37 to 7.16 pxl clock) and 512x242 (10.74 pxl clock).

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**tgfx16**] | **5.37 MHz**<br>**7.16 MHz**<br>**10.74 MHz** | **60.106 Hz** | **360x231** | **8:7**<br>**6:7**<br>**4:7** | **2048:1673**<br>**1961:2134**<br>**1024:847** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1440,48,32,80,924,3,10,14,91458`**   | **4x** | **1440x924**  | **4x** |
**`video_mode=1800,48,32,80,1155,3,10,20,139956`** | **5x** | **1800x1155** | **5x** |
**`video_mode=1800,48,32,80,1386,3,10,27,167994`** | **6x** | **1800x1386** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1260,48,32,80,982,3,10,15,86205`** | **4.25x** | **1260x982** | **3.5x** | **3** |

<br>
<br>
<br>

# Nintendo Hardware

## Nintendo Famicom / Nintendo Entertainment System

### Notes:<br>
The Nintendo Famicom / Nintendo Entertainment System utilizes two different vertical resolutions. Enable the following below to remove the visible overscan area and force 224p.

_**Hide Overscan: Yes**_<br>
_**Mask Edges: Auto**_

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**nes**] | **5.37 MHz** | **60.098 Hz** | **256x224**<br>**256x240** | **8:7**<br>**16:15** | **64:49**<br>**128:105**

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (224) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79791`**   | **4x** | **1280x896**  | **5x** |
**`video_mode=1536,48,32,80,1120,3,10,19,117419`** | **5x** | **1536x1120** | **6x** |
**`video_mode=1792,48,32,80,1344,3,4,32,162242`**  | **6x** | **1792x1344** | **7x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (240) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85503`**    | **4x** | **1280x960**  | **5x** |
**`video_mode=1536,48,32,80,1200,3,10,22,125879`** | **5x** | **1536x1200** | **6x** |
**`video_mode=1792,48,32,80,1440,3,10,28,173739`** | **6x** | **1792x1440** | **7x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89744`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>
<br>
<br>

## Game Boy / Game Boy Color

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**gameboy**] | **4.194805 MHz** | **59.723 Hz** | **160x144** | **10:9** | **3200:1971** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1120,48,32,80,1008,3,10,16,79274`**  | **7x**  | **1120x1008** | **7x** |
**`video_mode=1280,48,32,80,1152,3,10,20,101912`** | **8x**  | **1280x1152** | **8x** |
**`video_mode=1440,48,32,80,1296,3,10,24,127378`** | **9x**  | **1440x1296** | **9x** |
**`video_mode=1600,48,32,80,1440,3,10,28,155672`** | **10x** | **1600x1440** | **10x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89184`** | **7x** | **1280x1008** | **8x** | **1** |

<br>
<br>
<br>

## Super Famicom / Super Nintendo

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**snes**] | **5.37 MHz**<br>**10.47 MHz** | **60.098 Hz** | **256x224 / 256x240**<br>**512x224 / 512x240**| **8:7**<br>**16:7** | **64:49**<br>**128:105** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (224) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79797`**   | **4x** | **1280x896**  | **5x** |
**`video_mode=1536,48,32,80,1120,3,10,19,117419`** | **5x** | **1536x1120** | **6x** |
**`video_mode=1792,48,32,80,1344,3,4,32,162242`**  | **6x** | **1792x1344** | **7x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (240) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85503`**    | **4x** | **1280x960**  | **5x** |
**`video_mode=1536,48,32,80,1200,3,10,22,125879`** | **5x** | **1536x1200** | **6x** | 
**`video_mode=1792,48,32,80,1440,3,7,31,173739`** | **6x** | **1792x1440** | **7x** | 

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89744`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>
<br>
<br>

## Game Boy Advance

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**gba**] | **6.293706 MHz** | **59.713 Hz** | **240x160** | **3:2** | **60:41** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1440,48,32,80,960,3,10,15,94395`**   | **6x** | **1440x960**  | **6x** |
**`video_mode=1680,48,32,80,1120,3,10,19,126573`** | **7x** | **1680x1120** | **7x** |
**`video_mode=1920,48,32,80,1280,3,10,24,163576`** | **8x** | **1920x1280** | **8x** |
**`video_mode=1920,48,32,80,1440,3,4,34,183945`**  | **9x** | **1920x1440** | **8x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1256,48,32,80,1015,3,7,19,88274`** | **7.25x** | **1256x1015** | **5.25x** |**3** |

<br>
<br>
<br>

# Sega Hardware

## Sega SG-1000 / Sega Mark III / Sega Master System (Sega SG-1000 Compatible)

### Notes:<br>
The Sega Mark III / Sega Master System core also launches SG-1000 and GameGear titles. The dual mode compatible modeline corresponds with SG-1000, Mark III, Master System, and GameGear resolutions.

The recommended integer scale is a factor of two, this is a personal preference. The dual mode compatible modeline equates to 5x integer scale and may not resolve filters properly on your display.

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**sms**]<br><br>[**coleco**] |**5.3693175 MHz** | **59.922 Hz** | **256x192** | **4:3** | **32:21** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal | Dual Mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85253`**   | **5x** | **1280x960**  | **5x** | **No**  |
**`video_mode=1536,48,32,80,1152,3,4,26,120429`** | **6x** | **1536x1152** | **6x** | **Yes** |
**`video_mode=1792,48,32,80,1344,3,4,32,161767`** | **7x** | **1792x1344** | **7x** | **No**  |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89481`** | **5.25x** | **1008p** | **5x** | **3** |

<br>
<br>
<br>

## Sega Mega Drive / Sega Genesis

### Notes:<br>
The **Mega CD** and **Super 32x** are additional addon hardware for the Mega Drive. The visible resolution is 320x224 and all use the same pixel clock. Modelines for 256x224 only apply to the Mega Drive core.

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**genesis**]<br>[**megacd**]<br>[**s32x**] | **6.711647 MHz**<br>**5.3693175 MHz** | **59.852 Hz**<br>**59.922 Hz** | **320x224**<br>**256x224** | **10:7**<br>**8:7** | **64:49** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal (320) |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79465`**   | **4x** | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,121352`** | **5x** | **1600x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,172173`** | **6x** | **1920x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal (256) |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,65414`**   | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,19,99404`**  | **5x** | **1280x1120** | **5x** |
**`video_mode=1536,48,32,80,1344,3,10,26,140552`** | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89376`** | **4.5x** | **1280x1008** | **4x** | **2** |

<br>
<br>
<br>

## Sega Game Gear

### Notes:<br>
These modelines are for the GameGear titles. The "dual mode" compatible modeline corresponds with SG-1000, Mark III, Master System, and GameGear resolutions.

The recommended integer scale is a factor of two, this is a personal preference. The dual mode compatible modeline equates to 5x integer scale and may not resolve filters properly on your display.

<br>

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**sms**] | **5.3693175 MHz** | **59.922 Hz** | **160x144** | **10:9** | **80:63** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal | Dual Mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1120,48,32,80,1008,3,10,16,79642`**  | **7x**  | **1120x1008** | **7x**   | **No**  |
**`video_mode=1280,48,32,80,1152,3,10,20,102384`** | **8x**  | **1280x1152** | **8x**   | **No**  |
**`video_mode=1536,48,32,80,1152,3,4,26,120586`**  | **8x**  | **1536x1152** | **9.6x** | **Yes** |
**`video_mode=1440,48,32,80,1296,3,10,24,127968`** | **9x**  | **1440x1296** | **9x**   | **No**  |
**`video_mode=1600,48,32,80,1440,3,10,28,156394`** | **10x** | **1600x1440** | **9x**   | **No**  |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | **5.25x** | **256x192** | **5x** | **3** |

<br>
<br>
<br>

## Sega Saturn

### Notes:<br>
The Sega Saturn is mislabeled with a native vertical refresh of 59.8Hz or 60.0Hz with emulation. 
These modelines correspond to the pixel clocks listed below and are derived from official Sega documentation.

To circumvent the horizontal change between games, I recommend using a 352px wide horizontal mode and provide the correct custom aspect ratio for a 320px wide horizontal mode to adjust when switching titles in the OSD.

<br>

| Core | Pixel Clock | Refresh Rate |Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**saturn**] | **7.159 MHz (lo-res)**<br><br><br>**14.31818 MHz (hi-res)** | **59.826 Hz** | **320x224 / 240**<br>**352x224 / 240**<br><br>**640x448i / 480i**<br>**704x448i / 480i** | **10:7 / 4:3**<br>**11:7 / 22:15** | **3200:2611 / 1280:1119**<br>**3520:2611 / 1408:1119** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (224) | Horizontal (320) |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79430`**    | **4x**  | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,121299`**  | **5x**  | **1600x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,172098`**  | **6x**  | **1920x1344** | **6x** |
**`video_mode=1408,48,32,80,896,3,6,17,86491`**     | **4x**  | **1408x896**  | **4x** |
**`video_mode=1760,48,32,80,1120,3,6,23,132326`**   | **5x**  | **1760x1120** | **5x** |
**`video_mode=1760,48,32,80,1344,3,4,32,158860`**   | **6x**  | **1760x1344** | **5x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (240) | Horizontal (352) |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85116`**     | **4x**  | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,27,129933`**   | **5x**  | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,34,184293`**   | **6x**  | **1920x1440** | **6x** |
**`video_mode=1408,48,32,80,960,3,10,15,92682`**    | **4x**  | **1408x960**  | **4x** |
**`video_mode=1760,48,32,80,1200,3,10,21,141745`**  | **5x**  | **1760x1200** | **5x** |
**`video_mode=1760,48,32,80,1440,3,10,28,170117`**  | **6x**  | **1760x1440** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1232,48,32,80,1008,3,10,16,86360`** | **4.5x** | **1232x1008** | **3.5x** | **2** |

<br>
<br>
<br>

# SNK Hardware

## Neo Geo Advanced Entertainment System

| Core | Pixel Clock | Refresh Rate |Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**neogeo**] | **6.041957 MHz** | **59.599 Hz** | **320x224** | **10:7** | **640:441** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79129`**    | **4x** | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,120839`**  | **5x** | **1536x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,25,171321`**  | **6x** | **1920x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,88998`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>
<br>
<br>

# Sony Hardware

## Sony PlayStation

| Core | Pixel Clock | Refresh Rate |Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--:|:--:|:--:|:--:|:--:|:--:|
[**psx**] | **5.369318 MHz (lo-res)<br>6.711647 MHz (lo-res)<br>7.670454 MHz (lo-res)<br><br>10.738636 MHz (hi-res)<br>13.423295 MHz (hi-res)** | **59.826 Hz** | **256x224**<br>**320x224**<br>**384x224**<br>**512x224**<br>**256x240**<br>**320x240**<br>**384x240**<br><br>**512x240**<br>**640x480i**<br>**704x480i** | **4:3**<br>**10:7**<br>**12:7**<br>**8:7**<br>**56:45**<br>**4:3**<br>**23:18**<br>**8:5**<br>**4:3** | **1280:973**<br>**3200:2429**<br>**920:693**<br>**1024:777**<br>**512:417**<br>**1280:1041**<br>**368:297**<br>**2048:1665**<br>**1280:1041** |

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (224) | Horizontal (320) |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,896,3,10,13,79430`**   | **4x** | **1280x896**  | **4x** |
**`video_mode=1600,48,32,80,1120,3,10,19,121299`** | **5x** | **1600x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,172098`** | **6x** | **1920x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (240) | Horizontal (320) |
|:--|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,960,3,4,21,85116`**    | **4x** | **1280x960**  | **4x** |
**`video_mode=1600,48,32,80,1200,3,4,27,129933`**  | **5x** | **1600x1200** | **5x** |
**`video_mode=1920,48,32,80,1440,3,4,34,184293`**  | **6x** | **1920x1440** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,89337`** | **4.75x** | **1280x1008** | **5x** | **3** |
**`video_mode=1280,48,32,80,1020,3,7,19,90371`** | **4.25x** | **1280x1020** | **5x** | **3** |
