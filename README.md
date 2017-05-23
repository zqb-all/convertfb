convertfb
==========

Convertfb - python-based tool to adapt image to framebuffer


For help with command line options, use:
```bash
convertfb -h
```

### Installation

If you have the python 'python-imaging' module, you can just place convertfb

in a directory on your path, or add the directory containing convertfb

to your path, or just invoke convertfb directly.

This should work:
```bash
sudo cp convertfb /usr/local/bin

convertfb
```
### Example

#### Ubuntu

An example in ubuntu , the screen is 1376x768 and

the size of framebuffer is 1376x768

1. use fbset to show the size of framebuffer
    ```bash
    sudo apt-get install fbset

    sudo fbset -i
    ```
2. convert the image
    ```bash
    sudo apt-get install python-imaging

    convertfb -i demo.bmp -o demo.fb -bw 1376 -bh 768 -f BGRA
    ```
3. show the image

    press Ctrl + Alt + F1 and login in

    ```bash
    sudo cat demo.fb > /dev/fb0
    ```
