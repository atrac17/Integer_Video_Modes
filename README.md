
## Modeline Template

W.I.P


## Modeline Template Updater

W.I.P

## Integer Scaled Custom Video Modelines

<details>

 <summary><b>Arcade Core Video Modes</b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>
   
- The default resoltion for the `MiSTer.ini` should always be **720p**. This can be set by adjusting `video_mode=` to `0`.
- Unless stated below, the default `MiSTer.ini` settings for each core will be `vscale_mode=1` and `vsync_adjust=2`.

## <summary1><b> Capcom CP System Cores</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.00 MHz** | **59.6294 Hz NTSC** | **384x224**| **135:176** | **1280:973**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1152,48,32,80,896,3,10,13,72580`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1152x896** | **4x** | **896p** | **1152 (3x)**
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1536x1120** | **5x** | **1120p** | **1536 (4x)**
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1920x1344** | **6x** | **1344p** | **1920 (5x)**

</blockquote>

</details>


<details>

 <summary><b>Console Core Video Modes</b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>
   
- The default resoltion for the `MiSTer.ini` should always be **720p**. This can be set by adjusting `video_mode=` to `0`.
- Unless stated below, the default `MiSTer.ini` settings for each core will be `vscale_mode=1` and `vsync_adjust=2`.

## <summary1><b> Sega Mega Drive / Sega Genesis</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.71 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x224**| **8:7** | **64:49**

- <summary><b> VRR Capable Display Modes</b></summary>

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

</blockquote>

## <summary1><b> Super Famicom / Super Nintendo</b></summary1>

<blockquote>
 
- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224 / 256x240**| **8:7** | **64:49**
**10.47 MHz** | **60.098813897441 Hz NTSC** | **512x224 / 512x240**| **16:7** | **128:105**

- <summary><b> VRR Capable Display Modes</b></summary>

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

</blockquote>
 
</details>

## Support

Please consider showing support for this and future projects at [Patreon](https://www.patreon.com/atrac17). While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
