# Pointers Lab: demo

A demo of an interactive programming lab in Hebrew: the lesson on one side, and on the other an
editor, a terminal, line-by-line stepping with a live view of the call stack, and hidden tests for
every exercise.

**Open it:** https://nadavm-eng.github.io/pointers-lab-demo/

## What is here

The start page lists the courses of this demo. Each course is its own offline page:

| File | What it is |
|---|---|
| `index.html` | The course list, with your progress in each course |
| `math-sequences.html` | A proof of concept for math: proofs about bounded sequences (a Calculus 1 question), stepped line by line like code. A panel shows the bounds known so far (M₁, m₁, K₁, …) the way the C courses show the call stack |
| `example-net.html` | A networking example course: packet timing stepped event by event, with a live timeline, a panel of values with units, and answers checked with units |
| `example-c.html` | A small C course: loops, a sum, input, arrays and 2D arrays with pointers into them, a quiz and one lab exercise |
| `example.html` | A tiny course in an example language, which shows how the lab supports more than one language |

## What runs where

Everything runs in your browser:

- The C code is compiled with [xcc](https://github.com/tyfkda/xcc) to 32-bit WebAssembly, so a
  pointer is 4 bytes here.
- In the sidebar you can switch ▶ Run and ✓ Tests to real gcc on
  [Compiler Explorer](https://godbolt.org) (64-bit). Line-by-line stepping stays in the browser.
- Line by line also steps into functions in your other `.c` files, and you can edit the code while
  stepping. Press ⏯ again to run the new code.
- Your code and progress are saved only in your own browser (localStorage).
- **סיור מודרך** (guided tour) at the bottom of the sidebar shows how everything works. It starts
  by itself on your first visit.
- Turn on **מצב מנהל** (admin mode) to write lessons in the page:
  - rich text and the block tools;
  - add, rename, duplicate, convert and delete lessons;
  - drag lessons into a new order;
  - undo / redo (Ctrl+Z / Ctrl+Y).

  Changes are kept only in your own browser.

The full lab runs Run, Tests and line-by-line stepping on the student's own gcc (64-bit, the same
compiler CLion uses) through a small local runner, with live keyboard input.

The pages are built from the lab's Vite + React version (`npm run site -- public`). The version
each page was built from is shown at the bottom of its sidebar.

## Licenses

The lab itself is under the PolyForm Noncommercial License 1.0.0 (see `LICENSE`): free for
noncommercial use; commercial use is not allowed. The pages bundle xcc and tree-sitter, React and
ProseMirror (all MIT). Their notices and full license texts are in `THIRD_PARTY_NOTICES.md`.
