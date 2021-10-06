# D-Claw_practice

Learning D-Claw (probably Dig-Claw).

## Installation
* Download D-Claw: [src](https://github.com/geoflows/D-Claw), [apps](https://github.com/geoflows/dclaw-apps).
* Defining necessary environment variables in `.bashrc` file.
* Modifying `topotools.py` in `$D-Claw/python/dclaw/` to be consistent with Python3 syntax:
  1. `print` function
  2. `range` function
* Test if python could successfully import d-claw:
  ```bash
  python> import dclaw
  python> import dclaw.topotools as dt 
  ```
* Run `$D-Claw-apps/USGSFlume` for checking:
  1. Initialization:
     ```bash
     > python setinit.py
      ```
  2. Compilation:
     ```bash
     > make new 
     ```
     or 
     ```bash
     > make .exe
     ```
    The old Fortran syntax does not match the one used now (type dismatch). Add the flag in `Makefile`:

    > FFLAGS ?= -fallow-argument-mismatch

    **Possible error:**
    ```diff
    -: Error: Non-numeric character in statement label at (1)
    -call.i:1:3:
    ```
    This is probably because Fortran does not understand the path in `call.i`. **Solution:** delete `$D-Claw/geoclaw/2d/lib_dig/call.i`.

  3. Produce output:
     ```bash
     > make .output
     ```
     Should further fix some `print` function incompatiblity in `setrun.py`.
     This works??
     ```bash
     > make .plots
     ```
* Fix the visualization errors.

## Apps and Codes
