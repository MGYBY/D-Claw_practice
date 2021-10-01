# D-Claw_practice

Learning D-Claw (probably Dig-Claw).

## Installation
* Defining necessary environment variables in `.bashrc` file.
* Modifying `topotools.py` in `$D-Claw/python/dclaw/` to be consistent with Python3 syntax:
  1. `print` function
  2. `range` function
* 
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
