# ARM Cortex M0 First Steps

Dieses Projekt wird im Rahmen der Vorlesung "Systemnahe Programmierung" an der DHBW Ravensburg verwendet.

## Vorraussetzungen
 - Arm Cross-Compiler

### Installation Windows
 - [Arm Cross Toolchain](https://gnutoolchains.com/arm-eabi/)
   Enthält, GCC, Binutils und GDB

### Installation Linux
 - Arm Cross Compiler Paket: _gcc-arm-none-eabi_

### Installation MacOS
TODO

## Compilieren und Linken
 - Compilieren:
   `arm-none-eabi-gcc -c -save-temps -mcpu=cortex-m0 -nostdlib -g -o hello_world.o hello_world.c`
 - Linken:
   `arm-none-eabi-gcc -o hello_world.o hello_world.elf`

## Generiertes Output analysieren (optional)
 - ELF-Sections anzeige:
   `arm-none-eabi-objdump -x hello_world.o`
 - ELF-File disassemblieren (mit Quellcode-Verknüpfung):
   `arm-none-eabi-objdump -d Simple.elf`
   `arm-none-eabi-objdump -d -S Simple.elf`
