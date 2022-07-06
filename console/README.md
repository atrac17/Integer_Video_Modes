
## Console & Handheld Video Modes & Timings

<br>

Integer scaled modelines based on the information below. The visible resolution may coincide with actual hardware or the FPGA implementation (_i.e. Gameboy, GameGear,PC Engine etc_).<br><br>The pixel clock, horizontal total, and vertical total have been measured for the first grouping, for the second it is based on the core implementation. Modeline timings based off the vertical refresh rate and visible resolution.<br><br>
If a core has `Dual Mode=Yes`, then there will only be one primary video mode available as the core supports multiple systems for one video mode. For custom aspect ratios, the first will be for the primary hardware and the other for the secondary hardware.<br><br>

<br>

| Title | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|
[**Atari 7800**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#atari-7800) | 7.159090 MHz | 59.965 Hz | 372x224 | 454x263 |
[**Nintendo Famicom**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#nintendo-famicom--nintendo-entertainment-system) | 5.369318 MHz | 60.098 Hz | 256x224<br>256x240 | 341x262 |
[**Nintendo Gameboy**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#game-boy--game-boy-color) | 4.194805 MHz | 59.723 Hz | 160x144 | 266x264 |
[**Nintendo Super Famicom**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#super-famicom--super-nintendo) | 5.369318 MHz<br>10.738636 MHz | 60.098 Hz | 256x224 / 256x240<br>512x224 / 512x240 | 341x262 / 682x262 |
[**Nintendo Gameboy Advance**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#game-boy-advance) | 6.293706 MHz | 59.713 Hz | 240x160 | 399x264 |
[**Sega SG-1000**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-sg-1000)<br>[**Sega Mark III**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mark-iii--sega-master-system-sega-sg-1000-compatible) | 5.3693175 MHz | 59.922 Hz | 256x192 | 342x262 |
[**Sega Mega Drive**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mega-drive--sega-genesis)<br>[Sega Mega CD](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mega-drive--sega-genesis)<br>[Sega Super 32x](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-mega-drive--sega-genesis) | 6.711647 MHz | 59.852 Hz | 320x224<br>256x224 | 428x262 |
[**Sega GameGear**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-game-gear) | 5.3693175 MHz | 59.922 Hz | 160x144 | 342x262 |
[**Sega Saturn**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sega-saturn) | 7.15909 MHz (lo-res)<br><br><br>14.31818 MHz (hi-res) | 59.826 Hz | 320x224 / 240<br>352x224 / 240<br><br>640x448i / 480i<br>704x448i / 480i | 455x263 / 910x263 |
[**SNK NeoGeo AES**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#neo-geo-advanced-entertainment-system) | 6.041957 MHz | 59.599 Hz | 320x224 | 384x264 |
[**Sony PlayStation**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#sony-playstation) | 5.369318 MHz (lo-res)<br>6.711647 MHz (lo-res)<br>7.670454 MHz (lo-res)<br><br>10.738636 MHz (hi-res)<br>13.423295 MHz (hi-res) | 59.826 Hz | 256x224<br>320x224<br>384x224<br>512x224<br><br>256x240<br>320x240<br>384x240<br>512x240<br><br>640x480i<br>704x480i | 487.5x263 for 7.670454 MHz |

<br>

| Title | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|
[**Atari Lynx**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#atari-lynx) | 7.11 MHz | 59.176 Hz | 160x102 | 445x270 |
[**Bandai WonderSwan**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#bandai-wonderswan--wonderswan-color) | 7.37 MHz | 75.371 Hz | 224x144 | 379x258 |
[**NEC PC Engine Duo**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/console/console.md#pc-engine-duo--turbo-duo) | 5.37 MHz<br>7.16 MHz<br>10.74 MHz | 60.106 Hz | 360x231 | 341x262 |

<br>
