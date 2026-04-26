## Overview
The project is a C-based GUI application that demonstrates polymorphism using void pointers, sizes, and wrapper functions. The application provides features for creating, updating, and deleting shapes such as rectangles and circles.

## Features
- **Shapes**: Supports creation and rendering of different shapes (e.g., rectangle, circle).
- **Polymorphism**: Utilizes void pointers to implement polymorphism.
- **Wrapper Functions**: Uses wrapper functions for each shape type.
- **Transformation**: Allows transformation (scaling, translation) of shapes.
- **GUI**: Provides a simple GUI interface for interaction.

## Project Structure
```
<Project>/
├── build/              # .exe files produced by Main.c
├── src/                # src code
│   ├── Main.c          # Entry point
│   └── *.h             # stand alone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- **C/C++ Compiler and Debugger**: GCC, Clang
- **Make utility**
- **Standard development tools**

## Build & Run
The project is built using Makefiles tailored for different operating systems. Below are the build instructions for each platform:

### Linux
```sh
cd <Project>
make -f Makefile.linux all
```

To run:
```sh
make -f Makefile.linux exe
```

### Windows
```sh
cd <Project>
make -f Makefile.windows all
```

To run:
```sh
make -f Makefile.windows exe
```

### Wine (Cross-compiling for Windows on Linux)
```sh
cd <Project>
make -f Makefile.wine all
```

To run:
```sh
make -f Makefile.wine exe
```

### WebAssembly (Emscripten)
```sh
cd <Project>
make -f Makefile.web all
```

To run:
```sh
make -f Makefile.web exe
```

The build process compiles the source code into an executable, which can be run on the respective platform. The `Makefile` provides targets for cleaning and rebuilding the project.