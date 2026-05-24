# Maths Helper Rules

Use this brief when asking an LLM to help generate or edit my maths / ML preparation notebooks.

## Context

I am preparing for an ML / AI course and creating educational Jupyter notebooks in a GitHub repo.

The notebooks should be clear, teaching-focused, and bite-sized. They should build intuition gradually without turning into sprawling reference documents.

## Markdown and maths formatting

Use JupyterLab-safe markdown.

For display maths, prefer dollar-delimited display blocks:

```markdown
$$
...
$$
```

Do **not** use this style for display maths unless specifically asked:

```markdown
\[
...
\]
```

My JupyterLab / Brave setup has rendered `\[ ... \]` unreliably, with raw LaTeX leaking into the rendered notebook.

For inline maths, use single-dollar inline maths:

```markdown
$...$
```

For example:

```markdown
$$
\mathbf{v} = x\mathbf{e}_1 + y\mathbf{e}_2
$$
```

and inline:

```markdown
$\mathbf{e}_1$ points along the x-axis.
```

Avoid markdown / maths combinations that are likely to render badly in notebooks, such as raw `\[ ... \]` blocks or square-bracket vector notation that could be mistaken for markdown links.

Prefer column-vector notation where useful:

```markdown
$$
\mathbf{v} =
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$
```

## Plotting preferences

Use plots to teach the concept, not just to show a mathematically correct picture.

Prefer compact plots with minimal wasted space. Do not default to large symmetric axes if the action is mostly in one quadrant.

Set explicit axis limits when that makes the plot clearer.

For example, for a vector from $(0,0)$ to $(2,1)$, prefer something like:

```python
ax.set_xlim(-0.25, 2.45)
ax.set_ylim(-0.25, 1.45)
```

rather than showing a large unused bottom-left quadrant.

Use smaller figure sizes for simple ideas, for example:

```python
fig, ax = plt.subplots(figsize=(4.5, 4.5))
```

or:

```python
fig, ax = plt.subplots(figsize=(5, 4))
```

Use larger plots only when the concept genuinely needs the space.

## Visual teaching style

Avoid cluttered “arrow soup”.

When comparing a vector before and after a matrix transformation, prefer two clear plots:

1. before: vector built from the standard basis
2. after: transformed vector built from the transformed basis vectors

For example:

```markdown
$$
\mathbf{v} = 2\mathbf{e}_1 + 1\mathbf{e}_2
$$

$$
A\mathbf{v} = 2(A\mathbf{e}_1) + 1(A\mathbf{e}_2)
$$
```

The key teaching point is:

> The matrix changes the basis vectors. The vector follows because it is built from those basis vectors.

Use before / after plots when they reduce clutter and make the idea easier to see.

## Label preferences

Use clean mathematical labels where possible:

```python
"e₁"
"e₂"
"2e₁"
"1e₂"
"v"
```

If Unicode subscripts render badly, fall back to Matplotlib maths labels:

```python
"$e_1$"
"$e_2$"
"$2e_1$"
"$1e_2$"
"$v$"
```

Manually nudge labels where needed to avoid collisions, especially near vector tips.

## Prose and tone

Keep the prose direct and explanatory.

I like intuitive phrases such as “a vector as a recipe” or “coordinates as instructions”, but tie the metaphor back to the maths.

Useful phrasing:

> Its coordinates tell us how to build it from the standard basis vectors.

and:

> The vector is not just an arrow. It is also a set of instructions.

Do not overcomplicate the notebook. Make the concept land cleanly, then move on.

## Notebook structure

Prefer a gentle sequence:

1. introduce the idea in plain English
2. show the maths notation
3. demonstrate with a small Python example
4. visualise the result
5. summarise the intuition

Avoid making one notebook cover too many concepts. If the topic grows, split it into smaller notebooks and use a parent notebook or README-style overview to link them together.
