
![logo](https://user-images.githubusercontent.com/32810066/128452226-e23e1552-abb7-434b-92e1-b4b35a23a5af.png)

# Repository information

- This pre-release repository contains custom video modes for use with MiSTer FPGA cores.

- Due to time constraints, I will periodically update the video modes available for FPGA cores from their respective repositories once this enters a public release.

- Like the rest of this repository, all of this documentation is a work in progress.  Feel free to contribute to documentation improvements by sending me a pull request.

# What are these for?

- MiSTer provides only two standard ways to scale the image up to a high-resolution modern display, and each way has its problems:

  - Integer scaling yields pixel-perfect upscaling, but it also means the image can't fill your display's full height.
  - Non-integer scaling fills the screen height, but it introduces very annoying artifacts (uneven scanlines, "shimmering" during vertical scrolling, etc).

- Using a non-standard video mode effectively produces hybrid scaling, to give you the best of both worlds:

  - MiSTer integer-scales the content up to the full height of our custom video mode (defined as a perfect integer size of the original content), to feed the display the largest perfect image possible.
  - The display non-integer-scales that image the rest of the way up to fill the entire screen height.
  - The amount of non-integer scaling is minimized, so the annoying scaling imperfections are drastically reduced, to the point of being unnoticeable.

- But like everything in life, there are some catches:
  - Not all displays are compatible with all non-standard video modes.  Your display may not accept all or any of them.  I have no control over this.
  - Displays that support Variable Refresh Rate (VRR), G-Sync, or FreeSync are more likely to be compatible.
  - As you run different cores/content, the MiSTer framework can automatically change only the horizontal resolution.  It cannot automatically change the vertical resolution, so we must define our own custom video mode for each specific core/content.

- Please read all provided information thoroughly.  See the F.A.Q. for further assistance.


# What is provided?

- Information about custom video modes:
  - Modes designed for 4k televisions, 2048x1536p (iPad Displays), 1440p monitors, and 1080p monitors that upscale the provided resolution from the DE-10 Nano.
  - Modes designed for 1280x1024 LCD displays.
  - Modes designed for common VGA CRT monitors.

- Preconfigured MiSTer.ini files containing sensibly-grouped sets of the aforementioned custom video modes.

# How do I get them?

These custom modelines are not yet retrieved by the popular `update_all.sh` updater script.  For now, you'll need to manually download the .ini files from this repo or using `git clone` to make a local copy of it.

# MiSTer.ini Information

- The default display resolution for the MiSTer.ini is set to 720p when utilizing custom video modes. Each core will be `vscale_mode=1` and `vsync_adjust=2`. Integer Step-Scaled Video Modes will specify the `vscale_mode`.

- Due to the horizontal limitation of 2048 within cores, some video modes will utilize -1x for the horizontal scale. This will not affect the aspect ratio on your display if it's scaler takes advantage of the video mode provided. This is not a universal catch all. These are custom and display dependent.

- Integer-Step Scaled video modes are available for 1280x1024 LCD displays and common VGA CRT monitors with the same resolution; different video mode is provided. Video modes for VGA CRT monitors will utilize `vga_scaler=1`.

- When utilizing Integer-Step Scaled video modes set the `aspect ratio: full screen` in the MiSTer OSD. This properly displays the provided custom video mode. If you are using a common VGA CRT monitor, you can stretch the horizontal and vertical to fill the screen in the displays OSD in the monitors settings.

- If a core has `Dual Mode=Yes`, then there will only be one primary video mode available as the core supports multiple systems for one video mode. For custom aspect ratios, the first will be for the primary hardware and the other for the secondary hardware.

# Compatible Display List


- The Compatible Display List for this repository is currently a work in progress, just like the repository itself. This is currently a pre-release and more information regarding compatible displays will be added in the future.

- If you have a display that correctly resolves these custom video modes, please create an issue within the repository and provide the compatible resolutions, make, model, firmware (where applicable), and general information on how you resolve the proper aspect ratio on the display and I will add it to the repository.

<details>

<summary><b>2048x1536 QXGA 9.7" Displays</b></summary>

<blockquote>

- <summary><b>Display Panel Information:</b></summary>

|Display Model|Driver Board|Resolution (Native)|Resolution (Scaled)|VRR Capable|
|--|--|--|--|--|
**SAMSUNG LTN097QL01-A03** | **VS-RTD09703-V1** | **2048x1536**| **4x to 6x** | **Yes** |

</details>

<details>

<summary><b>4K Televisions</b></summary>

<blockquote>

- <summary><b>Compatibility information:</b></summary>

|Display Model|Resolution (Scaled)|VRR Capable|Notes
|--|--|--|--|
**Vizio P65QX-H1** | **4x to 6x** | **Yes** | Accepts custom resolutions, but only stable with `vsync_adjust=0` |

</details>

<details>

<summary><b>1440p Monitors</b></summary>

<blockquote>

- <summary><b>Compatibility information:</b></summary>

|Display Model|Panel Type|Resolution (Scaled)|VRR Capable|Notes
|--|--|--|--|--|
**LG 32QN600-B** | **IPS** | **4x to 6x** | **Yes** | Limited to 75Hz - support up to WonderSwan |
**LG 32QN55T-B** | **IPS** | **4x to 6x** | **Yes** | Limited to 75Hz - support up to WonderSwan |
**LG 32GN600-B** | **VA** | **4x to 6x** | **Yes** | |
**LG 32GN650-B** | **VA** | **4x to 6x** | **Yes** | |
**LG 32GK650F-B** | **VA** | **4x to 6x** | **Yes** | |
**LG 32GN63T-B** | **VA** | **4x to 6x** | **Yes** | Recommended Monitor (atrac17) |
**LG 27GN800-B** | **IPS** | **4x to 6x** | **Yes** | Recommended Monitor (atrac17) |

</details>

----

# Custom Video Mode Information

### Custom Video Modes:

<details>

<summary><b>Arcade Core Video Modes <a href="https://www.github.com/jotego">(Jotego)</a></b></summary>

<details>

_<summary><b>Capcom Hardware</b></summary>_

## <summary1><b>Capcom Z80 Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![0](https://user-images.githubusercontent.com/32810066/129500200-84051e5b-8ba4-409d-82f4-7640de618638.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **59.640000000 Hz NTSC** | **256x224**| **45:44** | **2560:2191**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,896,3,10,13,65499`** | [**jt1942**] [**jt1943**] [**jtbtiger**] [**jtcom**] [**jtgun**] [**jthige**] [**jtvulgus**] [**jtexes**] | **256x224**| **1024x896** | **4x** | **896p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1120,3,10,19,99533`** | [**jt1942**] [**jt1943**] [**jtbtiger**] [**jtcom**] [**jtgun**] [**jthige**] [**jtvulgus**] [**jtexes**] | **256x224**| **1280x1120** | **5x** | **1120p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1344,3,10,25,140632`** | [**jt1942**] [**jt1943**] [**jtbtiger**] [**jtcom**] [**jtgun**] [**jthige**] [**jtvulgus**] [**jtexes**] | **256x224**| **1536x1344** | **6x** | **1344p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**jt1942**] [**jt1943**] [**jtbtiger**] [**jtcom**] [**jtgun**] [**jthige**] [**jtvulgus**] [**jtexes**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **No** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**jt1942**] [**jt1943**] [**jtbtiger**] [**jtcom**] [**jtgun**] [**jthige**] [**jtvulgus**] [**jtexes**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

### <summary2><b>Hardware Information for:</b></summary2>

![10](https://user-images.githubusercontent.com/32810066/126890889-8628b3eb-1967-4b7f-bd7a-5ca45237e016.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.000 MHz** | **61.000000000 Hz NTSC** | **384x224**| **135:176** | **1280:973**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,896,3,10,13,93823`** | [**jtsarms**] | **384x224**| **1536x896** | **4x** | **896p** | **1536 (4x)** |
**`video_mode=1920,48,32,80,1120,3,10,20,143894`** | [**jtsarms**] | **384x224**| **1920x1120** | **5x** | **1120p** | **1920 (5x)** |
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**jtsarms**] | **384x224**| **1920x1344** | **6x / 5x (Hor.)** | **1344p** | **1920 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1248,48,32,80,1008,3,10,16,87606`** | [**jtsarms**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3** | **No** |
**`video_mode=1248,80,128,208,1008,3,10,26,104532`** | [**jtsarms**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3** | **1** |

## <summary1><b>Capcom M6809 Hardware</b></summary1>

### <summary2><b>Hardware Information for:</b></summary2>

![6](https://user-images.githubusercontent.com/32810066/126888618-87a76780-c1e6-418f-8e33-e569e36dd2ee.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **59.640000000 Hz NTSC** | **256x224**| **45:44** | **2560:2191**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>  
  
|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,896,3,10,13,65499`** | [**jtgng**] | **256x224**| **1024x896** | **4x** | **896p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1120,3,10,19,99533`** | [**jtgng**] | **256x224**| **1280x1120** | **5x** | **1120p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1344,3,10,26,140734`** | [**jtgng**] | **256x224**| **1536x1344** | **6x** | **1344p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**jtgng**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**jtgng**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

### <summary2><b>Hardware Information for:</b></summary2>

![7](https://user-images.githubusercontent.com/32810066/126888629-e5223547-a39c-49c5-b70b-db337915a2c6.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.000 MHz** | **57.440000000 Hz NTSC** | **352x240**| **135:176** | **1408:1251**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1056,48,32,80,960,3,10,14,72012`** | [**jtrumble**] | **352x240**| **1056x960** | **4x** | **960p** | **1056 (3x)** |
**`video_mode=1408,48,32,80,1200,3,10,20,116001`** | [**jtrumble**] | **352x240**| **1408x1200** | **5x** | **1200p** | **1408 (4x)** |
**`video_mode=1760,48,32,80,1440,3,10,27,170496`** | [**jtrumble**] | **352x240**| **1760x1440** | **6x/5x (Hor.)** | **1440p** | **1760 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1232,48,32,80,1020,3,10,15,87529`** | [**jtrumble**] | **352x240**| **1232x1020** | **4.25x** | **1020p** | **1232 (3.5x)** | **3** |
**`video_mode=1232,72,128,200,1020,3,10,24,103501`** | [**jtrumble**] | **352x240**| **1232x1020** | **4.25x** | **1020p** | **1232 (3.5x)** | **3** | **1** |

## <summary1><b>Capcom Z80 (SectionZ) Hardware</b></summary1>

### <summary2><b>Hardware Information for:</b></summary2>

![8](https://user-images.githubusercontent.com/32810066/126889323-a7d6bcd1-d230-4c99-b6bf-ce9a2811c05e.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **55.370000000 Hz NTSC** | **256x240**| **45:44** | **1024:939**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,960,3,10,13,70045`** | [**jtsz**] | **256x240**| **1024x960** | **4x** | **960p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1200,3,10,19,106445`** | [**jtsz**] | **256x240**| **1280x1200** | **5x** | **1200p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1440,3,10,25,150401`** | [**jtsz**] | **256x240**| **1536x1440** | **6x** | **1440p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,14,90461`** | [**jtsz**] | **256x240**| **1280x1020** | **4.25x** | **1020p** | **1280 (5x)** | **3**
**`video_mode=1280,80,128,208,1020,3,10,23,107459`** | [**jtsz**] | **256x240**| **1280x1020** | **4.25x** | **1020p** | **1280 (5x)** | **3** | **1** |

----

### <summary2><b>Hardware Information for:</b></summary2>

![9](https://user-images.githubusercontent.com/32810066/126889338-43ff4e0e-8379-4245-b664-d9edbb57bb8a.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **55.970000000 Hz NTSC** | **256x240**| **45:44** | **1024:939**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,960,3,10,13,70045`** | [**jttrojan**] | **256x240**| **1024x960** | **4x** | **960p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1200,3,10,19,106445`** | [**jttrojan**] | **256x240**| **1280x1200** | **5x** | **1200p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1440,3,10,26,150503`** | [**jttrojan**] | **256x240**| **1536x1440** | **6x** | **1440p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,14,90461`** | [**jttrojan**] | **256x224**| **1280x1020** | **4.25x** | **1020p** | **1280 (5x)** | **3** |
**`video_mode=1280,80,128,208,1020,3,10,23,107459`** | [**jttrojan**] | **256x224**| **1280x1020** | **4.25x** | **1020p** | **1280 (5x)** | **3** | **1** |

## <summary1><b>Capcom M68000 Hardware</b></summary1>

### <summary2><b>Hardware Information for:</b></summary2>

![1](https://user-images.githubusercontent.com/32810066/126862656-858c48c4-0b3f-4a77-9123-0e74670dced8.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **59.640000000 Hz NTSC** | **256x224**| **45:44** | **2560:2191**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,896,3,10,13,65499`** | [**jtbiocom**] [**jtf1drm**] [**jttora**] | **256x224**| **1024x896** | **4x** | **896p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1120,3,10,19,99533`** | [**jtbiocom**] [**jtf1drm**] [**jttora**] | **256x224**| **1280x1120** | **5x** | **1120p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1344,3,10,26,140734`** | [**jtbiocom**] [**jtf1drm**] [**jttora**] | **256x224**| **1536x1344** | **6x** | **1344p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**jtbiocom**] [**jtf1drm**] [**jttora**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**jtbiocom**] [**jtf1drm**] [**jttora**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

----

### <summary2><b>Hardware Information for:</b></summary2>

![2](https://user-images.githubusercontent.com/32810066/126862894-a8159ad3-64f8-4423-b6cc-2125e4021958.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.000 MHz** | **61.000000000 Hz NTSC** | **384x224**| **135:176** | **1280:973**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,896,3,10,13,93823`** | [**jtsf**] | **384x224**| **1536x896** | **4x** | **896p** | **1536 (4x)** |
**`video_mode=1920,48,32,80,1120,3,10,20,143894`** | [**jtsf**] | **384x224**| **1920x1120** | **5x** | **1120p** | **1920 (5x)** |
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**jtsf**] | **384x224**| **1920x1344** | **6x / 5x (Hor.)** | **1344p** | **1920 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1248,48,32,80,1008,3,10,17,87690`** | [**jtsf**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3** |
**`video_mode=1248,80,128,208,1008,3,10,26,104532`** | [**jtsf**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3** | **1** |

## <summary1><b>Capcom CP System Hardware</b></summary1>

### <summary2><b>Hardware Information for:</b></summary2>

![3](https://user-images.githubusercontent.com/32810066/126880018-e9512c29-e830-42eb-aad5-858b05a468e5.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.00 MHz** | **59.629400000 Hz NTSC** | **384x224**| **135:176** | **1280:973**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,896,3,10,13,93823`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1536x896** | **4x** | **896p** | **1536 (4x)** |
**`video_mode=1920,48,32,80,1120,3,10,19,143770`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1920x1120** | **5x** | **1120p** | **1920 (5x)** |
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1920x1344** | **6x / 5x (Hor.)** | **1344p** | **1920 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1248,48,32,80,1008,3,10,16,87606`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3** |
**`video_mode=1248,80,128,208,1008,3,10,25,104433`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Data East Hardware</b></summary>_

## <summary1><b>Data East MEC-M1 Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![DECO](https://user-images.githubusercontent.com/32810066/154137678-05590233-6159-4b8e-b007-d119c06c5d6a.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **57.444853 Hz NTSC** | **256x240**| **16:15** | **1024:939** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,960,3,10,14,70116`** | [**jtninja**] [**jtcop**] | **256x240**| **1024x960** | **4x** | **960p** | **1 (4x)** |
**`video_mode=1280,48,32,80,1200,3,10,20,106531`** | [**jtninja**] [**jtcop**] | **256x240**| **1280x1200** | **5x** | **1200p** | **1 (5x)** |
**`video_mode=1536,48,32,80,1440,3,10,27,150605`** | [**jtninja**] [**jtcop**] | **256x240**| **1536x1440** | **6x** | **1440p** | **1 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**jtninja**] [**jtcop**] | **256x240**| **1260x1020** | **1** | **1020p** | **1 (4.5x)** | **3** |
**`video_mode=1280,80,128,208,1020,3,10,24,107560`** | [**jtninja**] [**jtcop**] | **256x240**| **1260x1020** | **1** | **1020p** | **1 (4.5x)** | **3** | **1** |

</blockquote>

## <summary1><b>Data East MEC-M1 (Midnight Resistance Based) Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![DECO2](https://user-images.githubusercontent.com/32810066/154369296-a27d5a4d-910c-4705-9f56-157f2c1383ed.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **57.444853 Hz NTSC** | **256x240**| **16:15** | **1024:939** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,960,3,10,14,70116`** | [**jtmidres**] | **256x240**| **1024x960** | **4x** | **960p** | **1 (4x)** |
**`video_mode=1280,48,32,80,1200,3,10,20,106531`** | [**jtmidres**] | **256x240**| **1280x1200** | **5x** | **1200p** | **1 (5x)** |
**`video_mode=1536,48,32,80,1440,3,10,27,150605`** | [**jtmidres**] | **256x240**| **1536x1440** | **6x** | **1440p** | **1 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**jtmidres**] | **256x240**| **1260x1020** | **1** | **1020p** | **1 (4.5x)** | **3** |
**`video_mode=1280,80,128,208,1020,3,10,24,107560`** | [**jtmidres**] | **256x240**| **1260x1020** | **1** | **1020p** | **1 (4.5x)** | **3** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Konami Hardware</b></summary>_

## <summary1><b>Konami 007121 (Contra Based) Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![4](https://user-images.githubusercontent.com/32810066/126880048-97feb40c-4266-4d71-9f55-2a1ab3c0f04b.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.000 MHz** | **59.187400000 Hz NTSC** | **280x240**| **45:44** | **1120:939** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1120,48,32,80,896,3,7,16,70810`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1120x896** | **4x** | **896p** | **1120 (4x)** |
**`video_mode=1400,48,32,80,1120,3,7,22,107827`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1400x1120** | **5x** | **1120p** | **1400 (5x)** |
**`video_mode=1680,48,32,80,1344,3,7,28,152573`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1680x1344** | **6x** | **1344p** | **1680 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1260,48,32,80,1020,3,10,16,89123`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1260x1024** | **4.25** | **1020p** | **1260 (4.5x)** | **3** |
**`video_mode=1260,80,128,208,1020,3,10,25,106139`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1260x1024** | **4.25** | **1020p** | **1260 (4.5x)** | **3** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Sega Hardware</b></summary>_

## <summary1><b>Sega Sytem 16 Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![5](https://user-images.githubusercontent.com/32810066/126880122-ba46beae-604d-4045-acc4-40ade481ee5a.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.2937 MHz** | **60.280000000 Hz NTSC** | **320x224**| **39:40** | **400:287** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**jts16**] [**jts16a1**] [**jts16a2**] [**jts16b**] [**jts16b1**] [**jts16b2**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)** |
**`video_mode=1600,48,32,80,1120,3,10,19,121651`** | [**jts16**] [**jts16a1**] [**jts16a2**] [**jts16b**] [**jts16b1**] [**jts16b2**] | **320x224**| **1600x1120** | **5x** | **1120p** | **1600 (5x)** |
**`video_mode=1920,48,32,80,1344,3,10,26,172598`** | [**jts16**] [**jts16a1**] [**jts16a2**] [**jts16b**] [**jts16b1**] [**jts16b2**] | **320x224**| **1920x1344** | **6x** | **1344p** | **1920 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**jts16**] [**jts16a1**] [**jts16a2**] [**jts16b**] [**jts16b1**] [**jts16b2**] |  **320x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,136,216,1008,3,10,25,107445`** | [**jts16**] [**jts16a1**] [**jts16a2**] [**jts16b**] [**jts16b1**] [**jts16b2**] |  **320x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Taito Hardware</b></summary>_

## <summary1><b>Taito Z80 Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![12](https://user-images.githubusercontent.com/32810066/126892659-0248d08e-0f45-4c56-8cab-6b7048345934.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.00 MHz** | **59.1856060 Hz NTSC** | **256x225** | **45:44** | **563:484** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,900,3,10,13,65783`** | [**jtbubl**] | **256x225**| **1024x900** | **4x** | **900p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1125,3,10,19,99965`** | [**jtbubl**] | **256x225**| **1280x1125** | **5x** | **1125p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1350,3,10,25,141243`** | [**jtbubl**] | **256x225**| **1536x1350** | **6x** | **1350p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1013,3,10,16,90029`** | [**jtbubl**] | **256x225** | **1280x1013** | **4.5x** | **1013p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1013,3,10,25,106950`** | [**jtbubl**] | **256x225** | **1280x1013** | **4.5x** | **1013p** | **1280 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Technos Hardware</b></summary>_

## <summary1><b>Technos HD6309 Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![11](https://user-images.githubusercontent.com/32810066/126891755-d87d293b-be47-4e82-b31e-f593a85dd365.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.00 MHz** | **57.4448530 Hz NTSC** | **256x232**| **45:44** | **2560:2191**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,928,3,10,13,67772`** | [**jtdd**] [**jtdd2**] | **256x232**| **1024x928** | **4x** | **928p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1160,3,10,19,102989`** | [**jtdd**] [**jtdd2**] | **256x232**| **1280x1160** | **5x** | **1160p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1392,3,10,25,145517`** | [**jtdd**] [**jtdd2**] | **256x232**| **1536x1392** | **6x** | **1392p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1013,3,10,15,89942`** | [**jtdd**] [**jtdd2**] | **256x232** | **1280x986** | **4.25x** | **986p** | **1280 (5x)** | **3** |
**`video_mode=1280,80,128,208,1013,3,10,24,106848`** | [**jtdd**] [**jtdd2**] | **256x232** | **1280x986** | **4.25x** | **986p** | **1280 (5x)** | **3** | **1** |

</blockquote>

</details>

----

</details>

<details>

<summary><b>Arcade Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

<details>

_<summary><b>Cave Hardware</b></summary>_

## <summary1><b>Cave 68000</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![23](https://user-images.githubusercontent.com/32810066/126911397-e54b786a-39ff-4200-8fdb-8750d1b40976.png)

<b>The Cave 68000 core does not support custom aspect ratios at this time. The only available options are 4:3 and 16:9; these are [hardcoded](https://github.com/MiSTer-devel/Arcade-Cave_MiSTer/blob/5f2000bb8bb9aeec6760579bd5667414aecf99f0/quartus/cave.sv#L164) to the core.</b>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**7.00 MHz** | **57.4200000 Hz NTSC** | **320x240**| **135:154** | **256:219** |
**8.00 MHz** | **57.4200000 Hz NTSC** | **384x240**| **135:176** | **1280:1251** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,20,85277`** | [**cave**] | **320x240**| **1280x960** | **4x** | **960p** | **1280 (4x)** |
**`video_mode=1600,48,32,80,1200,3,4,26,130205`** | [**cave**] | **320x240**| **1600x1200** | **5x** | **1200p** | **1600 (5x)** |
**`video_mode=1920,48,32,80,1440,3,4,33,184704`** | [**cave**] | **320x240**| **1920x1440** | **6x** | **1440p** | **1920 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**cave**] | **320x240** | **1280x1020** | **4.25x** | **1020p** | **1280 (4x)** | **3** |
**`video_mode=1280,80,128,208,1020,3,10,24,107560`** | [**cave**] | **320x240** | **1280x1020** | **4.25x** | **1020p** | **1280 (4x)** | **3** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Irem Hardware</b></summary>_

## <summary1><b>Irem M62</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![30](https://user-images.githubusercontent.com/32810066/129884118-239953a3-8cd6-4ba1-9250-55a4eae3cfbe.png)

<b>Irem M62 hardware has different horizontal resolutions set by jumpers on the actual PCB. Spanning from 256px to 384px. The primary video mode will cover both horizontal resolutions. 256px mode will result in a border (Kung Fu Master / Spartan X) but display the correct aspect ratio.</b>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.144 MHz** | **56.338028  Hz NTSC** | **256x255**| **5625:5632** | **256:255** |
**8.00 MHz** | **55.017606  Hz NTSC** | **384x255**| **135:176** | **3409:2950** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,1020,3,10,14,106543`** | [**a.iremm62**] | **384x255**| **1536x1020** | **4x** | **1020p** | **1536 (4x)** |
**`video_mode=1920,48,32,80,1275,3,10,21,163363`** | [**a.iremm62**] | **384x255**| **1920x1275** | **5x** | **1275p** | **1920 (5x)** |

- _<b>Optional: Utilize the Secondary Modelines below if you are playing 256px (horizontal) titles.</b>_

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,1020,3,10,15,74450`** | [**a.iremm62**] | **256x255**| **1024x1020** | **4x** | **1020p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1275,3,10,21,113098`** | [**a.iremm62**] | **256x255**| **1280x1275** | **5x** | **1275p** | **1280 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1248,48,32,80,1020,3,10,15,88535`** | [**a.iremm62**] | **384x255** | **1248x1020** | **4x / 3.25x (Hor.)** | **1020p** | **1248 (3.25x)** | **3** |
**`video_mode=1248,72,128,200,1020,3,10,23,104417`** | [**a.iremm62**] | **384x255** | **1248x1020** | **4x / 3.25x (Hor.)** | **1020p** | **1248 (3.25x)** | **3** | **1** |

- _<b>Optional: Utilize the Secondary Modelines below if you are playing 256px (horizontal) titles.</b>_

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**a.iremm62**] | **256x255**| **1280x1275** | **4x / 5x (Hor.)** | **1020p** | **1280 (5x)** | **1** |
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**a.iremm62**] | **256x255**| **1280x1275** | **4x / 5x (Hor.)** | **1020p** | **1280 (5x)** | **1** | **1** |

</blockquote>

</details>

<details>

### <summary1><b>Konami 005849 (Green Beret Based) Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![33](https://user-images.githubusercontent.com/32810066/129899428-a1aea73c-3078-43eb-b3a1-e3f2415d817d.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.144 MHz** | **60.600000 Hz NTSC** | **240x224**| **5625:5632** | **15:14** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=960,48,32,80,896,3,10,13,61958`** | [**a.rshnatk**]| **240x224**| **960x896** | **4x** | **896p** | **960 (4x)** |
**`video_mode=1200,48,32,80,1120,3,10,20,94085`** | [**a.rshnatk**]| **240x224**| **1200x1120** | **5x** | **1120p** | **1200 (5x)** |
**`video_mode=1440,48,32,80,1344,3,10,26,132768`** | [**a.rshnatk**]| **240x224**| **1440x1344** | **6x** | **1344p** | **1440 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1200,48,32,80,1008,3,10,17,84701`** | [**a.rshnatk**]| **240x224**| **1200x1008** | **4.5x / 5x (Hor.)** | **1008p** | **1200 (5x)** | **2** |
**`video_mode=1200,48,32,80,1008,3,10,17,84701`** | [**a.rshnatk**]| **240x224**| **1200x1008** | **4.5x / 5x (Hor.)** | **1008p** | **1200 (5x)** | **2** | **1** |

</blockquote>

_<summary><b>Konami Hardware</b></summary>_

### <summary1><b>Konami 005885 (Double Dribble Based) Hardware</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![31](https://user-images.githubusercontent.com/32810066/129876516-e3f8bce1-662c-4027-8037-90b238fc4346.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.144 MHz** | **61.0500000 Hz NTSC** | **240x224**| **5625:5632** | **15:14** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=960,48,32,80,896,3,10,13,61958`** | [**a.ironhorse**] [**a.jackal**] | **240x224**| **960x896** | **4x** | **896p** | **960 (4x)** |
**`video_mode=1200,48,32,80,1120,3,10,20,94085`** | [**a.ironhorse**] [**a.jackal**] | **240x224**| **1200x1120** | **5x** | **1120p** | **1200 (5x)** |
**`video_mode=1440,48,32,80,1344,3,10,26,132768`** | [**a.ironhorse**] [**a.jackal**] | **240x224**| **1440x1344** | **6x** | **1344p** | **1440 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1200,48,32,80,1008,3,10,17,84701`** | [**a.ironhorse**] [**a.jackal**] | **240x224**| **1200x1008** | **4.5x / 5x (Hor.)** | **1008p** | **1200 (5x)** | **2** |
**`video_mode=1200,48,32,80,1008,3,10,17,84701`** | [**a.ironhorse**] [**a.jackal**] | **240x224**| **1200x1008** | **4.5x / 5x (Hor.)** | **1008p** | **1200 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Sega Hardware</b></summary>_

## <summary1><b>Sega System 1 / Sega System 2</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![26](https://user-images.githubusercontent.com/32810066/126917773-d9bc0d25-72c6-468e-a0e6-b19aa34a0939.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.00 MHz** | **60.0952000 Hz NTSC** | **256x224**| **27:22** | **2560:1827** | **280:261** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,896,3,10,13,65499`** | [**a.segasys1**] | **256x224**| **1024x896** | **4x** | **896p** | **1024 (4x)** |
**`video_mode=1280,48,32,80,1120,3,10,19,99533`** | [**a.segasys1**] | **256x224**| **1280x1120** | **5x** | **1120p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1344,3,10,26,140734`** | [**a.segasys1**] | **256x224**| **1536x1344** | **6x** | **1344p** | **1536 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**a.segasys1**] | **256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**a.segasys1**] | **256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>SNK Hardware</b></summary>_

## <summary1><b>Neo Geo Multi Video System</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![22](https://user-images.githubusercontent.com/32810066/127518927-4185dc35-049c-4276-a94b-ff301c2eed50.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.00 MHz** | **59.1856000 Hz NTSC** | **320x224**| **45:44** | **3200:2191**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**neogeo**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)** |
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**neogeo**] | **320x224**| **1536x1120** | **5x** | **1120p** | **1536 (5x)** |
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**neogeo**] | **320x224**| **1920x1344** | **6x** | **1334p** | **1920 (6x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**neogeo**] | **320x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**neogeo**] | **320x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Toaplan Hardware</b></summary>_

## <summary1><b>Toaplan V1</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![1](https://user-images.githubusercontent.com/32810066/156853872-a988118e-8fdd-40a9-98a4-c766777e336a.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**7.00 MHz** | **55.16 Hz** | **320x240**| **4:3** | **256:219**
**7.00 MHz** | **57.55 Hz** | **320x240**| **4:3** | **256:219**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,20,85277`** | [**zerowing**] | **320x240**| **1280x960** | **4x** | **960p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1200,3,4,26,130205`** | [**zerowing**] | **320x240**| **1600x1200** | **5x** | **1200p** | **1536 (5x)**
**`video_mode=1920,48,32,80,1440,3,4,33,184704`** | [**zerowing**] | **320x240**| **1920x1440** | **6x** | **1440p** | **1920 (6x)**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,19,85190`** | [**outzone***] | **320x240**| **1280x960** | **4x** | **960p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1200,3,4,25,130099`** | [**outzone***] | **320x240**| **1600x1200** | **5x** | **1200p** | **1536 (5x)**
**`video_mode=1920,48,32,80,1440,3,4,31,184454`** | [**outzone***] | **320x240**| **1920x1440** | **6x** | **1440p** | **1920 (6x)**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**zerowing**] | **320x240** | **1280x1020** | **4.5x** | **1020p** | **1280 (4x)** | **3** |
**`video_mode=1280,80,128,208,1020,3,10,24,107560`** | [**zerowing**] | **320x240** | **1280x1020** | **4.5x** | **1020p** | **1280 (4x)** | **3** | **1** |

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,14,90461`** | [**outzone***] | **320x240** | **1280x1020** | **4.5x** | **1020p** | **1280 (4x)** | **3** |
**`video_mode=1280,80,128,208,1020,3,10,23,107459`** | [**outzone***] | **320x240** | **1280x1020** | **4.5x** | **1020p** | **1280 (4x)** | **3** | **1** |

</blockquote>

</details>

----

</details>

</details>

</details>

<details>

<summary><b>Console Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

### **Console Core Custom Video Modes:**

- Utilize the primary modelines for dual mode cores listed below.

----

<details>

_<summary><b>Atari Hardware</b></summary>_

## <summary1><b> Atari 7800</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![Atari_7800_Logo](https://user-images.githubusercontent.com/32810066/129828819-21ef9138-42e9-4613-b664-a2e72855eb2a.png)

<b>The Atari 7800 hardware also utilizes a low-res pixel clock (3.58 MHz). The timings provided below cover all the resolution switching for an HDMI display.</b>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**7.16 MHz** | **59.922751013551 Hz NTSC** | **372x224**| **6:7** | **3720:2611** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1488,48,32,80,896,3,10,13,91167`** | [**atari7800**] | **372x224** | **1488x896**| **4x** | **896p** | **1488 (4x)** |
**`video_mode=1860,48,32,80,1120,3,10,19,139346`** | [**atari7800**] | **372x224** | **1860x1120**| **5x** | **1120p** | **1860 (5x)** |
**`video_mode=1860,48,32,80,1344,3,10,26,167288`** | [**atari7800**] | **372x224** | **1860x1344**| **6x / 5x (Hor.)** | **1344p** | **1860 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1208,48,32,80,1008,3,10,16,85117`** | [**atari7800**] | **372x224**| **1208x1008** | **4.5x / 3.25x (Hor.)** | **1008p** | **1280 (3.25x)** | **3** |
**`video_mode=1208,72,128,200,1008,3,10,25,100918`** | [**atari7800**] | **372x224**| **1208x1008** | **4.5x / 3.25x (Hor.)** | **1008p** | **1280 (3.25x)** | **3** | **1** |

</blockquote>

## <summary1><b>Atari Lynx</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![25](https://user-images.githubusercontent.com/32810066/126915335-bd6c5c2a-2038-4776-be8d-832e16b1fe4c.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**7.1100 MHz** | **59.89817311 Hz NTSC** | **160x102**| **80:51** | **4519:3340** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1440,48,32,80,918,3,10,14,90720`** | [**atarilynx**] | **160x102**| **1440x918** | **9x** | **1008p** | **1440 (9x)** |
**`video_mode=1600,48,32,80,1020,3,10,16,110774`** | [**atarilynx**] | **160x102**| **1600x1020** | **10x** | **1152p** | **1600 (10x)** |
**`video_mode=1760,48,32,80,1122,3,10,19,132941`** | [**atarilynx**] | **160x102**| **1760x1122** | **11x** | **1296p** | **1760 (11x)** |
**`video_mode=1920,48,32,80,1224,3,10,22,157123`** | [**atarilynx**] | **160x102**| **1920x1224** | **12x** | **1440p** | **1920 (12x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,16,90634`** | [**atarilynx**] | **160x102** | **1280x1020** | **10x** | **1020p** | **1280 (8x)** |**1** |
**`video_mode=1280,80,136,216,1020,3,10,25,108678`** | [**atarilynx**] | **160x102** | **1280x1020** | **10x** | **1020p** | **1280 (8x)** |**1** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Bandai Hardware</b></summary>_

## <summary1><b>Bandai Wonderswan / Bandia Wonderswan Color</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![24](https://user-images.githubusercontent.com/32810066/127161543-66e54ad0-77af-4be6-976b-e89af1f3be49.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|Display Aspec Ratio (Vert.)|
|--|--|--|--|--|--|
**7.3728 MHz** | **75.471698113207 Hz NTSC** | **224x144**| **14:9** | **35:27** | **15:28**|

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1568,48,32,80,1008,3,10,24,108346`** | [**wonderswan**] | **224x144** | **1568x1008** | **7x** | **1008p** | **1568 (7x)** |
**`video_mode=1792,48,32,80,1152,3,10,29,139841`** | [**wonderswan**] | **224x144** | **1792x1152** | **8x** | **1152p** | **1792 (8x)** |
**`video_mode=2016,48,32,80,1296,3,10,34,175342`** | [**wonderswan**] | **224x144** | **2016x1296** | **9x** | **1296p** | **2016 (9x)** |
**`video_mode=2016,48,32,80,1440,3,10,39,194796`** | [**wonderswan**] | **224x144** | **2016x1440** | **10x / 9x (Hor.)** | **1440p** | **2016 (9x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1232,48,32,80,1008,3,10,24,87278`** | [**wonderswan**] | **224x144** | **1232x1008** | **5.5x** | **1008p** | **1232 (7x)** | **2** |
**`video_mode=1232,88,128,216,1008,3,10,34,105331`** | [**wonderswan**] | **224x144** | **1232x1008** | **5.5x** | **1008p** | **1232 (7x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>NEC Hardware</b></summary>_

## <summary1><b>NEC PC Engine Duo / NEC Turbo Duo</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![31](https://user-images.githubusercontent.com/32810066/128566140-4c18387b-c0b6-434d-8741-861cbc2db988.png)

<b>The NEC PC Engine Duo core utilizes a resolution of 360x231 to cover all of the hardwares resolution switching for an HDMI display.</b>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.3700 MHz** | **59.826105453482 Hz NTSC** | **360x231 (FPGA Core)**| **8:7** | **2048:1673 (Based on 256x239)** |
**7.1600 MHz** | **59.826105453482 Hz NTSC** | **360x231 (FPGA Core)**| **6:7** | **1961:2134  (Based on 256x239)** |
**10.7400 MHz** | **59.826105453482 Hz NTSC** | **360x231 (FPGA Core)**| **4:7** | **1024:847 (Based on 512x242)** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1440,48,32,80,924,3,10,14,91296`** | [**tgfx16**] | **360x231 (FPGA Core)**| **1440x924** | **4x** | **924p** | **1440 (4x)** |
**`video_mode=1800,48,32,80,1155,3,10,20,139709`** | [**tgfx16**] | **360x231 (FPGA Core)**| **1800x1155** | **5x** | **1155p** | **1800 (5x)** |
**`video_mode=1800,48,32,80,1386,3,10,27,167698`** | [**tgfx16**] | **360x231 (FPGA Core)**| **1800x1386** | **6x / 5x (Hor.)** | **1386p** | **1800 (5x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1260,48,32,80,982,3,10,15,85810`** | [**tgfx16**] | **360x231 (FPGA Core)** | **1260x982** | **4.25x** | **982p** | **1260 (3.5x)** |**3** |
**`video_mode=1260,80,128,208,982,3,10,24,102226`** | [**tgfx16**] | **360x231 (FPGA Core)** | **1260x982** | **4.25x** | **982p** | **1260 (3.5x)** |**3** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Nintendo Hardware</b></summary>_

## <summary1><b>Nintendo Famicom / Nintendo Entertainment System</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![13](https://user-images.githubusercontent.com/32810066/126899153-f123d425-e904-451f-a26c-7633c2806fbf.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x240**| **8:7** | **128:105**
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224**| **8:7** | **64:49**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**nes**] | **256x240**| **1280x960** | **4x** | **960p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1200,3,10,22,125674`** | [**nes**] | **256x240**| **1536x1200** | **5x** | **1200p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1440,3,10,28,173455`** | [**nes**] | **256x240**| **1792x1440** | **6x** | **1440p** | **1792 (7x)**

- _<b>Utilize the Secondary Modelines below if you enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.</b>_

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**nes**] | **256x224**| **1280x896** | **4x** | **896p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**nes**] | **256x224**| **1536x1120** | **5x** | **1120p** | **1536 (6x)** |
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**nes**] | **256x224**| **1792x1344** | **6x** | **1344p** | **1792 (7x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

- _<b>Enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD. This simulates playing on a CRT with the overscan areas pushed out of the display horizontally and vertically.</b>_

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**nes**] | **256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**nes**] | **256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

## <summary1><b>Game Boy / Game Boy Color</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![14](https://user-images.githubusercontent.com/32810066/126899243-8a3d843e-2abf-41ce-946b-ddf4808339fb.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.7108864 MHz** | **59.727500569606 Hz NTSC** | **160x144**| **10:9** | **64:63**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1120,48,32,80,1008,3,10,16,79642`** | [**gameboy**] | **160x144**| **1120x1008** | **7x** | **1008p** | **1120 (7x)** |
**`video_mode=1280,48,32,80,1152,3,10,20,102384`** | [**gameboy**] | **160x144**| **1280x1152** | **8x** | **1152p** | **1280 (8x)** |
**`video_mode=1440,48,32,80,1296,3,10,24,127968`** | [**gameboy**] | **160x144**| **1440x1296** | **9x** | **1296p** | **1440(9x)** |
**`video_mode=1600,48,32,80,1440,3,10,28,156394`** | [**gameboy**] | **160x144**| **1600x1440** | **10x** | **1440p** | **1600 (10x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**gameboy**] | **160x144** | **1280x1008** | **7x** | **1008p** | **1280 (8x)** | **1** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**gameboy**] | **160x144** | **1280x1008** | **7x** | **1008p** | **1280 (8x)** | **1** | **1** |

</blockquote>

## <summary1><b>Super Famicom / Super Nintendo</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![15](https://user-images.githubusercontent.com/32810066/126899412-22aed1c8-569f-4ccb-8276-73f640763d9d.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224 / 256x240**| **8:7** | **64:49**
**10.47 MHz** | **60.098813897441 Hz NTSC** | **512x224 / 512x240**| **16:7** | **128:105**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|FPGA Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**snes**] | **256x224**| **1280x896** | **4x** | **896p** | **1280 (5x)** 
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**snes**] | **256x224**| **1536x1120** | **5x** | **1120p** | **1536 (6x)** 
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**snes**] | **256x224**| **1792x1344** | **6x** | **1344p** | **1792 (7x)**

|Secondary Modelines NTSC|FPGA Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**snes**] | **256x240**| **1280x960** | **4x** | **960p** | **1280 (5x)** 
**`video_mode=1536,48,32,80,1200,3,10,22,125674`** | [**snes**] | **256x240**| **1536x1200** | **5x** | **1200p** | **1536 (6x)** 
**`video_mode=1792,48,32,80,1440,3,10,28,173455`** | [**snes**] | **256x240**| **1792x1440** | **6x** | **1440p** | **1792 (7x)** 

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**snes**] | **256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**snes**] | **256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

## <summary1><b> Game Boy Advance</b></summary1>

<blockquote>

- <summary><b> Hardware Information for:</b></summary>

![16](https://user-images.githubusercontent.com/32810066/126899678-9b8d94ba-a2e6-4e37-a617-c6e42a806724.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.2925 MHz** | **59.727500569606 Hz NTSC** | **240x160**| **39:40** | **60:41** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1440,48,32,80,960,3,10,15,94848`** | [**gba**] | **240x160**| **1440x960** | **6x** | **960p** | **1440 (6x)** |
**`video_mode=1680,48,32,80,1120,3,10,19,127181`** | [**gba**] | **240x160**| **1680x1120** | **7x** | **1120p** | **1680 (7x)** |
**`video_mode=1920,48,32,80,1280,3,10,24,164362`** | [**gba**] | **240x160**| **1920x1280** | **8x** | **1280p** | **1920(8x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1256,48,32,80,1015,3,10,16,88698`** | [**gba**] | **240x160** | **1256x1015** | **7.25x** | **1015p** | **1260 (5.25x)** |**3** |
**`video_mode=1256,80,128,208,1015,3,10,25,105637`** | [**gba**] | **240x160** | **1256x1015** | **7.25x** | **1015p** | **1260 (5.25x)** | **3** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Sega Hardware</b></summary>_

## <summary1><b>Sega SG-1000</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![17](https://user-images.githubusercontent.com/32810066/126900508-ac01aad3-975c-4a41-a8ac-8a922a1d6e17.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x192**| **8:7** | **32:21** |

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

- _<b>The Sega Mark III / Sega Master System Core also launches SG-1000 titles. You have options for this hardware, this is an end user preference.</b>_

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**coleco**] | **256x192**| **1280x960** | **5x** | **960p** | **1280 (5x)** |
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**coleco**] | **256x192**| **1536x1152** | **6x** | **1152p** | **1536 (6x)** |
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**coleco**] | **256x192**| **1792x1344** | **7x** | **1344p** | **1792 (7x)** |

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

- _<b>The Sega Mark III / Sega Master System Core also launches SG-1000 titles. You have options for this hardware, this is an end user preference.</b>_

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**coleco**] | **256x192** | **1280x1008** | **5.25x** | **1008p** | **1280 (5x)** | **3** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**coleco**] | **256x192** | **1280x1008** | **5.25x** | **1008p** | **1280 (5x)** | **3** | **1** |

</blockquote>

## <summary1><b>Sega Mark III / Sega Master System (Sega SG-1000 Compatible)</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![18](https://user-images.githubusercontent.com/32810066/126900463-ccacf885-8a07-4ceb-a904-16e73a4141cc.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x192**| **8:7** | **32:21**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**sms**] | **256x192**| **1536x1152** | **6x** | **1152p** | **1536 (6x)** | **Yes**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**sms**] | **256x192**| **1280x960** | **5x** | **960p** | **1280 (5x)** | **No**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**sms**] | **256x192**| **1792x1344** | **7x** | **1344p** | **1792 (7x)** | **No**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**sms**] | **256x192** | **1280x1008** | **5.25x** | **1008p** | **1280 (5x)** | **3** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**sms**] | **256x192** | **1280x1008** | **5.25x** | **1008p** | **1280 (5x)** | **3** | **1** |

</blockquote>

## <summary1><b>Sega Mega Drive / Sega Genesis</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![19](https://user-images.githubusercontent.com/32810066/126900999-600e0d91-05ab-46df-9037-b82f6d127b72.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.71 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x224**| **8:7** | **64:49**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**genesis**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1120,3,10,19,121651`** | [**genesis**] | **320x224**| **1600x1120** | **5x** | **1120p** | **1600 (5x)**
**`video_mode=1920,48,32,80,1344,3,10,26,172598`** | [**genesis**] | **320x224**| **1920x1344** | **6x** | **1344p** | **1920 (6x)**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1024,48,32,80,896,3,10,13,65499`** | [**genesis**] | **256x224**| **1024x896** | **4x** | **896p** | **1024 (4x)**
**`video_mode=1280,48,32,80,1120,3,10,19,99533`** | [**genesis**] | **256x224**| **1280x1120** | **5x** | **1120p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1344,3,10,26,140734`** | [**genesis**] | **256x224**| **1536x1344** | **6x** | **1344p** | **1536 (6x)**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**genesis**] | **320x224/256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (4x/5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**genesis**] | **320x224/256x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (4x/5x)** | **2** | **1** |

</blockquote>

## <summary1><b>Sega Game Gear</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![20](https://user-images.githubusercontent.com/32810066/126901144-6217268c-3035-47f4-8f54-3588b8bf3d31.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **160x144**| **8:7** | **128:105**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**sms**] | **160x144**| **1536x1152** | **8x / 9.6x (Hor.)** | **1152p** | **1536 (9.6x)** | **Yes**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1120,48,32,80,1008,3,10,16,79642`** | [**sms**] | **160x144**| **1120x1008** | **7x** | **1008p** | **1120 (7x)** | **No**
**`video_mode=1280,48,32,80,1152,3,10,20,102384`** | [**sms**] | **160x144**| **1280x1152** | **8x** | **1152p** | **1280 (8x)** | **No**
**`video_mode=1440,48,32,80,1296,3,10,24,127968`** | [**sms**] | **160x144**| **1440x1296** | **9x** | **1296p** | **1440 (9x)** | **No**
**`video_mode=1600,48,32,80,1440,3,10,28,156394`** | [**sms**] | **160x144**| **1600x1440** | **10x** | **1440p** | **1600 (9x)** | **No**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**sms**] | **256x192** | **1280x1008** | **5.25x** | **1008p** | **1280 (5x)** | **3** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**sms**] | **256x192** | **1280x1008** | **5.25x** | **1008p** | **1280 (5x)** | **3** | **1** |

</blockquote>

## <summary1><b>Sega Mega CD / Sega CD</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![21](https://user-images.githubusercontent.com/32810066/126901391-d82effff-a2b3-40ef-bb2b-00495b44e43e.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.711647 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**megacd**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1120,3,10,19,121651`** | [**megacd**] | **320x224**| **1600x1120** | **5x** | **1120p** | **1600 (5x)**
**`video_mode=1920,48,32,80,1344,3,10,26,172598`** | [**megacd**] | **320x224**| **1920x1344** | **6x** | **1344p** | **1920 (6x)**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**megacd**] | **320x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**megacd**] | **320x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>SNK Hardware</b></summary>_

## <summary1><b>Neo Geo Advanced Entertainment System</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![29](https://user-images.githubusercontent.com/32810066/127527470-c3b38315-394a-4cc5-b4ea-117a51f892f0.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.041957 MHz** | **59.5999 Hz NTSC** | **320x224**| **65:64** | **640:441**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**neogeo**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)**
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**neogeo**] | **320x224**| **1536x1120** | **5x** | **1120p** | **1536 (5x)**
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**neogeo**] | **320x224**| **1920x1344** | **6x** | **1334p** | **1920 (6x)**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**neogeo**] | **320x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**neogeo**] | **320x224** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Sony Hardware</b></summary>_

## <summary1><b>Sony PlayStation</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![psx](https://user-images.githubusercontent.com/32810066/154302550-5a675470-a371-4d13-bbe3-9535aea30110.png)

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.322240 MHz** | **59.8261054534819 Hz NTSC** | **256x224**| **4:3** | **1280:973**
**6.652800 MHz** | **59.8261054534819 Hz NTSC** | **320x224**| **10:7** | **3200:2429**
**7.603200 MHz** | **59.8261054534819 Hz NTSC** | **368x224**| **115:84** | **920:693**
**10.644480 MHz** | **59.8261054534819 Hz NTSC** | **512x224**| **8:7** | **1024:777**
**5.322240 MHz** | **59.8261054534819 Hz NTSC** | **256x240**| **56:45** | **512:417**
**6.652800 MHz** | **59.8261054534819 Hz NTSC** | **320x240**| **4:3** | **1280:1041**
**7.603200 MHz** | **59.8261054534819 Hz NTSC** | **368x240**| **23:18** | **368:297**
**10.644480 MHz** | **59.8261054534819 Hz NTSC** | **512x240**| **16:15** | **2048:1665**
**13.305600 MHz** | **59.8261054534819 Hz NTSC** | **640x480i**| **4:3** | **1280:1041**

### <summary3><b>Integer Scale Custom Video Modes:</b></summary3>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**psx**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1120,3,10,19,121651`** | [**psx**] | **320x224**| **1600x1120** | **5x** | **1120p** | **1536 (5x)**
**`video_mode=1920,48,32,80,1344,3,10,26,172598`** | [**psx**] | **320x224**| **1920x1344** | **6x** | **1344p** | **1920 (6x)**
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**psx**] | **320x240**| **1280x960** | **4x** | **960p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1200,3,4,27,130310`** | [**psx**] | **320x240**| **1600x1200** | **5x** | **1200p** | **1536 (5x)**
**`video_mode=1920,48,32,80,1440,3,4,34,184829`** | [**psx**] | **320x240**| **1920x1440** | **6x** | **1440p** | **1920 (6x)**

### <summary4><b>Integer Step-Scaled Custom Video Modes:</b></summary4>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|vscale_mode|vga_scaler|
|--|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**psx**] | **320x224** | **1280x1008** | **4.75x** | **1008p** | **1008 (4.75x)** | **3** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**psx**] | **320x224** | **1280x1008** | **4.75x** | **1008p** | **1008 (4.75x)** | **3** | **1** |
**`video_mode=1280,48,32,80,1020,3,10,16,90634`** | [**psx**] | **320x240** | **1280x1020** | **4.25x** | **1020p** | **1280 (4.25x)** | **3** |
**`video_mode=1280,80,136,216,1020,3,10,25,108678`** | [**psx**] | **320x240** | **1280x1020** | **4.25x** | **1020p** | **1280 (4.25x)** | **3** | **1** |

</blockquote>

</details>

</details>

</details>

</details>

</details>

</details>

----

# F.A.Q.

<details>

_<summary><b>Q: Why does the OSD menu appear squished or stretched when using custom modes?</b></summary>_

This is by design and nothing to worry about.

</details>

<details>

_<summary><b>Q: Why does the core image appear squished or stretched?</b></summary>_

Adjust your display to use `Original` or `4:3` aspect ratio. For iPad or 1280x1024 displays, set `Aspect Ratio: Full Screen` in the MiSTer OSD.

</details>

# License

This repository and project is licensed under the GNU General Public License v3.0. If you utilize the information elsewhere, you must reference this source repository and provide credit to the author(s).

# Support

Please consider showing support for this and future projects on my **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
