

https://github.com/pipdstn/Snowflaker/assets/23411544/d0650ae3-4e5a-4861-bf5e-5be19ca62e71

# Simulation & Rendering Project: Snowflake Simulator

## Building
The Snowflaker program depends on the NCCA NGL graphics library, which must be installed.

The program can be built via the standard CMake build process:
```
mkdir build
cd build
cmake ..
cmake --build .
```

## Controls
The Snowflaker program has a limited interface consisting of the following keyboard commands:

`1`     - Generate a new snowflake.

`SPACE` - Export the current snowflake to a Houdini .geo file in the build folder.

`ESC`   - Exit the program.

## Readout
The UI contains some information about the current snowflake being generated.

- **\# of Particles**: the number of particles present in the presently rendered image. This is not the same as the number of particles which have been generated; the whole image comprises 6 rotations and 6 reflections of the initial particle set, and so this number is 12 times greater than the particle count defined in the snowflake.h header file.

- **Y-bias**: a measure of the "bias" of the snowflake, defined as the ratio between the maximum vertical perturbation allowed during the generation process and the particle radius. Anecdotally, values close to or greater than 1 yeild more satisfactory snowflakes. A Y-bias value close to 0 results in a trivial snowflake.
