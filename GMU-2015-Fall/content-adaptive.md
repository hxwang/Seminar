## Content-Adaptive Display Power Saving in Internet Mobile Streaming

- Mengbai Xiao

### Intro
- Power during playback
  - the display consumes 68% power during the playback
    - most of the energy consumes by back light
- Challenge of vedios
  

### Tech
- backlight scaling
  - combine RGB values and back light, the output will be the same, while the power consumption reduce
  

### Apply to Vedio
- apply backlight frame by frame

### Related Work
- existing solution: either requires hardware support, proxy, or has distoration

### CAD 
- backlight determine algorithm, use dynamic programming
  - constraints
    - backlight level must follow the maximum pixel luminance
    - user experience, can not have large jump
    - hardware
- GPU, pixel ...

### Luminance compensation
- YUV-RGB conversion is reuqired
- use GPU rather than CPU
  - GPU is better at computation
  - however, the GPU is also energy consuming

### Implementation
- use android app
- model
  - luminance v.s. energy consumption

