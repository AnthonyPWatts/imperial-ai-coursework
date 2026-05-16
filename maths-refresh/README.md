# Maths Refresh

Bite-sized maths refresh notebooks for the Imperial AI course preparation.

The aim is to rebuild useful intuition before the course starts, especially where mathematical ideas connect directly to machine learning, NumPy and visual reasoning.

## Current sequence

| Notebook | Topic | Purpose |
|---|---|---|
| `01-vectors-shapes-norms.ipynb` | Vectors, shapes and norms | How vectors are represented in NumPy, why shape matters, and how vector length works. |
| `02-dot-products-cosine-similarity.ipynb` | Dot products and cosine similarity | Dot products as alignment, magnitude and similarity. |
| `03-projections-and-components.ipynb` | Projections and components | Breaking one vector into parts relative to another vector. |
| `04-matrices-as-transformations.ipynb` | Matrix transformation overview | Parent notebook for the 2D matrix transformation sequence. |
| `04a-matrix-vector-multiplication.ipynb` | Matrix-vector multiplication | How a matrix maps an input vector to an output vector. |
| `04b-how-2x2-matrix-elements-work.ipynb` | 2x2 matrix elements | What each element of a 2x2 matrix contributes to a transformation. |
| `04c-scaling-reflection-and-shear.ipynb` | Scaling, reflection and shear | Common transformation types and their visual effects. |
| `04d-rotation-transformations.ipynb` | Rotation transformations | Rotation matrices and how they move points around the origin. |
| `04e-basis-vectors-and-matrix-columns.ipynb` | Basis vectors and matrix columns | Matrix columns as the transformed basis vectors. |
| `05-transforming-shapes-with-matrices.ipynb` | Transforming shapes | Applying matrices to sets of points rather than individual vectors. |
| `06-intro-to-least-squares.ipynb` | Least squares introduction | First steps towards fitting, residuals and optimisation intuition. |

## Interactive tools

The `interactive/` folder contains small browser-based companions for the notebooks.

Current tool:

- `interactive/matrix-transformer.html` — a standalone 2D matrix transformation playground.

These tools are not replacements for the notebooks. They are there to make the visual ideas easier to experiment with.

## Style

Each notebook should stay focused and reasonably small. When a topic starts to sprawl, split it into a follow-on notebook rather than turning one file into a textbook chapter.
