
## Console & Handheld Video Modes & Timings

<br>

Integer scaled modelines based on the information below. The visible resolution may coincide with actual hardware or the FPGA implementation (_i.e. Gameboy, GameGear,PC Engine etc_). The pixel clock, horizontal total, and vertical total have been measured for the first grouping, for the second it is based on the core implementation. Modeline timings based off the vertical refresh rate and visible resolution.<br><br>
If a core has `Dual Mode=Yes`, then there will only be one primary video mode available as the core supports multiple systems for one video mode. For custom aspect ratios, the first will be for the primary hardware and the other for the secondary hardware.<br><br>

<br>

| Title | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|
[**Nintendo Famicom**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#nintendo-famicom--nintendo-entertainment-system) | 5.369318 MHz | 60.098 Hz | 256x224<br>256x240 | 341x262 |
[**Nintendo Super Famicom**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#super-famicom--super-nintendo) | 5.369318 MHz<br>10.738636 MHz | 60.098 Hz | 256x224 / 256x240<br>512x224 / 512x240 | 341x262 / 682x262 |
[**Sega SG-1000**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-sg-1000)<br>[**Sega Mark III**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-mark-iii--sega-master-system-sega-sg-1000-compatible) | 5.3693175 MHz | 59.922 Hz | 256x192 | 342x262 |
[**Sega Mega Drive**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-mega-drive--sega-genesis)<br>[Sega Mega CD](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-mega-drive--sega-genesis)<br>[Sega Super 32x](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-mega-drive--sega-genesis) | 6.711647 MHz | 59.852 Hz | 320x224<br>256x224 | 428x262 |
[**Sega GameGear**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-game-gear) | 5.3693175 MHz | 59.922 Hz | 160x144 | 342x262 |
[**Sega Saturn**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sega-saturn) | 7.15909 MHz (lo-res)<br><br><br>14.31818 MHz (hi-res) | 59.826 Hz<br><br><br>59.730 Hz | 320x224 / 240<br>352x224 / 240<br><br>640x448i / 480i<br>704x448i / 480i | 455x263 / 910x263 |
[**SNK NeoGeo AES**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#neo-geo-advanced-entertainment-system) | 6.041957 MHz | 59.599 Hz | 320x224 | 384x264 |
[**Sony PlayStation**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#sony-playstation) | 5.322240 MHz<br>6.652800 MHz<br>7.603200 MHz<br>10.644480 MHz<br>5.322240 MHz<br>13.305600 MHz | 59.800 Hz | 256x224<br>320x224<br>368x224<br>512x224<br>256x240<br>320x240<br>368x240<br>512x240<br>640x480i | 423x263 for 6.652800 Mhz |

<br>

| Title | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|
[**Atari 7800**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#atari-7800) | 7.16 MHz | 59.965 Hz | 372x224 | 454x263 |
[**Atari Lynx**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#atari-lynx) | 7.11 MHz | 59.176 Hz | 160x102 | 445x270 |
[**Bandai WonderSwan**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#bandai-wonderswan--wonderswan-color) | 7.37 MHz | 75.371 Hz | 224x144 | 379x258 |
[**NEC PC Engine Duo**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#pc-engine-duo--turbo-duo) | 5.37 MHz<br>7.16 MHz<br>10.74 MHz | 60.106 Hz | 360x231 | 341x262 |
[**Nintendo Gameboy**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#game-boy--game-boy-color) | 4.194 MHz | 59.723 Hz | 160x144 | 266x264 |
[**Nintendo Gameboy Advance**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/Update/console/console.md#game-boy-advance) | 6.29 MHz | 59.713 Hz | 240x160 | 399x264 |

<br>
