# Pointers Lab: demo

A demo of an interactive C lab in Hebrew: the lesson on one side, and on the other an editor, a terminal, line-by-line stepping with a live view of the call stack, and hidden tests for every exercise.

**Open it:** https://nadavm-eng.github.io/pointers-lab-demo/

## What runs where

This demo runs a small example course (loops, a sum, input, a quiz and one lab exercise) entirely in your browser:

- The C code is compiled with [xcc](https://github.com/tyfkda/xcc) to 32-bit WebAssembly, so a pointer is 4 bytes here.
- In the sidebar you can switch ▶ Run and ✓ Tests to real gcc on [Compiler Explorer](https://godbolt.org) (64-bit). Line-by-line stepping stays in the browser.
- Your code is saved only in your own browser (localStorage).
- Turn on **מצב מנהל** (admin mode) to write lessons in the page: add, rename, duplicate, convert
  and delete lessons, drag them into a new order, and undo / redo (Ctrl+Z / Ctrl+Y). Changes
  update the page at once and are kept only in your own browser.

The full lab runs Run, Tests and line-by-line stepping on the student's own gcc (64-bit, the same compiler CLion uses) through a small local runner, with live keyboard input.

The whole site is one file, `index.html`, built from the lab's source.

## Licenses

The lab itself is public domain (see `LICENSE`). The page bundles xcc, tree-sitter and Preact
(MIT) and htm (Apache 2.0); their notices are in `THIRD_PARTY_NOTICES.md` and the full license
texts of Preact and htm in `licenses/`.
