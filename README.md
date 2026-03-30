# FREAK Apps & Demos

Demo applications and showcase programs written in [FREAK](https://github.com/FREAK-lang-dev/Freak-lang).

## Apps

| App | Description | Lines |
|-----|-------------|-------|
| [calculator](calculator/) | GUI calculator with black+purple theme, keyboard input, expression history | ~340 |
| [rpg-console](rpg-console/) | Console RPG with character stats and combat | ~90 |
| [anime-battle](anime-battle/) | Anime-themed battle simulator | ~60 |
| [ui-showcase](ui-showcase/) | UI widget showcase and window tests | ~2500 |

## Demos

| Demo | Description |
|------|-------------|
| [demos/http](demos/http/) | HTTP/1.1 client demo (GET/POST over TCP) |
| [demos/json](demos/json/) | JSON parser/serializer demos |
| [demos/algorithm](demos/algorithm/) | Sort, search, and algorithm demos |
| [demos/std](demos/std/) | Standard library feature demos |
| [demos/llvm](demos/llvm/) | LLVM backend comprehensive test |

## Building

These require the FREAK compiler. Install it from [Freak-lang](https://github.com/FREAK-lang-dev/Freak-lang).

```bash
# Using the self-hosting compiler (recommended)
freakc build calculator/calculator.fk

# Using the Python bootstrap compiler
python -m freakc build calculator/calculator.fk
```

The calculator requires the UI runtime and must be linked with platform libraries:
```bash
freakc build calculator/calculator.fk --ui
```

## Self-Hosted

The calculator was the first app compiled entirely through the self-hosting FREAK compiler — zero Python in the pipeline:

```
calculator.fk -> freakc_v2.exe (FREAK compiler written in FREAK) -> C -> clang -> native binary
```
