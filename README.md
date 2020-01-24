# Spectrum game dev in ZX BASIC

Place for me to keep track of what I'm doing.

## Compile basic code using [ZXBASIC](https://github.com/boriel/zxbasic) as a .tap file

```python
zxb -taB main.bas
```

## Compile your loading screen (.scr) file as a .tap file and merge both tap files into single one

```bash
./pasmo --tap --name SCREEN loading_screen.asm loading_screen.tap
cat main.tap loading_screen.tap game.tap
```

## Needed to compile pasmo tool for mac

```bash
cd tools/pasmo-0.5.4.beta2
./configure
make
```
