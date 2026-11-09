# Third-party software

The project's own code is under the PolyForm Noncommercial License 1.0.0 (see `LICENSE`). It ships with, or downloads, the
following software, which keeps its own license.

## xcc (in-browser C compiler) — MIT License

`lab.html` embeds the compiler and C library from [xcc](https://github.com/tyfkda/xcc), compiled to WebAssembly.

```
MIT License

Copyright (c) 2024 tyfkda

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```


## tree-sitter and tree-sitter-c (error-tolerant C parser) — MIT License

`lab.html` embeds [web-tree-sitter](https://github.com/tree-sitter/tree-sitter) 0.24.7 and the
[tree-sitter-c](https://github.com/tree-sitter/tree-sitter-c) 0.23.6 grammar, compiled to WebAssembly
(`src/engines/c/vendor/tree-sitter/`). They are used to step through code that does not compile.

```
The MIT License (MIT)

Copyright (c) 2018-2024 Max Brunsfeld (web-tree-sitter)
Copyright (c) 2014 Max Brunsfeld (tree-sitter-c)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## React and React DOM (and scheduler) — MIT License

Since option C stage 2, `lab.html` embeds [React](https://react.dev) 19.3.1, React DOM 19.3.1 and its
scheduler 0.28.0 (npm packages `react`, `react-dom`, `scheduler`; production builds, not minified).

```
MIT License

Copyright (c) Meta Platforms, Inc. and affiliates.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```


## GCC, GNU Binutils, GNU Make, MinGW-w64 (the `gcc\` folder in the release zip)

The release zip contains a reduced copy of the WinLibs build
`winlibs-x86_64-posix-seh-gcc-16.2.0-mingw-w64ucrt-14.0.0-r3` from
<https://winlibs.com/> (SHA-256 `3c69305081e4a647144339a936244fcf7d3d9e558319e1ad7be2cd2886d4b6a1`).
Files are copied unmodified; `scripts/trim-gcc.sh` lists exactly which ones.

- **GCC**: GNU General Public License v3 with the GCC Runtime Library Exception
  (programs you compile with it are not affected by the GPL).
- **GNU Binutils** and **GNU Make**: GNU General Public License v3.
- **MinGW-w64** runtime and headers: mostly public domain and permissive licenses (ZPL, MIT, BSD).
- **GMP, MPFR, MPC, ISL, zlib, zstd, libiconv, gettext**: their own free licenses (LGPL, MIT/BSD-style, zlib).

Source code for all of these is available from the projects themselves and from the WinLibs
release page:
<https://github.com/brechtsanders/winlibs_mingw/releases/tag/16.2.0posix-23.1.3-14.0.0-ucrt-r3>

## ProseMirror (the rich-text editor of admin mode) — MIT License

`lab.html` embeds [ProseMirror](https://prosemirror.net) (minified), the editor of the lesson
texts in admin mode (docs/VITE.md section 9): the packages below, all by Marijn Haverbeke and
others, under the same MIT license text (only the year in the copyright line differs).

- prosemirror-model 1.25.12: Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- prosemirror-state 1.4.4: Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- prosemirror-view 1.42.7: Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- prosemirror-transform 1.12.4: Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- prosemirror-keymap 1.2.3: Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- prosemirror-commands 1.7.2: Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- orderedmap 2.1.1: Copyright (C) 2016 by Marijn Haverbeke <marijn@haverbeke.berlin> and others
- w3c-keyname 2.2.8: Copyright (C) 2016 by Marijn Haverbeke <marijn@haverbeke.berlin> and others

```
Copyright (C) 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

## Temml (LaTeX to MathML, the networking and math courses) — MIT License

The pages that show LaTeX formulas embed [Temml](https://temml.org) 0.14.0 by Ron Kok
(minified), which turns LaTeX into native MathML, through `src/shared/tex.ts`: the networking
course (`src/engines/net`) and the courses on the proof engine (`src/engines/proof`, the math
courses). The browser lays the MathML out with its own math font: none of Temml's fonts are
used. `src/engines/proof/engine.css` holds a few layout rules from Temml's `Temml-Local.css`.

```
The MIT License (MIT)

Copyright (c) 2020 Ron Kok

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## TeaVM in-browser Java compiler (teavm-javac) — Apache License 2.0; contains OpenJDK javac — GPL v2 with the Classpath Exception

The pages of the courses on the Java engine (`src/engines/java`) embed the in-browser Java
compiler of [teavm-javac](https://github.com/konsoletyper/teavm-javac): javac and TeaVM compiled
to WebAssembly, TeaVM's class libraries, its runtime JavaScript and its stack deobfuscator. They
were downloaded unchanged from <https://teavm.org/playground/3/> on 2026-11-08 and are kept in
`src/engines/java/vendor/teavm/` (three of them gzip-compressed; the page inlines them and
unpacks them with the browser's `DecompressionStream`). The page is about 5.7 MB larger for it:
the five files it inlines are 4.25 MB, and base64 makes them a third bigger.

| file (downloaded) | bytes | SHA-256 |
|---|---|---|
| `compiler.wasm` | 4,294,850 | `7f3828e4b7bddf5504dadebfc4016e40f4441e15ee0519071781813ba2ed3a4c` |
| `compiler.wasm-runtime.js` | 13,573 | `9ff6a6771f698be00ab9d5c7b46d904350a8d4115dc0b409553f31ed66688a55` |
| `compiler.wasm-deobfuscator.wasm` | 36,544 | `af49c0a76f47a30be2b23a74ffed502717b72019d871566841e66e754e5865e0` |
| `compile-classlib-teavm.bin` | 200,623 | `e80ae10423a39290c5f20b6bb6da34d21c3ad0a75cd8dbdda4998d2813045e15` |
| `runtime-classlib-teavm.bin` | 2,387,011 | `ea670e71967eda93828cb894c1741a8ed2e94b3422eb99cb9eccec0de67daaa8` |

- **TeaVM and teavm-javac:** Copyright 2013-2026 Alexey Andreev, Apache License 2.0 (the full
  text is `src/engines/java/vendor/teavm/LICENSE-Apache-2.0.txt`).
- **javac inside `compiler.wasm`:** from the OpenJDK project, GNU General Public License version 2
  with the Classpath Exception (the GPL text is `src/engines/java/vendor/teavm/LICENSE-GPL-2.0.txt`,
  the exception `LICENSE-CLASSPATH-EXCEPTION.txt` beside it; also
  <https://openjdk.org/legal/gplv2+ce.html>). teavm-javac states that it does not modify OpenJDK.
  Source: teavm-javac builds javac from the OpenJDK 25 updates repository at commit
  `6c48f4ed707bf0b15f9b6098de30db8aae6fa40f`
  (<https://github.com/openjdk/jdk25u/tree/6c48f4ed707bf0b15f9b6098de30db8aae6fa40f>; the bundled
  javac knows Java releases up to 25); the build itself is <https://github.com/konsoletyper/teavm-javac>
  (the playground build names no commit; every commit from `9dd58592`, 2025-10-04, uses that
  OpenJDK commit).
- **On a site:** a site (`npm run site`) with a Java course carries the GPL v2, the Classpath
  Exception, the Apache 2.0 licence and `NOTICE.txt` next to its pages, and `java-compiler.html`
  (the files above with their SHA-256 and the links to their source), linked from the hub's footer
  (`src/engines/java/site.json`, docs/engines/java.md section 8).
- When the compiler loads, the lab renames some methods and classes of the compile class library
  in memory (TeaVM's own rename annotations, as later teavm-javac sources do); the files stay
  unchanged.

Not downloaded: tree-sitter-java (approved in the plan). The Java instrumenter needs only
statement-level parsing, which the engine does itself (`src/engines/java/stepping/lexer.ts`,
`structure.ts`), so no grammar is shipped.
