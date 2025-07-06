# kpukboard-zmk
Firmware for my keyboard

https://github.com/kriku/kpukboard-pcb

## Build instructions local
```basjh
west build -d build/right -b seeeduino_xiao_ble -- -DZMK_CONFIG=/home/otsu/github/kpukboard-zmk/config -DZMK_EXTRA_MODULES="/home/otsu/github/kpukboard-zmk/zmk-helpers;/home/otsu/github/kpukboard-zmk/zmk-tri-state;/home/otsu/github/kpukboard-zmk/zmk-rgbled-widget;" -DSHIELD="kpukboard_right"
```

## Flash your board
```bash
-- identify your board
-- enter into debug mode on xiao
-- usually /dev/sdb
lsblk

-- mount
sudo mount /dev/sdb/ ~/some-mnt

-- copy firmware
sudo cp ~/zmk/app/build/left/zephyr/zmk.uf2

-- umount
sudo umount ~/some-mnt
-- 
```

### DEFAULT

```
    dvorak

    = ' , . p y   f g c r l /
    ` a o e u i   d h t n s -
      ; q j k x   b m w v z

    йцукен

    ъ й ц у к е   н г ш щ з х
    ё ф ы в а п   р о л д ж э
      я ч с м и   т ь б ю .
```

### SYMBOL
```
    dvorak

    . [ ] { } +   * & a | ^ .
    . < > ( ) =   - a a a _ .
      ~ ! @ # \   / $ % ? 3

    йцукен

    . [ ] { } +   * ? а / : .
    . Ц У ( ) ъ   э а а а Э .
      Ë ! " № \   х ; % Х 3

a - means arrow
. - means transparent
```

### NUMBER
```
    ALT +
    . s 7 8 9 +   * 7 8 9 % .
    . s 4 5 6 =   - 4 5 6 0 .
      s 1 2 3 \   / 1 2 3 .

s - means scene selection (CTRL+ALT+GUI+F1/F2/F3)
```

### FUNCTIONAL
```
        F F F F
    . b 7 8 9 2   v u a d x .
    . b 4 5 6 1   v a a a x .
      b 1 2 3 0   m p p n 3

b - means bluetooth behavior
numbers - F1, F2, etc
```

### STREAMING
```
        F F F F
    . b 7 8 9 2   v u a d x .
    . b 4 5 6 1   v a a a x .
      b 1 2 3 0   m p p n 3

b - means bluetooth behavior
numbers - F1, F2, etc
```
