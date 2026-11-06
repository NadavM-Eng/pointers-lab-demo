# Pointers Lab: demo

A demo of an interactive C lab in Hebrew: the lesson on one side, and on the other an editor, a terminal, line-by-line stepping with a live view of the call stack, and hidden tests for every exercise.

**Open it:** https://nadavm-eng.github.io/pointers-lab-demo/

## What runs where

This demo runs a small example course (loops, a sum, input, a quiz and one lab exercise) entirely in your browser:

- The C code is compiled with [xcc](https://github.com/tyfkda/xcc) to 32-bit WebAssembly, so a pointer is 4 bytes here.
- In the sidebar you can switch ▶ Run and ✓ Tests to real gcc on [Compiler Explorer](https://godbolt.org) (64-bit). Line-by-line stepping stays in the browser.
- Your code is saved only in your own browser (localStorage).

The full lab runs Run, Tests and line-by-line stepping on the student's own gcc (64-bit, the same compiler CLion uses) through a small local runner, with live keyboard input.

The whole site is one file, `index.html`, built from the lab's source.

## Licenses

The lab itself is public domain (see `LICENSE`). The page bundles xcc and tree-sitter; their MIT licenses are in `THIRD_PARTY_NOTICES.md`.
