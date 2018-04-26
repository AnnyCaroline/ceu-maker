# ceu-maker

C�u-Maker is a ...

## Package Generation

C�u-Maker depends on
    [C�u](https://github.com/fsantanna/ceu),
    [C�u-Arduino](https://github.com/fsantanna/ceu-arduino),
    [C�u-SDL](https://github.com/fsantanna/ceu-sdl), and
    [pico-C�u](https://github.com/fsantanna/pico-ceu).

To generate a new version of C�u-Maker, use the instructions as follows.

### Collect all relevant files to C�u-Maker

Clone the source repositories:

```
$ git clone https://github.com/fsantanna/ceu
$ git clone https://github.com/fsantanna/ceu-arduino
$ git clone https://github.com/fsantanna/ceu-sdl
$ git clone https://github.com/fsantanna/pico-ceu
```

Checkout the target version for each of the source repositories, e.g.:

```
$ cd ceu/
$ git checkout v0.30
```

This step can be skipped if you want to use the `master` branches.

Edit `Makefile.dirs` to point to the source repositories:

```
$ vi Makefile.dirs
```

Run `make` to copy the files from the source repositories to `ceu-maker/`:

```
$ make
```

If the command `make` does not exist, follow the instructions in the link below:

https://gist.github.com/evanwill/0207876c3243bbb6863e65ec5dc3f058

### Test

- Open the Windows Explorer in the folder `ceu-maker/bin/` (WIN-A).
    - pico-C�u
        - Open the folder `ceu-maker/samples/pico-ceu/` in another window (WIN-1).
        - Drag & Drop the file `all.ceu` (WIN-1) into the icon `pico-C�u` (WIN-A).
        - Observe the application behavior.
    - C�u-Arduino
        - Plug the Arduino board you want to test.
        - Execute `ceu-maker/arduino-1.8.3/arduino` and configure `Tools->Board` and `Tools->Port`.
        - Open the folder `ceu-maker/samples/ceu-arduino/` in another window (WIN-2).
        - Drag & Drop the file `blink-01.ceu` (WIN-2) into the icon `C�u-Arduino` (WIN-A).
        - Observe the application behavior.
    - Both
        - Open the folder `ceu-maker/samples/both/` in another window (WIN-3).
        - Drag & Drop the same file `serial.ceu` (WIN-3) into the icon `pico-C�u` (WIN-A) and then into the icon `C�u-Arduino` (WIN-A).
        - Observe the application behavior.

