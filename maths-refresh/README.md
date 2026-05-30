# Maths Refresh

Bite-sized maths refresh notebooks for the Imperial AI course preparation.

The aim is to rebuild useful intuition before the course starts, especially where mathematical ideas connect directly to machine learning, NumPy, visual reasoning, and the early mechanics of model fitting.

This folder is intended to be a guided learning path rather than a loose collection of notes. Each notebook should have a clear job, build on the previous material, and avoid turning into a reference chapter.

## Stable learning path

The reviewed foundation currently runs from `01` through `07`.

| Notebook | Topic | Purpose |
|---|---|---|
| `01-vectors-shapes-norms.ipynb` | Vectors, shapes and norms | How vectors are represented in NumPy, why shape matters, and how vector length works. |
| `02-dot-products-cosine-similarity.ipynb` | Dot products and cosine similarity | Dot products as alignment, magnitude, and similarity. |
| `03-projections-and-components.ipynb` | Projections and components | Breaking one vector into parallel and perpendicular parts relative to another vector. |
| `04-matrices-as-transformations.ipynb` | Matrix transformation overview | Parent notebook for the 2D matrix transformation sequence. |
| `04a-matrix-vector-multiplication.ipynb` | Matrix-vector multiplication | How a matrix maps an input vector to an output vector, using the transformed-basis-vector view. |
| `04b-how-2x2-matrix-elements-work.ipynb` | 2x2 matrix elements | What each element of a 2x2 matrix contributes to a transformation. |
| `04c-scaling-reflection-and-shear.ipynb` | Scaling, reflection and shear | Common transformation types and their visual effects. |
| `04d-rotation-transformations.ipynb` | Rotation transformations | Rotation matrices, rotated basis vectors, and movement around the origin. |
| `05-transforming-shapes-with-matrices.ipynb` | Transforming shapes | Applying matrices to sets of points rather than individual vectors. |
| `06-intro-to-least-squares.ipynb` | Least squares introduction | Fitting a simple line, residuals, squared error, and the first matrix view of least squares. |
| `07-least-squares-as-projection.ipynb` | Least squares as projection | Least squares as projecting a target vector onto the reachable prediction space. |

## Section notes

### Vectors and projections

The first three notebooks build the basic vector intuition needed later:

- vectors as NumPy arrays with shapes
- vector length as a measurable quantity
- dot products as alignment
- projection as splitting a vector into a parallel part and a leftover perpendicular part

This prepares the ground for understanding least squares geometrically.

### Matrices as transformations

The `04` sequence is a small sub-section.

The central mental model is:

> A matrix moves the basis vectors, and every other vector follows because it is built from those basis vectors.

The parent notebook, `04-matrices-as-transformations.ipynb`, introduces the route through the matrix-transformation material. The child notebooks then build from mechanics to named transformations:

1. multiply a matrix by a vector
2. read a 2x2 matrix by its columns
3. vary matrix elements and observe the effect
4. recognise scaling, reflection, shear, and rotation
5. apply those transformations to whole shapes

The former standalone basis-vector / matrix-column recap has been absorbed into the active `04` sequence rather than kept as a separate notebook.

### Least squares

Notebooks `06` and `07` form the first model-fitting bridge.

`06-intro-to-least-squares.ipynb` introduces least squares through the visible line-fitting problem:

- choose a candidate line
- calculate residuals
- square the residuals
- minimise total squared error
- introduce the design-matrix view

`07-least-squares-as-projection.ipynb` then explains the geometry underneath:

- the columns of a matrix define the reachable prediction space
- the best prediction vector is the closest reachable vector
- the residual is perpendicular to that reachable space
- the normal equations are the algebraic version of that perpendicular-residual condition

Together, `06` and `07` connect line fitting, vectors, matrices, projections, and the earliest intuition needed for machine learning models.

## Later notebooks

Files numbered `08` and above may exist in this folder as placeholders or work-in-progress material.

They should be treated as the next part of the learning path, not as part of the reviewed foundation yet. Once `01` through `07` are stable, the later notebooks can be reviewed and reshaped in sequence.

## Interactive tools

The `interactive/` folder contains small browser-based companions for the notebooks.

Current tool:

- `interactive/matrix-transformer.html` — a standalone 2D matrix transformation playground.

These tools are not replacements for the notebooks. They are there to make the visual ideas easier to experiment with.

## Exports

The `exports/` folder may contain rendered versions of notebooks, such as HTML or PDF outputs.

Exports are useful for review and sharing, but the notebook files remain the source material.

## Style

Each notebook should stay focused and reasonably small.

When a topic starts to sprawl, prefer one of these options:

- trim repeated explanation
- move detail into a follow-on notebook
- create a parent notebook to frame a small sequence
- archive older drafts that no longer belong in the main path

The goal is a clean, intentional learning sequence: clear enough for learning, compact enough for revision, and polished enough for a public GitHub repo.
