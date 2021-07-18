[Hardware Pixel Clock]:
5.37MHz / 10.47MHz

[Refresh Rate]:
60.098813897441Hz NTSC
50.006978908189Hz PAL

[Pixel Aspect Ratio]:
8:7 ;PAR

[Display Aspect Ratio]:
64:49 ;DAR

[Visible Line Resolution]:
256x224 (5.37MHz)
256x240 (5.37MHz)
512x224 (10.47MHz)
512x240 (10.47MHz)

[Integer Scaling]:
896		;4x (Ver 224p)
1120	;5x (Ver 224p)
1344	;6x (Ver 224p)
1008	;4.5x (Ver 224p)

960		;4x (Ver 240p)
1200	;5x (Ver 240p)
1440	;6x (Ver 240p)
1020	;4.5x (Ver 240p)

1024	;4x (Hor)
1280	;5x (Hor)
1536	;6x (Hor)
1792	;7x (Hor)

MiSTer.ini settings for Super Famicom / Super Nintendo

[VRR Capable Display]:
[snes] ;NTSC 60.0988Hz / 5.37MHz / 256x224 Mode / Integer / VRR Capable Display
;video_mode=1280,48,32,80,896,3,10,13,79661		;4x (Ver) / 5x (Hor)
;video_mode=1536,48,32,80,1120,3,10,19,117228	;5x (Ver) / 6x (Hor)
video_mode=1792,48,32,80,1344,3,4,32,161977		;6x (Ver) / 7x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=64:49		;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[snes] ;PAL 50.0069Hz / 5.37MHz / 256x224 Mode / Integer / VRR Capable Display
;video_mode=1280,48,32,80,896,3,10,9,79315		;4x (Ver) / 5x (Hor)
;video_mode=1536,48,32,80,1120,3,10,14,116719	;5x (Ver) / 6x (Hor)
video_mode=1792,48,32,80,1344,3,4,25,161157		;6x (Ver) / 7x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=64:49		;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[...]
[snes] ;NTSC 60.0988Hz / 5.37MHz / 256x240 Mode / Integer / VRR Capable Display
;video_mode=1280,48,32,80,960,3,4,21,85363		;4x (Ver) / 5x (Hor)
;video_mode=1536,48,32,80,1200,3,10,22,125674	;5x (Ver) / 6x (Hor)
video_mode=1792,48,32,80,1440,3,10,28,173455	;6x (Ver) / 7x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=128:105	;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[snes] ;PAL 50.0069Hz / 5.37MHz / 256x240 Mode / Integer / VRR Capable Display
;video_mode=1280,48,32,80,960,3,4,16,84931		;4x (Ver) / 5x (Hor)
;video_mode=1536,48,32,80,1200,3,10,16,125063	;5x (Ver) / 6x (Hor)
video_mode=1792,48,32,80,1440,3,10,21,172635	;6x (Ver) / 7x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=128:105	;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[Compatibility Mode Display]:
[snes] ;NTSC 60.0988Hz / 5.37MHz / 256x224 Mode / Integer / Compatibility Mode Display
;video_mode=1920,48,32,80,896,3,10,13,115066		;4x (Ver)
;video_mode=1920,48,32,80,1120,3,10,19,143770		;5x (Ver)
video_mode=1920,48,32,80,1344,3,10,26,172598		;6x (Ver)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=64:49		;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[snes] ;PAL 50.0069Hz / 5.37MHz / 256x224 Mode / Integer / Compatibility Mode Display
;video_mode=1920,48,32,80,896,3,10,9,114566		;4x (Ver)
;video_mode=1920,48,32,80,1120,3,10,14,143146	;5x (Ver)
video_mode=1920,48,32,80,1344,3,10,19,171725	;6x (Ver)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=64:49		;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[...]
[snes] ;NTSC 60.0988Hz / 5.37MHz / 256x240 Mode / Integer / Compatibility Mode Display
;video_mode=1920,48,32,80,960,3,10,15,123302	;4x (Ver)
;video_mode=1920,48,32,80,1200,3,6,26,154128	;5x (Ver)
video_mode=1920,48,32,80,1440,3,4,34,184829		;6x (Ver)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=128:105	;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[snes] ;PAL 50.0069Hz / 5.37MHz / 256x240 Mode / Integer / Compatibility Mode Display
;video_mode=1920,48,32,80,960,3,10,10,122678	;4x (Ver)
;video_mode=1920,48,32,80,1200,3,6,20,153379	;5x (Ver)
video_mode=1920,48,32,80,1440,3,4,27,183955		;6x (Ver)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=128:105	;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2
[5:4 LCD Display]:
[snes] ;NTSC 60.0988Hz / 5.37MHz / 256x224 Mode / Half Integer / 5:4 Display
video_mode=1280,48,32,80,1008,3,10,16,89597 ;4.5x (Ver) / 5x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=64:49		;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=2
vsync_adjust=2
[snes] ;PAL 50.0069Hz / 5.37MHz / 256x224 Mode / Half Integer / 5:4 Display
video_mode=1280,48,32,80,1008,3,10,11,89165		;4.5x (Ver) / 5x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=64:49		;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=2
vsync_adjust=2
[...]
[snes] ;NTSC 60.0988Hz / 5.37MHz / 256x240 Mode / Half Integer / 5:4 Display
video_mode=1280,48,32,80,1020,3,10,17,90720		;4.5x (Ver) / 5x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=128:105	;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=2
vsync_adjust=2
[snes] ;PAL 50.0069Hz / 5.37MHz / 256x240 Mode / Half Integer / 5:4 Display
video_mode=1280,48,32,80,1020,3,10,12,90288		;4.5x (Ver) / 5x (Hor)
;original_aspect_ratio=64:49
;fullscreen_aspect_ratio=video_mode selected
custom_aspect_ratio_1=128:105	;DAR
custom_aspect_ratio_2=8:7		;PAR
vscale_mode=1
vsync_adjust=2