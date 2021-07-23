![5](https://user-images.githubusercontent.com/32810066/126727672-b63f5a04-28ad-436e-b3f2-8e0029f0f9eb.png)

## General Information

This repository will contain custom resolutions for all available MiSTerFPGA cores currently available and in development. The custom **`video_mode`**(s) available will be targeted towards displays that have variable refresh rate and unique resolution capabilities.

Several displays support VRR and unique resolutions. You will find a list of known working displays below. If your display is compatible and not listed, please inform me on github providing the information below in the template.

The updater script in the repository will fetch the **`MiSTer.ini`** file the end-user configures in the script. They will have the ability to dictate it's name (**`MiSTer_alt_1.ini`**, **`MiSTer_alt_2.ini`** etc). Technical information regarding the video modes for each core are below. Please ensure to throughly read the information provided if you are configuring your own **`MiSTer.ini`** file from the information provided in this readme.

## Updater Information

W.I.P

## Compatible Displays (Panel / CRT)

W.I.P

## Integer Scaled Custom Video Modelines (VRR Displays)

<details>

<summary><b>Arcade Core Video Modes <a href="https://www.github.com/jotego">(Jotego)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>
   
- The default resolution for the **`MiSTer.ini`** should always be **720p**. Change the following default **`video_mode=0`** to set **720p** as your default resolution. If the end-user is generating a pre-configured **`MiSTer.ini`** this will be the default.

- Unless stated below, the default **`MiSTer.ini`** settings for each core will be **`vscale_mode=1`** and **`vsync_adjust=2`**. If the end-user is generating a pre-configured **`MiSTer.ini`** they will have the option to configure **`vsync_adjust`** themselves.

----

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

----

</details>

<details>

<summary><b>Arcade Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>
   
- The default resolution for the **`MiSTer.ini`** should always be **720p**. Change the following default **`video_mode=0`** to set **720p** as your default resolution. If the end-user is generating a pre-configured **`MiSTer.ini`** this will be the default.

- Unless stated below, the default **`MiSTer.ini`** settings for each core will be **`vscale_mode=1`** and **`vsync_adjust=2`**. If the end-user is generating a pre-configured **`MiSTer.ini`** they will have the option to configure **`vsync_adjust`** themselves.

----

### W.I.P

----

</details>

<details>

<summary><b>Console Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default resolution for the **`MiSTer.ini`** should always be **720p**. Change the following default **`video_mode=0`** to set **720p** as your default resolution. If the end-user is generating a pre-configured **`MiSTer.ini`** this will be the default.- Unless stated below, the default **`MiSTer.ini`** settings for each core will be **`vscale_mode=1`** and **`vsync_adjust=2`**. If the end-user is generating a pre-configured **`MiSTer.ini`** they will have the option to configure **`vsync_adjust`** themselves.

- Below are the correct **`custom aspect ratio`**(s) for each console core. These will be available in the pre-configured **`MiSTer.ini`** file(s). The end user can download pre-configered **`.cfg`** files for each core. This will override any current custom settings. Please ensure to back up your **`.cfg`** files for each console core in **`/media/fat/cfg/`** and apply any setting you previously had.

- If a core has **`Dual Mode=Yes`** below, then there will only be one **`primary video mode`** available as the **FPGA core** supports multiple systems. For aspect ratios, **`custom_aspect_ratio_1=`** will support the primary playable hardware and **`custom_aspect_ratio_2=`** will be for the secondary playable hardware. 

---

### <summary1><b>Console Core Custom Aspect Ratios:</b></summary1> 

- Matching the **vertical resolution** to the modline will tell you which **custom aspect ratios** to utilize if you are configuring your own **`MiSTer.ini`** file.

----

<details>

<summary><b> Primary Custom Aspect Ratios</b></summary>

|Console|Core|Custom Aspect Ratio|Custom Aspect Ratio|Dual Mode|Resolution|
|--|--|--|--|--|--|
**Sega SG-1000** | [**coleco**] | **`custom_aspect_ratio_1=4:3`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**192p**_ |
**Sega Mark III / Sega Master System** | [**sms**] | **`custom_aspect_ratio_1=4:3`**| **N/A** | **Yes** | _**192p**_ |
**Sega Mega Drive / Sega Genesis** | [**genesis**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=32:25`** | **No** | _**224p**_ |
**Sega Game Gear** | [**sms**] | **N/A**| **`custom_aspect_ratio_2=128:105`** | **Yes** | _**144p**_ |
**Sega Mega CD / Sega CD** | [**megacd**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=32:25`** | **No** | _**224p**_ |
**Famicom / Nintendo Entertainment System** | [**nes**] | **`custom_aspect_ratio_1=128:105`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**240p**_ |
**Super Famicom / Super Nintendo** | [**snes**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**224p**_ |

</details>

<details>

<summary><b> Secondary Custom Aspect Ratios</b></summary>

|Console|Core|Custom Aspect Ratio|Custom Aspect Ratio|Dual Mode|Resolution|
|--|--|--|--|--|--|
**Famicom / Nintendo Entertainment System** | [**nes**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**224p**_ |
**Super Famicom / Super Nintendo** | [**snes**] | **`custom_aspect_ratio_1=128:105`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**240p**_ |

</details>

----

### **Console Core Custom Video Modes:**

- Utilize the **`Primary Modelines`** for **`dual mode`** **console cores** listed below with the **custom aspect ratios** provided above. If you compile your own console core(s), you can utilize Secondary Modelines as well. In the future, I will have a tutorial for compiling if a core supports more than one resolution or piece of hardware. 

----

<details>

_<summary><b>Sega Hardware</b></summary>_

## <summary1><b> Sega SG-1000</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x192**| **8:7** | **32:21**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**coleco**] | **256x192**| **1280x960** | **5x** | **960p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**coleco**] | **256x192**| **1536x1152** | **6x** | **1152p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**coleco**] | **256x192**| **1792x1344** | **7x** | **1344p** | **1792 (7x)**

</blockquote>

## <summary1><b> Sega Mark III / Sega Master System (Sega SG-1000 Compatible)</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x192**| **8:7** | **32:21**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**sms**] | **256x192**| **1536x1152** | **6x** | **1152p** | **1536 (6x)** | **Yes**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**sms**] | **256x192**| **1280x960** | **5x** | **960p** | **1280 (5x)** | **No**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**sms**] | **256x192**| **1792x1344** | **7x** | **1344p** | **1792 (7x)** | **No**

</blockquote>

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

## <summary1><b> Sega Game Gear</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **160x144**| **8:7** | **128:105**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**sms**] | **160x144**| **1536x1152** | **8x** | **1152p** | **1536 (9.6x)** | **Yes**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1120,48,32,80,1008,3,10,16,79642`** | [**sms**] | **160x144**| **1120x1008** | **7x** | **1008p** | **1120 (7x)** | **No**
**`video_mode=1280,48,32,80,1152,3,10,20,102384`** | [**sms**] | **160x144**| **1280x1152** | **8x** | **1152p** | **1280 (8x)** | **No**
**`video_mode=1440,48,32,80,1296,3,10,24,127968`** | [**sms**] | **160x144**| **1440x1296** | **9x** | **1296p** | **1440 (9x)** | **No**
**`video_mode=1600,48,32,80,1440,3,10,28,156394`** | [**sms**] | **160x144**| **1600x1440** | **10x** | **1440p** | **1600 (9x)** | **No**

</blockquote>

## <summary1><b> Sega Mega CD / Sega CD</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.711647 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**megacd**] | **320x224**| **1280x896** | **4x** | **896p** | **1280 (4x)**
**`video_mode=1600,48,32,80,1120,3,10,19,121651`** | [**megacd**] | **320x224**| **1600x1120** | **5x** | **1120p** | **1600 (5x)**
**`video_mode=1920,48,32,80,1344,3,10,26,172598`** | [**megacd**] | **320x224**| **1920x1344** | **6x** | **1344p** | **1920 (6x)**

</blockquote>

----

</details>

<details>

_<summary><b>Nintendo Hardware</b></summary>_

## <summary1><b> Nintendo Famicom (Family Computer) / Nintendo NES (Nintendo Entertainment System)</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x240**| **8:7** | **128:105**
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224**| **8:7** | **64:49**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**nes**] | **256x240**| **1280x960** | **4x** | **960p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1200,3,10,22,125674`** | [**nes**] | **256x240**| **1536x1200** | **5x** | **1200p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1440,3,10,28,173455`** | [**nes**] | **256x240**| **1792x1440** | **6x** | **1440p** | **1792 (7x)**

- _<b>Utilize the **`Secondary Modelines`** below if you enable **`Hide Overscan: Yes`** in the **`MiSTer OSD`** and **`Mask Edges: Auto`** in the **NES core**</b>._

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**nes**] | **256x224**| **1280x896** | **4x** | **896p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**nes**] | **256x224**| **1536x1120** | **5x** | **1120p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**nes**] | **256x224**| **1792x1344** | **6x** | **1344p** | **1792 (7x)**

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

----

</details>

----

</details>


## Integer-Step Scaled Custom Video Modelines (5:4 IPS/LCD/TFT Displays)

<details>

<summary><b>Arcade Core Video Modes <a href="https://www.github.com/jotego">(Jotego)</a></b></summary>

## <summary1><b>General Information</b></summary1>

- Designed for **5:4 IPS/LCD/TFT** displays with a native resolution of **1280x1024**. Do not use these **`video_mode`**(s) with common **VGA CRT** monitors with the same native resolution.

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default resolution for the **`MiSTer.ini`** should always be **720p**. Change the following default **`video_mode=0`** to set **720p** as your default resolution. If the end-user is generating a pre-configured **`MiSTer.ini`** this will be the default.

- Unless stated below, the default **`MiSTer.ini`** settings for each core will be **`vscale_mode=1`** and **`vsync_adjust=2`**. If the end-user is generating a pre-configured **`MiSTer.ini`** they will have the option to configure **`vsync_adjust`** themselves.

## <summary1><b> Capcom CP System Cores</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.00 MHz** | **59.6294 Hz NTSC** | **384x224**| **135:176** | **1280:973**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modeline NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1248,48,32,80,1008,3,10,16,87606`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3**

</blockquote>

</details>

<details>

 <summary><b>Console Core Video Modes</b></summary>

## <summary1><b>General Information</b></summary1>

- Designed for **5:4 IPS/LCD/TFT** displays with a native resolution of **1280x1024**. Do not use these **`video_mode`**(s) with common **VGA CRT** monitors with the same native resolution.

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default resolution for the **`MiSTer.ini`** should always be **720p**. Change the following default **`video_mode=0`** to set **720p** as your default resolution. If the end-user is generating a pre-configured **`MiSTer.ini`** this will be the default.

- Unless stated below, the default **`MiSTer.ini`** settings for each core will be **`vscale_mode=1`** and **`vsync_adjust=2`**. If the end-user is generating a pre-configured **`MiSTer.ini`** they will have the option to configure **`vsync_adjust`** themselves.

## <summary1><b> Sega Mega Drive / Sega Genesis</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.71 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x224**| **8:7** | **64:49**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modeline NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**genesis**] | **320x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (4x)** | **2**

|Secondary Modeline NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**genesis**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2**

</blockquote>

## <summary1><b> Super Famicom / Super Nintendo</b></summary1>

<blockquote>

- <summary><b> Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224 / 256x240**| **8:7** | **64:49**
**10.47 MHz** | **60.098813897441 Hz NTSC** | **512x224 / 512x240**| **16:7** | **128:105**

- <summary><b> VRR Capable Display Modes</b></summary>

|Primary Modeline NTSC|FPGA Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**snes**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2**

|Secondary Modeline NTSC|FPGA Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**snes**] | **256x240**| **1280x960** | **4x** | **960p** | **1280 (5x)** | **2**

</blockquote>

</details>

## Support

Please consider showing support for this and future projects at **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
