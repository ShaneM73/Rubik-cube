# Rubik-cube

An interactive 3D Rubik's cube that shows the linear algebra and the group theory behind it, with a step-by-step solving guide. It is a single web page: open `index.html` in a browser.

The linear-algebra model follows Steffen's video [The Rubik's cube is secretly linear algebra](https://www.youtube.com/watch?v=kRrK4VJBf2s): every cubelet is a vector, every colour is a basis vector, and a move is a dot product followed by a matrix product.

## What is in it

| Tab | What it shows |
|---|---|
| Linear algebra | Each cubelet as a pair `(c, R)`: home vector and rotation matrix. Live values of `p = R·c` and `R·diag(c)`, layer selection with `v·p > 0`, the update `R ← M·R`, and the solved test `R·diag(c) = diag(c)` read as an eigenvector condition. |
| Group theory | Move words and their inverses, the order of any word, the twist, flip and parity invariants, and buttons that mis-assemble the cube to leave the group. |
| Questions | Why each `R` cannot be factored separately, whether the model is a solver, and whether a shortest solution is unique. |
| Solve | A seven-stage layer-by-layer guide that reads the current state, shows the next step with its moves, and explains why each sequence works. Arrows on the cube point each piece to its destination. |

Other controls: face-turn buttons and keyboard (`U D L R F B`, Shift for the reverse turn), scramble, reset, an explode slider, and an X-ray view of a cartoon of the internal mechanism.

## Conventions

- Axes: `x` front/back, `y` right/left, `z` top/bottom.
- Colours: green `+x`, blue `−x`, red `+y`, orange `−y`, white `+z`, yellow `−z`.
- A letter is a clockwise quarter turn seen from outside that face; `'` reverses it; `2` is a half turn.

## Notes

- The page loads three.js (r128) from cdnjs and two fonts from Google Fonts, so it needs an internet connection.
- The Solve guide aims for clarity, not short solutions: about 140 turns for a full scramble. It was checked on 1,500 random scrambles.
- The mechanism in the X-ray view is a simplified cartoon.
