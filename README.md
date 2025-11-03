# CS-Postex-Template

The `postexMain` entrypoint can be found in `postexmain.zig`.

## Building 

`zig build-lib -dynamic postexmain.zig -target x86_64-windows -O ReleaseSmall -femit-bin=./postex.dll -fno-emit-implib`

Optimizing for size:

`zig build-lib -dynamic postexmain.zig -target x86_64-windows -mcpu generic+64bit -O ReleaseSmall -femit-bin=./postex.dll -fno-emit-implib -fstrip -fno-unwind-tables -fomit-frame-pointer -flto --gc-sections -fsingle-threaded`

## Usage

The DLL can be execute from a Beacon using `execute-dll`:

`execute-dll /path/to/dll/postex.dll`

## Example

![](https://github.com/Sizeable-Bingus/CS-Postex-Template/blob/main/img/console.png)
