# demo-assembly

## Install nasm

```
brew install nasm
```

## Create build folder

```
mkdir -p build
```

## Assembler

```
nasm -f macho64 main-64.asm -o build/main-64.o
```

## Linker

```
ld -e start -macos_version_min 10.13.0 -static -o build/main-64 build/main-64.o
```

## Run

```
build/main-64
```
