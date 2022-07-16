
## Arcade Video Modes & Timings

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and pixel clock, horizontal total, and vertical total have been measured. Modeline timings based off the vertical refresh rate and visible resolution. If a modeline for an arcade core is not provided below, it may be added in the future.

<br>

## [Capcom  Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/capcom.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**1942**<br><br>**1943**<br><br>**Black Tiger**<br><br>**Commando**<br><br>**Gun.Smoke**<br><br>**Pirate Ship Higemaru**<br><br>**Vulgus**<br><br>**Exed Exes** | Capcom Z80 | 6.00 MHz | 59.637 Hz | 256x224 | 384x262 |
**Hyper Dyne: Side Arms** | Capcom Z80<br>(Side Arms Based) | 8.00 MHz | 60.096 Hz | 384x224 | 512x260 |
**Section Z**<br><br>**Legendary Wings**<br><br>**Trojan** | Capcom Z80<br>(Section Z Based) | 6.00 MHz | 55.407 Hz<br><br>56.003 Hz | 256x240 | 384x282 / 279 |
**Ghosts 'n Goblins** | Capcom M6809 Based | 6.00 MHz | 59.637 Hz | 256x224 | 384x262 |
**The Speed Rumbler** | Capcom M6809 Based | 8.00 MHz | 57.444 Hz | 353x240 | 512x272 |
**Bionic Commando**<br><br>**F-1 Dream**<br><br>**Tiger Road** | Capcom M68000 Based | 6.00 MHz | 59.637 Hz | 256x224 | 384x262 |
**Street Fighter** | Capcom M68000 Based | 8.00 MHz | 61.035 Hz | 384x224 | 512x256 |
**CP System Hardware** | CP System<br><br>CP System Dash<br><br>CP System II | 8.00 MHz | 59.629 Hz (FPGA core) / 59.637 HZ (Calculation) | 384x224 | 512x262 |

<br>

## [Cave Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/cave.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Dangun Feveron**<br><br>**Donpachi**<br><br>**DoDonpachi**<br><br>**ESP Ra.De.**<br><br>**Puzzle Uo Poko**<br><br>**Gunwange** | Cave 68000<br>(240p Visible) | 7.00 MHz | 57.400 Hz | 320x240 | 450x271 |
**Gaia Crusaders**<br><br>**Thunder Heroes** | Cave 68000<br>(224p Visible) | 7.00 MHz | 57.400 Hz | 320x224 | 450x271 |

<br>

## [DataEast Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/data_east.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Bad Dudes vs Dragon Ninja**<br><br>**Birdie Try**<br><br>**Fighting Fantasy**<br><br>**Heavy Barrel**<br><br>**RoboCop**<br><br>**Stadium Hero** | DataEast MEC-M1 Based | 6.00 MHz | 57.407 Hz | 256x240 | 384x282 |
**Boulder Dash 2**<br><br>**Midnight Resistance**<br><br>**Sly Spy** | DataEast MEC-M1<br>(Midnight Resistance Based) | 6.00 MHz | 57.407 Hz | 256x240 | 384x282 |

<br>

## Irem Arcade Hardware

<br>

**Notes:**<br>
Irem M62 hardware has different horizontal resolutions set by jumpers on the actual PCB. Spanning from 256 to 384 horizontal. This information is based on schematics; I have purchased Kid Niki and Kung-Fu Master schematics to verify this information as they are no legible scans available.<br><br>256 horizontal video modes will result in a border for Kung Fu Master / Spartan X etc. but display the correct aspect ratio of 1:1. The core currently has the **incorrect vertical refresh rate and visible resolution**. 384x256 titles are notated by mameset in the `pre-configured .ini` files.

<br>

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Horizon**<br><br>**Kung-Fu Master**<br><br>**The Battle-Road**<br><br>**Youjyuden** | [**Irem M62<br>Based**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/irem_m62.md) | 6.144 MHz (lo-res) | 56.338 Hz | 256x256 | 384x284 |
**Kid Niki: Radical Ninja**<br><br>**Lode Runner**<br><br>**Lode Runner II: The Bungeling Strikes Back**<br><br>**Lode Runner III: Majin no Fukkatsu**<br><br>**Lode Runner IV: Teikoku Karano Dasshutsu**<br><br>**LotLot**<br><br>**Spelunker**<br><br>**Spelunker II: 23 no Kagi** | [**Irem M62<br>Based**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/irem_m62.md) | 8.00 MHz (hi-res)  | 55.017 Hz | 384x256 | 512x284 |
**Vigilante** | [**Irem M75 Based**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/irem_m75.md) | 6.144 MHz | 56.338 Hz | 256x256 | 384x284 |

<br>

## [Konami Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/konami.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Kicker**<br><br>**Mikie**<br><br>**Road Fighter**<br><br>**Super Basketball** | Konami M6809<br>(082/083, 503 Customs) | 6.144 MHz | 60.606 Hz | 224x256 | 264x384 |
**Hyper Sports**<br><br>**Konami's Ping Pong**<br><br>**Track & Field**<br><br>**Yie Ar Kung-Fu** | Konami M6809<br>(082/083, 503 Customs) | 6.144 MHz | 60.606 Hz | 256x224 | 384x264 |
**Contra**<br><br>**Fast Lane**<br><br>**Labrynth Runner** | Konami M6309<br>(007121 Custom) | 6.00 MHz | 59.185 Hz | 224x280 | 264x384 |
**Combat School**<br><br>**MX5000** | Konami M6309<br>(007121 Custom) | 6.00 MHz | 59.185 Hz | 280x224 | 384x264 |

<br>

## [Mitchell Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/mitchell.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Pang**<br><br>**Super Pang**<br><br>**Block Block** | Mitchell Z80 Based | 8.00 MHz | 56.338 Hz | 384x240 | 512x272 |

<br>

## [Nichibutsu Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/nichibutsu.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Terra Cresta**<br><br>**Sei Senshi Amatelass**<br><br>**Kid no Hore Hore Daisakusen** | Nichibutsu M68000 Terra Cresta Based | 6.00 MHz | 59.410 Hz | 256x224 | 384x263 |
**Terra Force**<br><br>**Kozure Ōkami**<br><br>**Chouji Meikyuu Legion**<br><br>**Crazy Climber 2**<br><br>**Armed F** | Nichibutsu M68000 Terra Force Based | 6.00 MHz | 58.950 Hz | 320x240<br><br>288x224 | 387x263 |

<br>

## Sega Arcade Hardware

<br>

**Notes:**<br>
Sega System E hardware implementation is shared with Sega Master System, custom video modes for this hardware are notated by mameset in the `pre-configured .ini` files.

<br>

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Sega System I<br><br> Sega System II** | [**Sega System I<br><br>Sega System II**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/sega_sys_I_II.md) | 5.00 MHz | 60.096 Hz | 256x224 | 320x260 |
**Sega System E** | [**Sega System E**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/sega_sys_e.md) | 5.37 MHz | 59.930 Hz | 256x192 | 342x262 |
**Sega System 16** | [**Sega System16A<br><br>Sega System16B**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/sega_sys_16.md) | 6.2937 MHz | 60.054 Hz | 320x224 | 400x262 |
**Sega Super Scaler HW:**<br>**OutRun**<br><br>**Super Hang-On**<br><br>**Turbo OutRun** | [**Sega OutRun Based**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/sega_outrun.md) | 6.2937 MHz | 60.054 Hz | 320x224 | 400x262 |

<br>

## SNK Arcade Hardware

<br>

**Notes:**<br>
Neo Geo Multi Video System hardware implementation is shared with NeoGeo Advanced Entertainment System, custom video modes for this hardware default to MVS in the `pre-configured .ini` files.<br><br>NeoGeo MVS titles are designed to run at 59.185 Hz, the NeoGeo AES has a crystal oscillator bringing the refresh rate closer to 59.64 Hz for compatibility. There may be minor differences in the game; you can use the unibios to run the game in AES mode without changing the native refresh rate.

<br>

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**NeoGeo Multi Video System** | [**NeoGeo MVS Based**](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/neogeo_mvs.md) | 6.00 MHz | 59.185 Hz | 320x224 | 384x264 |

<br>

## [Taito Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/taito.md)

<br>

**Notes:**<br>
Taito z80 based hardware FPGA implementations reflect a vertical of 225 pixels, the hardware is 224. Currently, the video modes coincide with the resolution provided by the FPGA implementation for proper scaling. The pixel clock and timings are correct in these implementations.

<br>

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Arkanoid**<br><br>**Bubble Bobble**<br><br>**Tokio** | Taito Z80 Based | 6.00 MHz | 59.185 Hz | 256x224 (Hardware)<br>256x225 (FPGA Core) | 384x264 |
**Rastan** | Taito M68000 Based | 6.677 MHz | 59.876 Hz | 320x240 | 424x263 |

<br>

## [Technos Arcade Hardware](https://github.com/atrac17/MiSTer_Integer_Modelines/blob/main/arcade/technos.md)

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Double Dragon**<br><br>**Double Dragon II: The Revenge** | Technos 6309 Based | 6.00 MHz | 57.444 Hz | 256x232 | 384x272 |

<br>

## Toaplan Arcade Hardware

| Title | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) | Resolution (Total) |
|:--|:--:|:--:|:--:|:--:|:--:|
**Tatsujin**<br>**Vimana**<br>**Fire Shark**<br>**Zero Wing**<br>**Hellfire** | Toaplan V1 Based | 7.00 MHz | 57.613 Hz | 320x240 | 450x270 |
**OutZone**<br>**Dash Yarou**<br>**Horror Story** | Toaplan V1 Based | 7.00 MHz | 55.161 Hz | 320x240 | 450x282 |

<br>
