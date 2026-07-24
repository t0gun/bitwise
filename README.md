# bitwise

A small CLI tool built  for learning how bitwise operations work in rust from first principles.


## Features

- **Base converter** — show a number in binary and hex using manual implementation
- **Core operators** — `&`, `|`, `^`, `~`, `<<`, `>>`
- **Compound assignment** — `&=`, `|=`, `^=`, `<<=`, `>>=` with before/after output
- **Bit manipulation** — `set`, `clear`, `toggle`, `test` individual bits
- **Popcount** — count set bits (manual loop, verified against built-in)
- **Flag combiner** — OR named flags into a combined bitmask
- **Flag inspector** — test which named flags are set in a value
- **Type experiments** — see how `u8`/`u16`/`u32`/`u64` and overflow differ



## Usage

```
cargo run -- convert 0b1111
cargo run -- 0b1111 & 0b1010
cargo run -- 0b1111 &= 0b1010
cargo run -- set 0b0001 2
cargo run -- test 0b1010 3
cargo run -- popcount 0xFF
cargo run -- combine FLAG_A FLAG_C
cargo run -- inspect 0b0101
cargo run -- types 0xFF & 0x0F
cargo run -- --help
```
