# stm32F746Disco_TgfxQspiSdram
stm32CubeMxIde and TouchGfx with Quad SPI Flash in Memory Mapped Mode and SDRam for frame buffer
It took some doing but this base build is finally working!

After getting the screen frame buffer addressing and screen timing set correctly,
I was able to get the image data @0x90000000 and display it - touch wasn't working, surprise!
I noticed that the timing was not correct so I compared the TouchGfx code and found some overrides that the code generator didn't generate in the stm32CubeIde project.
After updating the code for touch everything appears to work.

Project is due for some optimization since i had to hack up some paths to get it to compile and link.
