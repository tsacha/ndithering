This project is a fork of [nvibrant](https://github.com/Tremeschin/nvibrant).


```sh
# Clone the code alongside nvidia kernel headers
git clone https://github.com/tsacha/ndithering && cd ndithering
git submodule update --init --recursive
```

From here, you can either build only the C++ part for a target driver:

```sh
# Any tag from https://github.com/NVIDIA/open-gpu-kernel-modules/tags
$ cd open-gpu && git checkout 575.64.03 && cd ..

# Configure and compile project, final binary at 'build' directory
$ meson setup --buildtype release ./build && ninja -C ./build
$ ./build/ndithering 0
```
