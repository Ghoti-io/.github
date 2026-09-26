# Ghoti.io

Hand-written, dependency-light C libraries. C17, **LGPL-3.0-only**, no
framework underneath them, and each one usable on its own.

They share a small set of conventions rather than a build system: every
library builds with `make`, tests with `make test`, installs with
`make install`, ships a pkg-config `.pc` file, and includes as
`ghoti.io/<library>/…`. Where one library needs another it finds it through
pkg-config and nothing else.

## Start here

**[`suite`](https://github.com/Ghoti-io/suite)** clones every library,
builds them in dependency order, and renders the combined manual.

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

Not every library is finished, and each repository's own README says where it
stands. `suite` builds whatever is checked out.

## License

Every library is LGPL-3.0-only. Each repository carries `COPYING` (GPL-3.0)
and `COPYING.LESSER` (LGPL-3.0), because LGPLv3 is written as a set of
additional permissions on top of GPLv3.

**Contributions are not being accepted at this time.** Each repository's
`CONTRIBUTING.md` says so, and the position is expected to change only
alongside a decision about licensing.
