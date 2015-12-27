# mjpg-streamer

This is the original mjpg-streamer from `svn://svn.code.sf.net/p/mjpg-streamer/code/ mjpg-streamer`
and has been applied patched from `https://github.com/raspberrypi/firmware/issues/347` to fix MJPEG stream from my Logitech C110 webcam for the Raspberry Pi 2.

Before the patch, i only able to use YUV format. Got the source code, patch, compile and make a switch to MJPEG format reduce the RPI's CPU usage drastically from 30% to under 1%.

### Compile the source

This is how i build it, you may simply follow the steps or add your own optimization flag for the compilation.

```
# git clone git@github.com:frengky/mjpg-streamer.git mjpg-streamer
# cd mjpg-streamer/mjpg-streamer
# export CFLAGS="-mcpu=cortex-a7 -mfpu=neon -mfloat-abi=hard"
# make USE_LIBV4L2=true
```

Thanks to the original author and credits to someone out there who provide the patch.
Enjoy.

