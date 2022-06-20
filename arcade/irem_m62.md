
# Custom Video Mode Information for Irem Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with the core resolution which is **incorrect**. The actual hardware and pxlclk/htotal/vtotal have been measured for an active area of 256x256 on Kung-Fu Master / Spartax-X. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Irem Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**a.iremm62**] | Irem M62 Based | 6.144 MHz (lo-res) | 56.338 Hz | 256x256 |
[**a.iremm62**] | Irem M62 Based | 8.00 MHz (hi-res)  | 55.017 Hz | 384x256 |

<br>

## Irem M62:<br><br>Horizon<br>Kaiketsu Yanchamaru / Kid Niki: Radical Ninja<br>Spartan-X / Kung-Fu Master<br>Lode Runner<br>Lode Runner II: The Bungeling Strikes Back<br>Lode Runner III: Majin no Fukkatsu<br>Lode Runner IV: Teikoku Karano Dasshutsu<br>Rotto Rotto / LotLot<br>Spelunker<br>Spelunker II: 23 no Kagi<br>The Battle-Road<br>Youjyuden

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**a.iremm62**] | **6.144 MHz** | **56.338 Hz** | **256x256** | **1:1** | **1:1** |
[**a.iremm62**] | **8.00 MHz**  | **55.017 Hz** | **384x256** | **3:2** | **160:139** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (lo-res) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,1024,3,10,15,70173`**   | **4x** | **1024x1024** | **4x** |
**`video_mode=1280,48,32,80,1280,3,10,22,106682`**  | **5x** | **1280x1280** | **5x** |
**`video_mode=1536,48,32,80,1536,3,10,28,150682`**  | **6x** | **1536x1536** | **6x** |

<br>

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution (hi-res) | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1536,48,32,80,1024,3,10,14,98068`**   | **4x** | **1536x1024** | **4x** |
**`video_mode=1920,48,32,80,1280,3,10,21,106682`**  | **5x** | **1920x1280** | **5x** |
**`video_mode=1920,48,32,80,1536,3,7,30,180351`**   | **6x** | **1920x1536** | **5x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1024,3,7,18,85346`** | **4x** | **1280x1024** | **5x** | **1** |

<br>
