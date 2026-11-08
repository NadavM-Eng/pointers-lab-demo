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
(`src/vendor/tree-sitter/`). They are used to step through code that does not compile.

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
