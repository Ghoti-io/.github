# Ghoti.io (it's pronounced "[Fish](https://en.wikipedia.org/wiki/Ghoti)")

Dependency-light, cross-platform C libraries. C17, **LGPL-3.0-only**.

## Welcome

This is the org page for the Ghoti.io suite of libraries.  They are my own collection of libraries that exist simply because I wanted to build them.  They are primariliy for my own projects, but you can use them, too... they are LGPL-3.

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
| [`cutil`](https://github.com/Ghoti-io/cutil) | The foundation the rest of the suite is built on: an allocator, containers, checked arithmetic, threads and synchronisation, and the filesystem |
| [`security`](https://github.com/Ghoti-io/security) | Cryptographic primitives: hashes, MACs, key derivation, symmetric encryption, key agreement, signatures, password hashes, and the certificate encodings — DER, PEM, PKCS#8, PKCS#12, X.509, CRL and OCSP. No handshake lives here |
| [`unicode`](https://github.com/Ghoti-io/unicode) | The Unicode Character Database as generated tables, and the algorithms the Standard Annexes define over them: properties, normalisation, case mapping, segmentation, bidi and character names |
| [`chron`](https://github.com/Ghoti-io/chron) | Time: instants, civil dates, calendars, durations, time zones, and the text formats for all of them |
| [`compress`](https://github.com/Ghoti-io/compress) | Streaming compression: deflate, zlib and gzip, plus LZ4, LZW, RLE and zstd, with crc32 and xxhash |
| [`text`](https://github.com/Ghoti-io/text) | Structured text, each format with a document, a streaming parser and a writer: JSON (with Pointer, Path, Patch and Schema), CSV, YAML 1.2, TOML v1.0.0, and IDNA2008 and UTS #46 host names |
| [`color`](https://github.com/Ghoti-io/color) | A colour engine: colour-space description, ICC profiles, and transforms between spaces. Deliberately not a colour *management* system. **Scaffolding only so far** — the phases are planned, not built |
| [`image`](https://github.com/Ghoti-io/image) | Raster imaging as a multi-image document with metadata, colour information and operations: PNG and APNG, JPEG, BMP, GIF, and TIFF |
| [`model`](https://github.com/Ghoti-io/model) | 3D model formats over a byte stream: Wavefront OBJ geometry and MTL materials, and STL in both spellings |
| [`archive`](https://github.com/Ghoti-io/archive) | Archive containers, read and written **without touching the filesystem** — it hands you a member's name, size, time and bytes and never opens a file. Tar is read and written, zip is read, and `.tar.gz`, `.tar.zst` and `.tar.lz4` work both ways. No zip writer yet |
| [`regex`](https://github.com/Ghoti-io/regex) | Regular expressions over one parser and three engines. Ten of seventeen dialects compile and match — ECMAScript, PCRE2, Perl, POSIX and GNU BRE and ERE, Python, Vim and I-Regexp — and the other seven are named and report unsupported |
| [`ctang`](https://github.com/Ghoti-io/ctang) | Tang, a template language with an x86-64 JIT and a bytecode-VM fallback, which are required to agree |
| [`cjelly`](https://github.com/Ghoti-io/cjelly) | Vulkan-first cross-platform GUI toolkit: native windows, its own renderer, a render graph per window, and it draws Wavefront models |
| [`font`](https://github.com/Ghoti-io/font) | Fonts: sfnt and `ttcf` collections, `glyf` and CFF outlines with composites and CID-keyed fonts, cmap lookup and advances, rasterised to 8-bit coverage. Shaping, layout, variations and the bitmap formats are not built yet |

Not every library is finished, and each repository's own README says where it stands. `suite` builds whatever is checked out.

## Puns

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

## License

Every library is LGPL-3.0-only. Each repository carries `COPYING` (GPL-3.0) and `COPYING.LESSER` (LGPL-3.0), because LGPLv3 is written as a set of additional permissions on top of GPLv3.

**Contributions are not being accepted at this time.** That may change in the future.
