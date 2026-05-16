# OpenDIR

A faithful recreation of the MS-DOS `dir` command, modernized for Rust-supporting systems.  
Brings the classic DOS directory listing aesthetic to Linux, Android (Termux), macOS, and Windows — with colors, unicode, and modern file size formatting.

## Features

- DOS-inspired directory listing with a modernized look
- Color-coded file types (source code, archives, media, configs, etc.)
- Wide listing mode (`/W`)
- Recursive directory listing (`/S`)
- Hidden file support (`/A`)
- Pagination (`/P`)
- Sorting by name, size, date, or extension (`/O:N/S/D/E`)
- Free disk space display
- Works on glibc, musl, Bionic (Android), and macOS

## Building

Make sure you have Rust and Cargo installed, then:

```bash
cargo build --release
```

The binary will be at `target/release/opendir`.  
See `BuildInstructions.MD` for platform-specific Rust installation instructions.

## Usage

```
opendir [PATH] [FLAGS]
```

### Flags

| Flag | Description |
|------|-------------|
| `/W` | Wide list format |
| `/P` | Pause after each screen |
| `/S` | Recurse into subdirectories |
| `/A` | Show hidden files (dotfiles) |
| `/O:<key>` | Sort by: N=name, S=size, D=date, E=ext |
| `/H` | Show help |
| `/V` | Show version |

### Examples

```bash
opendir
opendir /home/user /S /A
opendir . /W /O:S
```
