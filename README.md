# Unofficial OpenGL VSYNC Demo for Linux

This is a very basic OpenGL demo for testing vsync technology on Linux.

The demo simply draws a vertical bar moving accross the screen at constant speed,
but deliberately rendered at a variable frame rate.

The min and max frame rates can be manually changed at runtime, by step of 10 fps
and with a min of 10 fps.

The demo also allows to toggle V-Sync on/off. Here are the expected effects:

| V-Sync | Effects
|:------:|--------
|   ON   | No tearing but stuttering below monitor's refresh rate
|   OFF  | Tearing, stuttering below monitor's refresh rate

![Screenshot of gl-gsync-demo](images/screenshot.png)

## Dependencies

The demo is written in C99 and uses the legacy OpenGL 1.x API and requires the
following libraries:

* [FreeGLUT](http://freeglut.sourceforge.net/)
* [GLEW](http://glew.sourceforge.net/)
* libXNVCTRL (from [nvidia-settings](https://github.com/NVIDIA/nvidia-settings))

On Ubuntu, you can install dependencies with the following command:

```
sudo apt install freeglut3-dev libglew-dev libxnvctrl-dev
```

You will also need NVIDIA's proprietary driver and its development files installed.

## Build instructions

In project's root directory, type:

``
make
``

After building, you can run the demo by typing:

``
./gl-gsync-demo
``

## License

See the [LICENSE](LICENSE) file for license rights and limitations (MIT).
