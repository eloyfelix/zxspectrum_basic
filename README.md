# ZX Spectrum game dev in BASIC

Place for me to keep track of what I'm doing.

## Compile basic code using [ZXBASIC](https://github.com/boriel/zxbasic) as a .tap file

```python
zxb -taB main.bas
```

## Compile your loading screen (.scr) file as a .tap file and merge both tap files into single one

You will first need to get your .scr image. I used: https://github.com/KodeMunkie/imagetozxspec.

```bash
./pasmo --tap --name SCREEN loading_screen.asm loading_screen.tap
cat main.tap loading_screen.tap > game.tap
```

## Compile [pasmo](http://pasmo.speccy.org/)

```bash
cd tools/pasmo-0.5.4.beta2
./configure
make
```

## Save emulation video with fuse (in .fmf format) and convert it to mp4. [fuse-utils](https://sourceforge.net/projects/fuse-emulator/files/fuse-utils/1.4.3/) needed.

Compile fuse-utils
```bash
cd tools/fuse-utils-1.4.3
./configure
make
```

```bash
./fmfconv emu_video.fmf | ffmpeg -i - -aspect 4:3 output.mp4
```
