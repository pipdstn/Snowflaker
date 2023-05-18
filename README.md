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