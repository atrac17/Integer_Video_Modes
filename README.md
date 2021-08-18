
![logo](https://user-images.githubusercontent.com/32810066/128452226-e23e1552-abb7-434b-92e1-b4b35a23a5af.png)

# Repository Information

- This repository will house custom video modes for FPGA cores. This project has been ongoing for over seven months. I'd like to take a moment to thank those who have supported it. 

- These settings are not universal for every display, they enhance the overall experience and target variable refresh rate, g-sync, or freesync displays. Your display may not accept them, I have no control over this. Please read the information provided thoroughly. See the F.A.Q for further assistance.

- The custom video modes provided will integer scale the default resolution of the FPGA core. This will enhance filters and display the image bezel to bezel vertically if applied properly. 
  
  The scale function available in the MiSTerFPGA framework is limited to adjusting the horizontal resolution only based upon an algorithm. Though this may be similar, custom video modes also adjust the vertical resolution.

<details>

_<summary><b>Detailed Information</b></summary>_

<blockquote>

- These custom video modes are designed for 4k televisions, 2048x1536p (iPad Displays), 1440p monitors, and 1080p monitors that upscale the provided resolution from the DE-10 Nano. 

- Also provided are custom video modes for 1280x1024 LCD displays and common VGA CRT monitors. Again, ensure to read the information provided thoroughly or utilize one the provided MiSTer.ini files.

- If an aspect ratio is not displayed properly, adjust your television or monitor to original or 4:3 aspect ratio. For iPad or 1280x1024 displays, you will always set Aspect Ratio: Full Screen in the MiSTer OSD.

</blockquote>

</details>

<details>

_<summary><b>Repository Notes</b></summary>_

<blockquote>

- In the future, I will provide compatibility modes for the custom video modes below. This may resolve the issues with certain Samsung and Sony displays.

- Due to time constraints, I will periodically update the video modes available for FPGA cores from their respective repositories once this enters a public release.

- The F.A.Q for this repository is currently a work in progress, just like the repository itself. This is currently a pre-release and currently setup to ease the burden on the end user. While this may be work, the end results speak for themselves.

</blockquote>

</details>

# Updater Information

W.I.P

# Compatible Display List

<details>

_<summary><b>2048x1536 QXGA 9.7" Displays</b></summary>_

<blockquote>

- <summary><b>Display Panel Information:</b></summary>

|Display Model|Driver Board|Resolution (Native)|Resolution (Scaled)|VRR Capable|
|--|--|--|--|--|
**SAMSUNG LTN097QL01-A03** | **VS-RTD09703-V1** | **2048x1536**| **4x to 6x** | **Yes** |

</details>

<details>

_<summary><b>Compatible Display List Notes</b></summary>_

<blockquote>

The Compatible Display List for this repository is currently a work in progress, just like the repository itself. This is currently a pre-release and more information regarding compatible displays will be added in the future. 

If you have a display that correctly resolves these custom video modes, please create an issue within the repository and provide the compatible resolutions, make, model, firmware (where applicable), and general information on how you resolve the proper aspect ration on the display and I will add it to the repository.

</blockquote>

</details>

# Custom Video Mode Information

### Custom Video Modes:

<details>

<summary><b>Arcade Core Video Modes <a href="https://www.github.com/jotego">(Jotego)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default display resolution for the MiSTer.ini should always be 720p when utilizing custom video modes.

- The default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. Integer Step-Scaled Video Modes will specify the vscale_mode below.

- Due to the horizontal limitation of 2048 within cores, some video modes will utilize -1x for the horizontal scale. This will not affect the aspect ratio on your display if it's scaler takes advantage of the video mode provided. This is not a universal catch all. These are custom and display dependent.

- Integer-Step Scaled video modes are available for 1280x1024 LCD displays and common VGA CRT monitors with the same resolution; different video mode is provided. Video modes for VGA CRT monitors are to be utilized with vga_scaler=1.

- When utilizing Integer-Step Scaled video modes set the aspect ratio: full screen in the MiSTer OSD. This properly displays the provided custom video modes. If you are using a common VGA CRT monitor, you can stretch the horizontal and vertical to fill the screen in the displays OSD. This is the proper way to utilize VGA CRT monitor custom video modes.

----

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
**`video_mode=1232,48,32,80,1020,3,10,15,87529`** | [**jtrumble**] | **256x224**| **1232x1020** | **4.25x** | **1020p** | **1232 (3.5x)** | **2** |
**`video_mode=1232,72,128,200,1020,3,10,24,103501`** | [**jtrumble**] | **256x224**| **1232x1020** | **4.25x** | **1020p** | **1232 (3.5x)** | **2** | **1** |

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
**`video_mode=1280,48,32,80,1020,3,10,14,90461`** | [**jtsz**] | **256x224**| **1280x1020** | **4.25x** | **1020p** | **1280 (5x)** | **3**
**`video_mode=1280,80,128,208,1020,3,10,23,107459`** | [**jtsz**] | **256x224**| **1280x1020** | **4.25x** | **1020p** | **1280 (5x)** | **3** | **1** |

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
**`video_mode=1256,80,128,208,1020,3,10,25,106139`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1260x1024** | **4.25** | **1020p** | **1260 (4.5x)** | **3** | **1** |

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

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default display resolution for the MiSTer.ini should always be 720p when utilizing custom video modes.

- The default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. Integer Step-Scaled Video Modes will specify the vscale_mode below.

- Due to the horizontal limitation of 2048 within cores, some video modes will utilize -1x for the horizontal scale. This will not affect the aspect ratio on your display if it's scaler takes advantage of the video mode provided. This is not a universal catch all. These are custom and display dependent.

- Integer-Step Scaled video modes are available for 1280x1024 LCD displays and common VGA CRT monitors with the same resolution; different video mode is provided. Video modes for VGA CRT monitors are to be utilized with vga_scaler=1.

- When utilizing Integer-Step Scaled video modes set the aspect ratio: full screen in the MiSTer OSD. This properly displays the provided custom video modes. If you are using a common VGA CRT monitor, you can stretch the horizontal and vertical to fill the screen in the displays OSD. This is the proper way to utilize VGA CRT monitor custom video modes.

----

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

![31](https://user-images.githubusercontent.com/32810066/129868429-6ef36ae3-55b3-48ef-a5de-e1e9cf5551a8.png)

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

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**a.iremm62**] | **256x255**| **1280x1275** | **4x / 5x (Hor.)** | **1020p** | **1280 (5x)** | **1** |
**`video_mode=1280,48,32,80,1020,3,10,15,90547`** | [**a.iremm62**] | **256x255**| **1280x1275** | **4x / 5x (Hor.)** | **1020p** | **1280 (5x)** | **1** | **1** |

</blockquote>

</details>

<details>

_<summary><b>Sega Hardware</b></summary>_

## <summary1><b>Sega System 1 / Sega System 2</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![26](https://user-images.githubusercontent.com/32810066/126917773-d9bc0d25-72c6-468e-a0e6-b19aa34a0939.png)

<b>Vertical titles displayed on a horizontal screen will have a different display aspect ratio. You may need to adjust your displays aspect ratio from 4:3, Original, or Zoom 1 to 16:9 depending on the model and display type.</b>

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

----

</details>

</details>

<details>

<summary><b>Console Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default display resolution for the MiSTer.ini should always be 720p when utilizing custom video modes.

- The default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. Integer Step-Scaled Video Modes will specify the vscale_mode below.

- Due to the horizontal limitation of 2048 within cores, some video modes will utilize -1x for the horizontal scale. This will not affect the aspect ratio on your display if it's scaler takes advantage of the video mode provided. This is not a universal catch all. These are custom and display dependent.

- Integer-Step Scaled video modes are available for 1280x1024 LCD displays and common VGA CRT monitors with the same resolution; different video mode is provided. Video modes for VGA CRT monitors are to be utilized with vga_scaler=1.

- When utilizing Integer-Step Scaled video modes set the aspect ratio: full screen in the MiSTer OSD. This properly displays the provided custom video modes. If you are using a common VGA CRT monitor, you can stretch the horizontal and vertical to fill the screen in the displays OSD. This is the proper way to utilize VGA CRT monitor custom video modes.

- If a core has Dual Mode=Yes below, then there will only be one primary video mode available as the core supports multiple systems for one video mode. For custom aspect ratios, the first will be for the primary hardware and the other for the secondary hardware. This only applies to Dual Mode=Yes video modes.

----

### **Console Core Custom Video Modes:**

- Utilize the primary modelines for dual mode cores listed below.

----

<details>

_<summary><b>Atari Hardware</b></summary>_

## <summary1><b> Atari 7800</b></summary1>

<blockquote>

### <summary2><b>Hardware Information for:</b></summary2>

![Atari_7800_Logo](https://user-images.githubusercontent.com/32810066/129828819-21ef9138-42e9-4613-b664-a2e72855eb2a.png)

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
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**snes**] | **256x240** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** |
**`video_mode=1280,80,128,208,1008,3,10,25,106441`** | [**snes**] | **256x240** | **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2** | **1** |

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

</details>

</details>

----

### <summary1><b>Custom Aspect Ratios:</b></summary1>

<details>

<summary><b>Console Core Custom Aspect Ratios <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>MiSTer.ini Information:</b></summary1>

- Below are custom aspect ratios for each console core. They represent Display Aspect Ratio, Pixel Aspect Ratio, or Custom Aspect Ratios.

- These should be utilized with 4k televisions, 1440p monitors, and 1080p monitors that upscale the provided resolution from the DE-10 Nano.

- These should not be utilized with 2048x1536 (iPad) displays or 1280x1024 LCD displays.

- These custom aspect ratios may be utilized on 1280x1024 VGA CRT monitors. Find a custom aspect ratio you prefer, stretch the image horizontally and vertically to fit the screen within your displays OSD. This mimics what the hardware would show on a normal CRT television or monitor.

- The vertical resolution should match the modline. This will tell you which custom aspect ratio to utilize.

----

<details>

_<summary><b>Primary Custom Aspect Ratios</b></summary>_

|Console|Core|Custom Aspect Ratio|Custom Aspect Ratio|Dual Mode|Resolution|
|--|--|--|--|--|--|
**Atari Lynx** | [**atarilynx**] | **`custom_aspect_ratio_1=4519:3340`**| **`custom_aspect_ratio_2=80:51`** | **No** | _**102p**_ |
**Bandai Wonderswan** | [**wonderswan**] | **`custom_aspect_ratio_1=35:27`**| **`custom_aspect_ratio_2=15:28`** | **No** | _**144p**_ |
**Famicom / Nintendo Entertainment System** | [**nes**] | **`custom_aspect_ratio_1=128:105`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**240p**_ |
**Game Boy / Game Boy Color** | [**gameboy**] | **`custom_aspect_ratio_1=64:63`**| **`custom_aspect_ratio_2=10:9`** | **No** | _**144p**_ |
**Super Famicom / Super Nintendo** | [**snes**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**224p**_ |
**Game Boy Advance** | [**gba**] | **`custom_aspect_ratio_1=60:41`**| **`custom_aspect_ratio_2=3:2`** | **No** | _**160p**_ |
**Sega SG-1000** | [**coleco**] | **`custom_aspect_ratio_1=4:3`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**192p**_ |
**Sega Mark III / Sega Master System** | [**sms**] | **`custom_aspect_ratio_1=4:3`**| **N/A** | **Yes** | _**192p**_ |
**Sega Mega Drive / Sega Genesis** | [**genesis**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=32:25`** | **No** | _**224p**_ |
**Sega Game Gear** | [**sms**] | **N/A**| **`custom_aspect_ratio_2=128:105`** | **Yes** | _**144p**_ |
**Sega Mega CD / Sega CD** | [**megacd**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=32:25`** | **No** | _**224p**_ |

</details>

<details>

_<summary><b>Secondary Custom Aspect Ratios</b></summary>_

|Console|Core|Custom Aspect Ratio|Custom Aspect Ratio|Dual Mode|Resolution|
|--|--|--|--|--|--|
**Famicom / Nintendo Entertainment System** | [**nes**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**224p**_ |
**Super Famicom / Super Nintendo** | [**snes**] | **`custom_aspect_ratio_1=128:105`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**240p**_ |

</details>

</details>

----

</details>

# F.A.Q

W.I.P

# License

This repository and project is licensed under the GNU General Public License v3.0. If you utilize the information elsewhere, you must reference this source repository and provide credit to the author(s).

# Support

Please consider showing support for this and future projects on my **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
