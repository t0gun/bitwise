# bitwise

A small CLI tool built for learning how bitwise operations work in Go from first principles.

## Features

- **Base converter** — show a number in binary and hex using manual implementation
- **Core operators** — `&`, `|`, `^`, `^` (NOT), `<<`, `>>`
- **Compound assignment** — `&=`, `|=`, `^=`, `<<=`, `>>=` with before/after output
- **Bit manipulation** — set, clear, toggle, test individual bits
- **Popcount** — count set bits (manual loop, verified against `math/bits`)
- **Flag combiner** — OR named flags into a combined bitmask
- **Flag inspector** — test which named flags are set in a value
- **Type experiments** — see how `uint8`/`uint16`/`uint32`/`uint64` and overflow differ

## Usage

```
go run . convert 0b1111
go run . 0b1111 & 0b1010
go run . 0b1111 &= 0b1010
go run . set 0b0001 2
go run . test 0b1010 3
go run . popcount 0xFF
go run . combine FLAG_A FLAG_C
go run . inspect 0b0101
go run . types 0xFF & 0x0F
go run . --help
```

## Go-specific notes

- Go uses `^` for bitwise NOT (not `~` like Rust/C)
- Go has no implicit type conversions — you must explicitly cast (e.g. `uint8(x)`)
- Go wraps silently on overflow — no debug/release distinction like Rust
- All base conversions (binary, hex, decimal) are implemented manually, not via `strconv`
