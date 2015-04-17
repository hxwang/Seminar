## Content-Adaptive Display Power Saving in Internet Mobile Streaming

- Mengbai Xiao
- Date: 3/6/2015

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

### Conclusion
- dim the light level 
- build a decision model to predict the power savings resulting from the CAD
- 83.4% vedio can save power


### CS800 Summary
- Speaker: Mengbai Xiao
- Time: 03/06/2015
- Summary: In this lecture, the speaker presents his work on deisgining and implementation of content adpative display power saving mechanisms for reducing power consumption on mobile device. The main idea is to tune the backlight based on GPU rather than CPU, which allows them to design more complex algorithms. They designed an algorithm based on dynamic programming. 
- As the battery capacity is constrained in mobile devices, it is important to design energy efficient mechanism to increase the power-on time of mobile device. It shows that the display consumes 68% power during the playback, and most of the energy is consumed by back light. In order to save power, backlight sacling techniques has been proposed. This technique reduce power consumption by dimming the display backlight. Meanwhile, the brightness preceived by the human eye is maintained by increasing the affeted image's luminance. 
- The strongness of their mechanism is that they solved the following three challeges. First, to maintain image fidelity, the backlight level cannot be lower than a point determined by the brightless characteristic of an image. This constraint requires that the maximum pixel lumnnance of every frame to be computed, which can be both time consuming and energy intensive. Second, it is infeasible to adjust the backlight level for every freame because the display hardware takes time to perform the djustment. Thrid, larger inter-frame backlight varianction ca cause flickering effects. 
- Their technique is based on the fact that by backlight scaling and combined RGB values with the tuned backlight, the output could be the same, while the power consumption reduced. In their implementaion, YUV-RGB conversion is reuqired. They use GPU rather than CPU as GPU is better at computation. However,  GPU is also energy consuming. They implement the designed mechanism on android and experiment with more than 470 randomly selected YouTube Vedio clips. They dim the light a decision model to predict the power savings resulting from the CAD. The results showed that the deisgned mechanism can reduce energy consumption which not affect users' satisfaction. In their experiments, 83.4% vedio can save power.
- The weakness of their work is that they didn't do the real power consumption measurment in the experiments. Instead, they use a decision model that correlates the power consumption with backlight. However, it would be more accurate to do the real experiment. In addition, it is also interesting to measure the overhead of computation. 
