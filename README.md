# STM32 base project

## `make` - build and flash your code

### `make` commands

Run `make` to compile the code.

```sh { closeTerminalOnSuccess=false }
# compile code
make
```

Run `make clean` to remove the compiled code. This does not remove the backup.

```sh { closeTerminalOnSuccess=false }
# clean up
make clean
```

Run `make flash` to flash the code to the board.

```sh { closeTerminalOnSuccess=false }
# flash to board
make flash
```

Run `make erase` to erase the code from the board.

```sh { closeTerminalOnSuccess=false }
# erase from board
make erase
```

### `make` variables

Run `make` with `DEBUG=0` to compile the code without debug information.

```sh { closeTerminalOnSuccess=false }
# compile code without debug information
make DEBUG=0
```

Make sure to also flash with `DEBUG=0` as both versions are kept in the build folder.

```sh { closeTerminalOnSuccess=false }
# flash to board without debug information
make flash DEBUG=0
```

### `make` arguments

Run `make` with `V=1` to see the commands that are executed.

```sh { closeTerminalOnSuccess=false }
# show commands
make V=1
```

## folder structure

```sh
├── .vscode/                # vscode settings
├── build/                  # build folder
│   ├── debug/              # debug build
│   │   ├── ...             # all object, dependency and binary files
│   └── release/            # release build
│       ├── ...             # same as in debug, but without debug information
├── ...                     # all Standard CubeMX files
├── backup.zip              # backup of the project
├── Makefile                # makefile to build and flash the code
└── README.md               # this file
```

## VSCode files

### `cpp_properties.json`

Added all information in order to get code completion and linting working.

### `launch.json`

Added a task to start debugging with OpenOCD: `Debug with OpenOCD`.

### `settings.json`

Random file associations and disabling clang-tidy.

### `tasks.json`

Added a task to build the code: `Build`.

Added a task to build flash the code: `Build and Flash`. (default build task)