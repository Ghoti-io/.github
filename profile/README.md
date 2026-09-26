# Ghoti.io (it's pronounced "[Fish](https://en.wikipedia.org/wiki/Ghoti)")

Dependency-light, cross-platform C libraries. C17, **LGPL-3.0-only**.

## Welcome

This is the org page for the Ghoti.io suite of libraries.  They are my own collection of libraries that exist simply because I wanted to build them.  They are primariliy for my own projects, but you can use them, too... they are LGPL-3.

### Puns

- "Ghoti" is pronounced "[Fish](https://en.wikipedia.org/wiki/Ghoti)".
  - I thought it was funny.
  - It takes the basics of English phonetics and uses them for it's own purposes.  This project is written in C... you can definitely do unexpected things!
- ".io" (the suffix)
  - It has come to represent technology (input/output), but it actually stands for [Indian Ocean](https://en.wikipedia.org/wiki/.io).
  - "Fish" and "Indian Ocean"... "Ghoti.io".
- **C**, the programming language.
  - "C"... "sea"... the joke writes itself.
- Most libraries in this collection are named practically, but some fall victim to the silliness:
  - **Tang** (the scripting language in this project that I wanted to use for templating)
    - A common name for a type of [fish](https://en.wikipedia.org/w/index.php?title=Tang_(fish)&redirect=no).
    - "Tang"... "T - ang"... **T**-emplate l-**ANG**-uage.  It's a stretch, but it works.
    - `ctang` is the name of the library, naming the implementor (C) and the implementee (Tang).  Like "cpython".
  - **CJelly** A GUI library (very early development at this moment)
    - A GUI ("gooey") Ghoti ("fish") in the .io ("Indian Ocean").  It's obviously a jellyfish.
    - `cjelly`... "[sea jelly](https://en.wikipedia.org/wiki/Jellyfish)"
    - I think I'm hilarious.

## Start here

**[`suite`](https://github.com/Ghoti-io/suite)** clones every library, builds them in dependency order, and renders the combined manual.

### Very Quick Start

```bash
mkdir ghoti.io && cd ghoti.io
git clone https://github.com/Ghoti-io/suite.git
cd suite && ./clone.sh && ./install.sh
```

## The libraries

| Library | What it is |
| --- | --- |
| [`cutil`](https://github.com/Ghoti-io/cutil) | Foundation utilities: containers, hash tables, a traced allocator, overflow-checked size math, threads and synchronisation |
| [`unicode`](https://github.com/Ghoti-io/unicode) | The Unicode Character Database as generated tables, plus the UAX algorithms over them |
| [`chron`](https://github.com/Ghoti-io/chron) | Time: instants, civil dates, calendars, durations, time zones, and the text formats for all of them |
| [`compress`](https://github.com/Ghoti-io/compress) | Streaming compression: deflate, gzip, lz4, lzw, rle, zstd, with crc32 and xxhash |
| [`text`](https://github.com/Ghoti-io/text) | JSON, CSV, JSON Schema, streaming YAML, IDNA2008 and UTS #46 host names |
| [`image`](https://github.com/Ghoti-io/image) | Raster imaging: hand-written PNG/APNG, JPEG and BMP codecs, colour management, metadata |
| [`model`](https://github.com/Ghoti-io/model) | 3D model formats: Wavefront OBJ geometry and MTL materials |
| [`regex`](https://github.com/Ghoti-io/regex) | Regular expressions across several dialects, over one parser and three engines |
| [`ctang`](https://github.com/Ghoti-io/ctang) | Tang, a template language with an x86-64 JIT and a bytecode-VM fallback |
| [`cjelly`](https://github.com/Ghoti-io/cjelly) | Vulkan-first cross-platform GUI toolkit that draws its own widgets |
| [`font`](https://github.com/Ghoti-io/font) | Fonts: reading, rasterisation, shaping and paragraph layout |

Not every library is finished, and each repository's own README says where it stands. `suite` builds whatever is checked out.

## License

Every library is LGPL-3.0-only. Each repository carries `COPYING` (GPL-3.0) and `COPYING.LESSER` (LGPL-3.0), because LGPLv3 is written as a set of additional permissions on top of GPLv3.

**Contributions are not being accepted at this time.** That may change in the future.
