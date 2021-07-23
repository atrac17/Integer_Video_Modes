![5](https://user-images.githubusercontent.com/32810066/126727672-b63f5a04-28ad-436e-b3f2-8e0029f0f9eb.png)

## General Information

W.I.P

## Updater Information

W.I.P

## Compatible Display List

W.I.P

# Custom Video Mode Information

## Integer Scaled Custom Video Modelines

<details>

<summary><b>VRR Capable Display</a></b></summary>

----

<details>

<summary><b>Arcade Core Video Modes <a href="https://www.github.com/jotego">(Jotego)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default display resolution for the MiSTer.ini should always be 720p. When generating a pre-configured MiSTer.ini this will be the default.

- Unless stated below, the default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. When generating a pre-configured MiSTer.ini they will have the option to configure vsync_adjust.

----

## <summary1><b>Capcom CP System Cores</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.00 MHz** | **59.6294 Hz NTSC** | **384x224**| **135:176** | **1280:973**|

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1152,48,32,80,896,3,10,13,72580`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1152x896** | **4x** | **896p** | **1152 (3x)**
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1536x1120** | **5x** | **1120p** | **1536 (4x)**
**`video_mode=1920,48,32,80,1344,3,10,25,172474`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1920x1344** | **6x** | **1344p** | **1920 (5x)**

</blockquote>

## <summary1><b>Konami 007121 (Contra Based) Cores</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.25 MHz** | **59.1874 Hz NTSC** | **280x240**| **54:55** | **200:163** |

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1120,48,32,80,896,3,7,16,70810`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1120x896** | **4x** | **896p** | **1120 (4x)**
**`video_mode=1400,48,32,80,1120,3,7,22,107827`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1400x1120** | **5x** | **1120p** | **1400 (5x)**
**`video_mode=1680,48,32,80,1344,3,7,28,152573`** | [**jtcontra**] [**jtcomsc**] [**jtlabrun**] | **280x240**| **1680x1344** | **6x** | **1344p** | **1680 (6x)**

</blockquote>

----

</details>

<details>

<summary><b>Arcade Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default display resolution for the MiSTer.ini should always be 720p. When generating a pre-configured MiSTer.ini this will be the default.

- Unless stated below, the default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. When generating a pre-configured MiSTer.ini they will have the option to configure vsync_adjust.

----

### W.I.P

----

</details>

<details>

<summary><b>Console Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>MiSTer.ini Information</b></summary1>

- The default display resolution for the MiSTer.ini should always be 720p. When generating a pre-configured MiSTer.ini this will be the default.

- Unless stated below, the default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. When generating a pre-configured MiSTer.ini they will have the option to configure vsync_adjust.

- If a core has Dual Mode=Yes below, then there will only be one primary video mode available as the core supports multiple systems for one video mode. For custom aspect ratios, the first will be for the primary hardware and the other for the secondary hardware. This only applies to Dual Mode=Yes video modes.

- Below are the correct custom aspect ratios for each console core. These will be generated in the pre-configured MiSTer.ini files. The end-user can download pre-configured .cfg files for each core if applicable.

---

### <summary1><b>Console Core Custom Aspect Ratios:</b></summary1> 

- The vertical resolution should match the modline. This will tell you which custom aspect ratio to utilize.

----

<details>

<summary><b>Primary Custom Aspect Ratios</b></summary>

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

<summary><b>Secondary Custom Aspect Ratios</b></summary>

|Console|Core|Custom Aspect Ratio|Custom Aspect Ratio|Dual Mode|Resolution|
|--|--|--|--|--|--|
**Famicom / Nintendo Entertainment System** | [**nes**] | **`custom_aspect_ratio_1=64:49`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**224p**_ |
**Super Famicom / Super Nintendo** | [**snes**] | **`custom_aspect_ratio_1=128:105`**| **`custom_aspect_ratio_2=8:7`** | **No** | _**240p**_ |

</details>

----

### **Console Core Custom Video Modes:**

- Utilize the primary modelines for dual mode cores listed below. Utilize thecustom aspect ratios provided above.

----

<details>

_<summary><b>Sega Hardware</b></summary>_

## <summary1><b>Sega SG-1000</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x192**| **8:7** | **32:21**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**coleco**] | **256x192**| **1280x960** | **5x** | **960p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**coleco**] | **256x192**| **1536x1152** | **6x** | **1152p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**coleco**] | **256x192**| **1792x1344** | **7x** | **1344p** | **1792 (7x)**

</blockquote>

## <summary1><b>Sega Mark III / Sega Master System (Sega SG-1000 Compatible)</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x192**| **8:7** | **32:21**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1536,48,32,80,1152,3,4,26,120586`** | [**sms**] | **256x192**| **1536x1152** | **6x** | **1152p** | **1536 (6x)** | **Yes**

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|Dual Mode|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**sms**] | **256x192**| **1280x960** | **5x** | **960p** | **1280 (5x)** | **No**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**sms**] | **256x192**| **1792x1344** | **7x** | **1344p** | **1792 (7x)** | **No**

</blockquote>

## <summary1><b>Sega Mega Drive / Sega Genesis</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.71 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x224**| **8:7** | **64:49**

- <summary><b>VRR Capable Display Modes</b></summary>

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

## <summary1><b>Sega Game Gear</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **59.922751013551 Hz NTSC** | **160x144**| **8:7** | **128:105**

- <summary><b>VRR Capable Display Modes</b></summary>

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

## <summary1><b>Sega Mega CD / Sega CD</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.711647 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**

- <summary><b>VRR Capable Display Modes</b></summary>

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

## <summary1><b>Nintendo Famicom / Nintendo Entertainment System</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x240**| **8:7** | **128:105**
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224**| **8:7** | **64:49**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**nes**] | **256x240**| **1280x960** | **4x** | **960p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1200,3,10,22,125674`** | [**nes**] | **256x240**| **1536x1200** | **5x** | **1200p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1440,3,10,28,173455`** | [**nes**] | **256x240**| **1792x1440** | **6x** | **1440p** | **1792 (7x)**

- _<b>Utilize the Secondary Modelines below if you enable Hide Overscan: Yes and Mask Edges: Auto in the MiSTer OSD</b>._

|Secondary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,896,3,10,13,79661`** | [**nes**] | **256x224**| **1280x896** | **4x** | **896p** | **1280 (5x)**
**`video_mode=1536,48,32,80,1120,3,10,19,117228`** | [**nes**] | **256x224**| **1536x1120** | **5x** | **1120p** | **1536 (6x)**
**`video_mode=1792,48,32,80,1344,3,4,32,161977`** | [**nes**] | **256x224**| **1792x1344** | **6x** | **1344p** | **1792 (7x)**

</blockquote>

## <summary1><b>Game Boy / Game Boy Color</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**4.194304 / 8.388608 MHz** | **59.727500569606 Hz NTSC** | **160x144**| **10:9** | **3200:1971**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modelines NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|
|--|--|--|--|--|--|--|
**`video_mode=1120,48,32,80,1008,3,10,16,79642`** | [**gameboy**] | **160x144**| **1120x1008** | **7x** | **1008p** | **1120 (7x)**
**`video_mode=1280,48,32,80,1152,3,10,20,102384`** | [**gameboy**] | **160x144**| **1280x1152** | **8x** | **1152p** | **1280 (8x)**
**`video_mode=1440,48,32,80,1296,3,10,24,127968`** | [**gameboy**] | **160x144**| **1440x1296** | **9x** | **1296p** | **1440(9x)**
**`video_mode=1600,48,32,80,1440,3,10,28,156394`** | [**gameboy**] | **160x144**| **1600x1440** | **10x** | **1440p** | **1600 (10x)**

</blockquote>

## <summary1><b>Super Famicom / Super Nintendo</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224 / 256x240**| **8:7** | **64:49**
**10.47 MHz** | **60.098813897441 Hz NTSC** | **512x224 / 512x240**| **16:7** | **128:105**

- <summary><b>VRR Capable Display Modes</b></summary>

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

</details>

</details>

----

<details>

<summary><b>2048x1536 Hi-Res CRT Monitor</b></summary>

----

### W.I.P

----

</details>

----

<details>

<summary><b>1280x1024 CRT Monitor</b></summary>

----

### W.I.P

----

</details>

----

## Integer-Step Scaled Custom Video Modelines

<details>

<summary><b>1280x1024 IPS LCD TFT Display</b></summary>

----

<details>

<summary><b>Arcade Core Video Modes <a href="https://www.github.com/jotego">(Jotego)</a></b></summary>

## <summary1><b>General Information</b></summary1>

- Designed for 5:4 IPS/LCD/TFT displays with a native resolution of 1280x1024. Not to be utilized on CRT monitors with the same native resolution.

## <summary1><b>MiSTer.ini Information</b></summary1>

- Unless stated below, the default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. When generating a pre-configured MiSTer.ini they will have the option to configure vsync_adjust.

## <summary1><b>Capcom CP System Cores</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**8.00 MHz** | **59.6294 Hz NTSC** | **384x224**| **135:176** | **1280:973**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modeline NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1248,48,32,80,1008,3,10,16,87606`** | [**jtcps1**] [**jtcps15**] [**jtcps2**] | **384x224**| **1248x1008** | **4.5x** | **1008p** | **1248 (3.25x)** | **3**

</blockquote>

----

</details>

<details>

<summary><b>Arcade Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>General Information</b></summary1>

- Designed for 5:4 IPS/LCD/TFT displays with a native resolution of 1280x1024. Not to be utilized on CRT monitors with the same native resolution.

## <summary1><b>MiSTer.ini Information</b></summary1>

- Unless stated below, the default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. When generating a pre-configured MiSTer.ini they will have the option to configure vsync_adjust.

----

### W.I.P

----

</details>

<details>

<summary><b>Console Core Video Modes <a href="https://github.com/MiSTer-devel">(MiSTer-devel)</a></b></summary>

## <summary1><b>General Information</b></summary1>

- Designed for 5:4 IPS/LCD/TFT displays with a native resolution of 1280x1024. Not to be utilized on CRT monitors with the same native resolution.

## <summary1><b>MiSTer.ini Information</b></summary1>

- Unless stated below, the default MiSTer.ini settings for each core will be vscale_mode=1 and vsync_adjust=2. When generating a pre-configured MiSTer.ini they will have the option to configure vsync_adjust.

----

<details>

_<summary>Sega Hardware</summary>_

## <summary1><b>Sega Mega Drive / Sega Genesis</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**6.71 MHz** | **59.922751013551 Hz NTSC** | **320x224**| **32:25** | **64:49**
**5.37 MHz** | **59.922751013551 Hz NTSC** | **256x224**| **8:7** | **64:49**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modeline NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**genesis**] | **320x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (4x)** | **2**

|Secondary Modeline NTSC|Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**genesis**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2**

</blockquote>

</details>

----

<details>

_<summary>Nintendo Hardware</summary>_

## <summary1><b>Super Famicom / Super Nintendo</b></summary1>

<blockquote>

- <summary><b>Hardware Information</b></summary>

|Pixel Clock|Refresh Rate|Resolution (Visible)|Pixel Aspect Ratio|Display Aspect Ratio|
|--|--|--|--|--|
**5.37 MHz** | **60.098813897441 Hz NTSC** | **256x224 / 256x240**| **8:7** | **64:49**
**10.47 MHz** | **60.098813897441 Hz NTSC** | **512x224 / 512x240**| **16:7** | **128:105**

- <summary><b>VRR Capable Display Modes</b></summary>

|Primary Modeline NTSC|FPGA Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,1008,3,10,16,89597`** | [**snes**] | **256x224**| **1280x1008** | **4.5x** | **1008p** | **1280 (5x)** | **2**

|Secondary Modeline NTSC|FPGA Core|Resolution (Visible)|Resolution (Scaled)|Integer (Scaled)|Resolution (Vert.)|Resolution (Hor.)|**vscale_mode**|
|--|--|--|--|--|--|--|--|
**`video_mode=1280,48,32,80,960,3,4,21,85363`** | [**snes**] | **256x240**| **1280x960** | **4x** | **960p** | **1280 (5x)** | **2**

</blockquote>

----

</details>

----

</details>

</details>

----

<details>

<summary><b>2048x1536 IPS LCD HI-DPI Display</b></summary>

----

### W.I.P

----

</details>

----

<details>

<summary><b>1280x1024 CRT Monitor</b></summary>

----

### W.I.P

----

</details>

----
## Support

Please consider showing support for this and future projects at **[Patreon](https://www.patreon.com/atrac17)**. While it isn't necessary, it's greatly appreciated.

![123269746-440cb600-d4cd-11eb-9e11-90ed7fc951d7](https://user-images.githubusercontent.com/32810066/123511968-b529a600-d652-11eb-9cd5-ca45d16e81a5.png)
