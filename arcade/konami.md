
# Custom Video Mode Information for Konami Arcade Hardware

<br>

Integer scaled modelines based on the information below. The visible resolution coincides with actual hardware and the pxlclk/htotal/vtotal have been measured. Timings based off the vertical refresh rate (calculated pxlclk/htotal/vtotal) and visible resolution.

<br>

# Konami Hardware

| Core | Hardware | Pixel Clock | Refresh Rate | Resolution (Visible) |
|:--|:--:|:--:|:--:|:--:|
[**jtbaskt**]<br>[**jtkicker**]<br>[**jtmikie**]<br>[**jtroadf**] | Konami M6809 Based<br>(082, 083, 503 Konami Customs) | 6.144 MHz | 60.606 Hz | 224x256 |
[**jtpinpon**]<br>[**jtroadf**]<br>[**jttrack**]<br>[**jtyiear**] | Konami M6809 Based<br>(082, 083, 503 Konami Customs) | 6.144 MHz | 60.606 Hz | 256x224 |
[**jtcontra**]<br>[**jtflane**]<br>[**jtlabrun**] | Konami (6309<br>00712 Based) | 6.00 MHz | 59.185 Hz | 224x280 |
[**jtcomsc**]<br>[**jtmx5k**] | Konami (6309<br>00712 Based) | 6.00 MHz | 59.185 Hz | 280x224 |

<br>

## Konami (6809 / 082, 083, 503 Based) Hardware

### Hyper Sports / Hyper Olympics '84<br>Shao-Lin's Road / Kicker<br>Shinnyū Shain Tōru-kun / Mikie<br>Ping Pong<br>Road Fighter<br>Super Basketball<br>Hyper Olypic / Track & Field<br>Yie Ar Kung-Fu

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtyiear**]<br>[**jttrack**]<br>[**jtpinpon**]<br>[**jtroadf**] | **6.144 MHz** | **60.606 Hz** | **256x224** | **8:7** | **8:7** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1024,48,32,80,896,3,10,13,66161`**    | **4x** | **1024x896**  | **4x** |
**`video_mode=1280,48,32,80,1120,3,10,20,100626`**  | **5x** | **1280x1120** | **5x** |
**`video_mode=1920,48,32,80,1344,3,10,26,142156`**  | **6x** | **1536x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1280,48,32,80,1008,3,7,19,90502`** | **4.5x** | **1280x1008** | **5x** | **2** |

<br>

## Konami (6309 / 00712 Based) Hardware

### Contra<br>Boot Camp / Combat School<br>Fast Lane<br>Trick Trap / Labyrinth Runner<br>Flak Attack / MX5000

| Core | Pixel Clock | Refresh Rate | Resolution (Visible) | Pixel Aspect Ratio | Display Aspect Ratio |
|:--|:--:|:--:|:--:|:--:|:--:|
[**jtcontra**]<br>[**jtflane**]<br>[**jtlabrun**] | **6.00 MHz** | **59.185 Hz** | **224x280** | **4:5** | **256:313** |
[**jtcomsc**]<br>[**jtmx5k**] | **6.00 MHz** | **59.185 Hz** | **280x224** | **5:4** | **400:313** |

<br>

### Video Modes:

| CVT-RB Standard NTSC Modelines (HDTV) | Integer | Resolution | Horizontal |
|:--|:--:|:--:|:--:|
**`video_mode=1120,48,32,80,896,3,7,16,69848`**    | **4x** | **1120x896**  | **4x** |
**`video_mode=1400,48,32,80,1120,3,7,22,106363`**  | **5x** | **1400x1120** | **5x** |
**`video_mode=1680,48,32,80,1344,3,7,28,150501`**  | **6x** | **1680x1344** | **6x** |

<br>

| CVT-RB Standard NTSC Modeline (LCD Integer-Step Scaled) | Integer | Resolution | Horizontal | vscale_mode |
|:--|:--:|:--:|:--:|:--:|
**`video_mode=1260,48,32,80,1008,3,7,19,87153`** | **4.5x** | **1260x1008** | **5x** | **2** |

<br>
