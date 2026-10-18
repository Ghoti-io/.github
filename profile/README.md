# Ghoti.io (it's pronounced "[Fish](https://en.wikipedia.org/wiki/Ghoti)")

Dependency-light, cross-platform C libraries. C17, **LGPL-3.0-only**.

## Welcome

This is the org page for the Ghoti.io suite of libraries.  They are my own collection of libraries that exist simply because I wanted to build them.  They are primarily for my own projects, but you can use them, too... they are LGPL-3.

## Start here

**[`suite`](https://github.com/Ghoti-io/suite)** clones every library, builds them in dependency order, and renders the combined manual.

### Very Quick Start

```bash
mkdir ghoti.io && cd ghoti.io
git clone https://github.com/Ghoti-io/suite.git
cd suite && ./clone.sh && ./install.sh && ./docs.sh
```

`./install.sh` and `./docs.sh` run in a container. Podman is used when it is installed, otherwise Docker, and one of the two is required. `./install.sh --no-container` and `./docs.sh --no-container` use the compiler and the documentation tools already on the host. The suite README names the packages a host build needs.

## The libraries

### Foundation

| Library | What it is |
| --- | --- |
| [`cutil`](https://github.com/Ghoti-io/cutil) | The foundation the rest of the suite is built on: an allocator, containers, checked arithmetic, threads and synchronisation, and the filesystem |
| [`math`](https://github.com/Ghoti-io/math) | Deterministic elementary functions that give the same bits on every host: sin, cos, tan, atan2, exp, log, pow and hypot on `double`, within 1 ulp and identical on every target |

### Text

| Library | What it is |
| --- | --- |
| [`regex`](https://github.com/Ghoti-io/regex) | Regular expressions over one parser and four engines. Twelve of eighteen dialects compile and match — ECMAScript, PCRE2, Perl, POSIX and GNU BRE and ERE, Python, Vim, I-Regexp, RE2 and Rust — and the other six are named and report unsupported |
| [`text`](https://github.com/Ghoti-io/text) | Structured text, each format with a document, a streaming parser and a writer: JSON (with Pointer, Path, Patch, Merge Patch and Schema), CSV, YAML 1.2.2, TOML v1.0.0, and INI |
| [`unicode`](https://github.com/Ghoti-io/unicode) | The Unicode Character Database as generated tables, and the algorithms the Standard Annexes define over them: properties, normalisation, case mapping, segmentation, bidi and character names |

### Time

| Library | What it is |
| --- | --- |
| [`chron`](https://github.com/Ghoti-io/chron) | Time: instants, civil dates, calendars, durations, time zones, and the text formats for all of them |

### Compression and archives

| Library | What it is |
| --- | --- |
| [`archive`](https://github.com/Ghoti-io/archive) | Archive containers, read and written **without touching the filesystem**. Tar is read in all four forms (v7, ustar, GNU and pax) and written as pax; zip is read and written (stored, deflate, bzip2, zstd and LZMA); 7z, ar and cpio are read and written, and shar is written. `.tar.gz`, `.tar.zst`, `.tar.lz4`, `.tar.lzma` and `.tar.bz2` work both ways |
| [`compress`](https://github.com/Ghoti-io/compress) | Streaming compression: deflate, zlib, gzip, Brotli, bzip2, xz, LZMA, LZ4, LZW, RLE and zstd, with CRC-32, Adler-32 and xxHash |

### Security

| Library | What it is |
| --- | --- |
| [`certificate`](https://github.com/Ghoti-io/certificate) | Certificates and keys: strict DER, PEM, PKCS#8, PKCS#12, X.509 with path validation and issuance, a certificate revocation list and a basic OCSP response, plus a trust store, path building and RFC 9525 names. The cryptography is security's |
| [`security`](https://github.com/Ghoti-io/security) | Cryptographic primitives: hashes, MACs, key derivation, symmetric encryption, key agreement, signatures, password hashes, and the kernel generator. Certificates and handshakes live in their own libraries |
| [`tls`](https://github.com/Ghoti-io/tls) | TLS 1.3 over buffers, for both roles, with no I/O and no clock: a record layer for a byte stream, or handshake messages by epoch for QUIC, plus session tickets, resumption and early data |

### Media

| Library | What it is |
| --- | --- |
| [`audio`](https://github.com/Ghoti-io/audio) | Sound as tracks with metadata: WAV, AIFF and FLAC read and written; MPEG audio read and MP3 written; Vorbis and Opus read and decoded |
| [`color`](https://github.com/Ghoti-io/color) | A colour engine: colour-space description, ICC profiles, and transforms between spaces, including CMYK and PQ/HLG. Deliberately not a colour *management* system |
| [`font`](https://github.com/Ghoti-io/font) | Fonts: sfnt and `ttcf` collections, `glyf`, CFF and CFF2 outlines, Type 1, WOFF and WOFF2, variable fonts, shaping and paragraph layout (inline objects, columns, ruby and emphasis marks), and the standalone bitmaps PCF, BDF, PSF and Unifont hex, rasterised to 8-bit coverage |
| [`image`](https://github.com/Ghoti-io/image) | Raster imaging as a multi-image document with metadata, colour information and operations: PNG and APNG, JPEG, BMP, GIF, ICO and CUR, WebP, and TIFF |
| [`model`](https://github.com/Ghoti-io/model) | 3D model formats over a byte stream: Wavefront OBJ geometry and MTL materials, STL in both spellings, and Geomview OFF |

### Shapes

A family of libraries for 2D vector graphics that gives the same bits on every host. They are scaffolds so far: a version call and the gates every library runs in `make test`.

| Library | What it is |
| --- | --- |
| [`shape-geometry`](https://github.com/Ghoti-io/shape-geometry) | Paths, transforms and flattening |
| [`shape-scene`](https://github.com/Ghoti-io/shape-scene) | The family's waist: resources and lists, and the versioned scene above them |
| [`shape-cpu`](https://github.com/Ghoti-io/shape-cpu) | The CPU rasterizer |

### Network

| Library | What it is |
| --- | --- |
| [`http`](https://github.com/Ghoti-io/http) | An HTTP/1.1, HTTP/2 and WebSocket codec — parsers, writers, HPACK, a connection state machine and permessage-deflate — bytes in and bytes out, with no sockets |

### Language and runtime

#### Tang (deprecated)

| Library | What it is |
| --- | --- |
| [`ctang`](https://github.com/Ghoti-io/ctang) | **Deprecated; use `lang-tang`.** Tang, a template language with an x86-64 JIT and a bytecode-VM fallback, which are required to agree |

#### The runtime

The parts any engine runs on.

| Library | What it is |
| --- | --- |
| [`runtime-core`](https://github.com/Ghoti-io/runtime-core) | The core of the language runtime: the execution context and the frame protocol that engines run on, and no engine of its own |
| [`runtime-heap`](https://github.com/Ghoti-io/runtime-heap) | The collector of the language runtime: a precise, non-moving mark-and-sweep heap that attaches to a runtime-core context |
| [`runtime-jit`](https://github.com/Ghoti-io/runtime-jit) | The baseline JIT of the language runtime: a low-level IR, an x86-64 backend and an arm64 backend, and stack maps and deoptimization records in runtime-core's format |
| [`runtime-debug`](https://github.com/Ghoti-io/runtime-debug) | The debugger of the language runtime: breakpoints, stepping and the state of a stop, and a Debug Adapter Protocol adapter over a transport the host binds |

#### Engines

Languages that run on the runtime.

| Library | What it is |
| --- | --- |
| [`lang-tang`](https://github.com/Ghoti-io/lang-tang) | The Tang engine of the language runtime, replacing ctang: templates and scripts, an interpreter, and a baseline JIT through runtime-jit |
| [`lang-wasm`](https://github.com/Ghoti-io/lang-wasm) | A WebAssembly 3.0 decoder, validator, translator, interpreter and baseline JIT, with a WAT and WAST parser. Still being filled in |

### Defiant

Defiant is a self-hosted application framework, written in C on the Ghoti.io suite. Web is one front end of several planned, and the only one that exists today. It is meant to keep working across upgrades, to lock no one in, and to be operable by AI. Early development; do not use.

#### Storage

| Library | What it is |
| --- | --- |
| [`defiant-storage`](https://github.com/Ghoti-io/defiant-storage) | A storage port for immutable revision documents, blobs, projection rows and outbox rows. A read sees the last commit; writes to one tenant are serializable |
| [`defiant-storage-memory`](https://github.com/Ghoti-io/defiant-storage-memory) | The in-memory backend for defiant-storage. Committed bytes stay in the process |
| [`defiant-storage-sqlite`](https://github.com/Ghoti-io/defiant-storage-sqlite) | The SQLite backend for defiant-storage: one database file per tenant, using vendor-sqlite |

#### Application

| Library | What it is |
| --- | --- |
| [`defiant-core`](https://github.com/Ghoti-io/defiant-core) | The Defiant kernel: a request context, a fiber scheduler, an offload pool and a yield watchdog, with the tenant carried on every request |
| [`defiant-web`](https://github.com/Ghoti-io/defiant-web) | The HTTP adapter for Defiant: one listener, HTTP/1.1 in, and a call to defiant-core for the tenant, the session and the page, with a server-rendered admin |
| [`defiant-test`](https://github.com/Ghoti-io/defiant-test) | The milestone harness for Defiant: tenant export and import, and the six gates that close milestone 1 — cross-tenant isolation, an access-filter bypass, erasure that survives restore, a memory-to-SQLite round trip, an unsafe-list lint and a scan for internal ids in rendered pages |

### Vendored

Third-party code, kept as its own repository and built like the rest. It was not written by this project.

| Library | What it is |
| --- | --- |
| [`vendor-sqlite`](https://github.com/Ghoti-io/vendor-sqlite) | SQLite 3.53.4, the official amalgamation, so more than one library can link the same pin. The public API is `sqlite3_*`, with no wrapper |

### Experimental

**Proof of concept. Do not use it for anything yet.**

| Library | What it is |
| --- | --- |
| [`cjelly`](https://github.com/Ghoti-io/cjelly) | A Vulkan-first GUI: native windows, its own renderer, and a render graph per window. The demo runs on Linux, with X11 and Vulkan, and draws panels, an image and a Wavefront model |

Not every library is finished, and each repository's own README says where it stands. The shape libraries are scaffolds, and `lang-wasm` is partly done. `vendor-sqlite` is the SQLite amalgamation, not a library written here, and it keeps SQLite's public-domain header. `suite` builds whatever is checked out.

## Puns

- "Ghoti" is pronounced "[Fish](https://en.wikipedia.org/wiki/Ghoti)".
  - I thought it was funny.
  - It takes the basics of English phonetics and uses them for its own purposes.  This project is written in C... you can definitely do unexpected things!
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
  - **CJelly** A GUI library (the demo runs on Linux, with X11 and Vulkan)
    - A GUI ("gooey") Ghoti ("fish") in the .io ("Indian Ocean").  It's obviously a jellyfish.
    - `cjelly`... "[sea jelly](https://en.wikipedia.org/wiki/Jellyfish)"
    - I think I'm hilarious.

## License

Every library written here is LGPL-3.0-only. Each of those repositories carries `COPYING` (GPL-3.0) and `COPYING.LESSER` (LGPL-3.0), because LGPLv3 is written as a set of additional permissions on top of GPLv3. `vendor-sqlite` keeps SQLite's public-domain header.

**Contributions are not being accepted at this time.** That may change in the future.
