# radare2 cheat sheet

## r2

hex editor, disassembler and debugger

### command-line options

| Option | Description                        |
|--------|------------------------------------|
| -A     | analyze all and autoname functions |
| -d     | debug file or process id           |
| -w     | open file writable                 |

### radare2 commands

| Command  | Description          |
|----------|----------------------|
| s        | show current address |
| s 0xff00 | go to address 0xff00 |
| pd       | disassemble bytes    |
| pd 10    | disassemble 10 bytes |
| px       | hexdump bytes        |
| px 10    | hexdump 10 bytes     |
| V        | visual mode          |


## rabin2

get information from binary files

### command-line options

| Option | Description             |
|--------|-------------------------|
| -I     | show binary information |
| -s     | show symbols            |
| -S     | show sections           |
| -z     | show strings            |


## rasm2

assemble and disassemble

### command-line options

| Option | Description               |
|--------|---------------------------|
| -a     | set architecture          |
| -b     | set register size         |
| -d     | disassemble               |
| -D     | disassemble with hexpairs |
| -s     | set syntax                |

### examples

disassemble 32-bit x86 hex bytes b82a000000:

```
# rasm2 -a x86 -b 32 -d b82a000000
mov eax, 0x2a
```
