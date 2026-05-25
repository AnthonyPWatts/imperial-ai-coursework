# Maths Helper Rules

Use this brief when asking an LLM to help generate, review, or edit my maths / ML preparation notebooks.

## Context

I am preparing for an ML / AI course and creating educational Jupyter notebooks in a GitHub repo.

The notebooks should be clear, teaching-focused, and bite-sized. They should build intuition gradually without turning into sprawling reference documents.

The best notebooks should feel like guided learning notes: a little prose, a little maths, a small amount of code, a carefully chosen plot, and then a concise statement of the intuition.

The goal is not only to improve individual notebooks. The goal is to improve the learning path.

## Core style principles

- Teach the concept, not just the mechanics.
- Prefer one clear idea per section.
- Keep explanations direct, plain-English, and grounded in the maths.
- Mention important mathematical edge cases briefly when they prevent misleading intuition, but avoid turning the notebook into a reference manual.
- Avoid turning a notebook into a reference manual.
- Avoid unnecessary repetition once a stronger later section makes an earlier section redundant.
- Use code and plots to support the explanation, not to show off.
- Make the concept land cleanly, then move on.
- Review notebooks as part of a sequence, not only as isolated documents.

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

Avoid `\( ... \)` for inline maths unless there is a specific reason to use it. Prefer `$...$` for consistency.

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

For short inline references, bracket notation is fine if it renders clearly:

```markdown
The vector $[2, 1]$ can be read as $2\mathbf{e}_1 + 1\mathbf{e}_2$.
```

## Avoid display maths inside bullet points

Display maths inside bullet points often renders with awkward spacing in JupyterLab.

Avoid this:

```markdown
- The standard basis vectors are

$$
\mathbf{e}_1 = [1, 0]
$$
```

Prefer either inline maths inside bullets:

```markdown
- The first column is where $\mathbf{e}_1$ lands.
- The second column is where $\mathbf{e}_2$ lands.
```

or use short prose followed by a separate display block:

```markdown
The standard basis vectors are:

$$
\mathbf{e}_1 =
\begin{bmatrix}
1 \\
0
\end{bmatrix}
\qquad
\mathbf{e}_2 =
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$
```

Use display maths for important equations, not as decoration for every small symbol.

## Notebook structure

Prefer a gentle sequence:

1. introduce the idea in plain English
2. show the maths notation
3. demonstrate with a small Python example
4. visualise the result
5. summarise the intuition

A strong section usually has this shape:

```markdown
## Concept name

A short explanation of the idea.

$$
\text{one useful equation or definition}
$$
```

```python
# Small numerical example
```

```python
# One clear plot, if a plot helps
```

```markdown
A short statement of what the example showed.
```

Avoid making one notebook cover too many concepts. If the topic grows, split it into smaller notebooks and use a parent notebook or README-style overview to link them together.

## Section-level review and pruning

When reviewing a notebook, check whether it still has a unique job in the wider sequence.

A notebook may be technically good but no longer necessary if later revisions have moved its core teaching idea into earlier notebooks.

Ask:

- What does this notebook teach that no other notebook teaches?
- Does it move the learner forward?
- Is it introducing a new idea, consolidating a previous idea, or duplicating material?
- Would the learning path be clearer if this became part of a parent notebook or summary instead?
- Is this notebook part of the main learning path, or should it be retired, archived, or merged?

Do not preserve a notebook merely because it is good. If its purpose has been absorbed elsewhere, consider retiring it.

Possible review outcomes are:

- keep as-is
- lightly polish
- structurally remake
- merge into another notebook
- move into a parent/summary notebook
- archive/delete from the main learning path

For public-facing learning material, a cleaner sequence is usually better than keeping every useful draft.

## Parent notebooks and section summaries

For a multi-notebook section, the parent notebook should do more than list links.

It should briefly explain:

- the purpose of the section
- the prerequisites
- the recommended order
- the central mental model
- what each child notebook contributes
- the section-level summary
- what comes next

If a recap notebook only repeats the central idea of the section, consider folding that recap into the parent notebook instead.

A good parent notebook is a landing page, route map, and concise section summary. It should not become a full teaching notebook that duplicates the child notebooks.

## Distribute central ideas across the teaching path

If an idea is central to a whole section, do not leave it isolated in a late recap notebook.

Introduce it early, then reuse it consistently in later notebooks.

A final summary can reinforce the idea, but the learner should already have been using it throughout the section.

For example, in a matrix-transformation sequence, the basis-vector / column-view idea should appear throughout the sequence, not only in a final recap notebook.

## Main path versus archive

Keep the main learning path clean and intentional.

If an old notebook still has useful material but no longer belongs in the main sequence, either:

- salvage its best ideas into the active notebooks, or
- move it to an archive area

Avoid leaving deprecated notebooks in the main sequence where they may confuse the learning order.

## Replacement notebook workflow

When generating a replacement notebook, it is fine to use a temporary filename such as:

```text
04c-scaling-reflection-and-shear-replacement.ipynb
```

But once accepted, the replacement should normally take the canonical filename in the repo.

Avoid leaving both old and replacement versions side by side in the final learning path unless there is a clear reason.

If an executed notebook is useful for review, generate both:

```text
notebook-name-replacement.ipynb
notebook-name-replacement-executed.ipynb
```

The canonical repo version should normally be the clean accepted notebook, not a growing collection of draft replacements.

## Conceptual reframes and metaphors

Conceptual reframes, analogies, and alternate mental models usually work best after the concrete mechanics have landed.

For example, in a projection notebook, first show:

1. scalar projection
2. vector projection
3. parallel component
4. perpendicular component

Then introduce a reframe such as “imagine the target vector as a temporary axis”.

This lets the reframe consolidate understanding rather than interrupt the initial learning path.

## Flow and redundancy

Review the notebook as a learning journey, not just as isolated cells.

If an early plot or explanation is later replaced by a better before/after comparison, consider removing the earlier version rather than keeping both.

Avoid orphaned cells: every plot should either introduce a new idea, prepare for the next idea, or provide the payoff for a concept just explained.

For comparison sections, it is often better to build up the idea with code first, then use the paired plot as the visual payoff.

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
fig, ax = plt.subplots(figsize=(4, 4))
```

or:

```python
fig, ax = plt.subplots(figsize=(5, 4))
```

Use larger plots only when the concept genuinely needs the space.

## Comparison plots

For comparison-style plots, especially before/after plots, use shared axis limits wherever practical.

This is more important than cropping each plot individually as tightly as possible.

Shared limits make the comparison visually honest and easier to read. For example:

```python
fig, axes = plt.subplots(1, 2, figsize=(10, 4))

shared_xlim = (-1.1, 3.35)
shared_ylim = (-0.25, 2.75)

for ax in axes:
    ax.set_xlim(*shared_xlim)
    ax.set_ylim(*shared_ylim)
```

Use separate limits only if shared limits make one side genuinely unreadable or misleading.

## Plot helper design

It is fine to start with a simple helper such as:

```python
def setup_axis(ax, title, limit=4):
    ax.axhline(0, linewidth=1)
    ax.axvline(0, linewidth=1)
    ax.set_xlim(-limit, limit)
    ax.set_ylim(-limit, limit)
    ax.set_aspect("equal", adjustable="box")
    ax.grid(True, alpha=0.3)
    ax.set_title(title)
    ax.set_xlabel("x")
    ax.set_ylabel("y")
```

But if most plots immediately override the limits, prefer evolving the helper to accept explicit limits:

```python
def setup_axis(ax, title, xlim=(-4, 4), ylim=(-4, 4)):
    ax.axhline(0, linewidth=1)
    ax.axvline(0, linewidth=1)
    ax.set_xlim(*xlim)
    ax.set_ylim(*ylim)
    ax.set_aspect("equal", adjustable="box")
    ax.grid(True, alpha=0.3)
    ax.set_title(title)
    ax.set_xlabel("x")
    ax.set_ylabel("y")
```

Then call it like this:

```python
setup_axis(
    ax,
    "After: transformed basis vectors",
    xlim=(-1.1, 3.35),
    ylim=(-0.25, 2.75)
)
```

Keep helpers simple. Do not hide important teaching choices inside overly clever plotting utilities.

## Visual teaching style

Avoid cluttered “arrow soup”.

When comparing a vector before and after a matrix transformation, prefer two clear plots:

1. before: the vector built from the standard basis vectors
2. after: the transformed vector built from the transformed basis vectors

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

> The coefficients stay the same. The basis vectors have moved.

or:

> The matrix changes the basis vectors. The vector follows because it is built from those basis vectors.

Use before / after plots when they reduce clutter and make the idea easier to see.

For named transformations, show the transformed basis vectors as the main visual object:

- scaling changes basis-vector lengths
- reflection flips one basis direction
- shear slants one basis direction into the other
- rotation turns both basis vectors while preserving length and right angles

## Titles and labels in plots

Keep plot titles plain and descriptive. Do not overuse metaphors in titles.

Good examples:

```python
"Before: standard basis vectors"
"After: transformed basis vectors"
"The standard basis vectors"
"The transformed basis vectors"
"Rotation by 45 degrees"
"Horizontal shear"
```

Less ideal if overused:

```python
"Before: standard basis recipe"
"After: transformed basis recipe"
```

The “recipe” metaphor can be useful in prose, but plot titles should usually remain clean and mathematical.

Use clean mathematical labels where possible:

```python
"e₁"
"e₂"
"2e₁"
"1e₂"
"v"
"Ae₁"
"Ae₂"
"2Ae₁"
"1Ae₂"
"Av"
"Re₁"
"Re₂"
"Rv"
```

Avoid overly code-like labels inside plots:

```python
"A @ e1"
"2(A @ e1)"
"A @ v"
"R @ v"
```

Those are fine in code cells or printed output, but they are usually too busy for plot labels.

If Unicode subscripts render badly, fall back to Matplotlib maths labels:

```python
"$e_1$"
"$e_2$"
"$2e_1$"
"$1e_2$"
"$v$"
"$Ae_1$"
"$Ae_2$"
"$Av$"
"$Re_1$"
"$Re_2$"
"$Rv$"
```

Manually nudge labels where needed to avoid collisions, especially near vector tips.

It is acceptable to draw an arrow without using the helper label, then place the label manually with `ax.text(...)`.

## Vector construction plots

For simple vector construction, a helper such as `draw_chain(...)` may be fine. But for polished teaching plots, manual placement is often clearer.

Prefer this kind of approach when labels are awkward:

```python
# Draw the first component.
ax.arrow(
    0, 0,
    2, 0,
    length_includes_head=True,
    head_width=0.08,
    head_length=0.12,
    linewidth=2
)

ax.text(
    1.0, -0.18,
    "2e₁",
    fontsize=11,
    ha="center",
    va="top"
)

# Draw the second component from the end of the first.
ax.arrow(
    2, 0,
    0, 1,
    length_includes_head=True,
    head_width=0.06,
    head_length=0.08,
    linewidth=2,
    linestyle="--",
    alpha=0.8
)
```

Use a dashed arrow for the second component if it helps show the vector-addition construction.

Use slightly fainter arrows for context vectors, such as the original basis vectors in a plot focused on transformed basis vectors.

## Matrix transformation notebooks

For notebooks about matrices as transformations, a strong learning sequence is:

1. define the standard basis vectors
2. show that coordinates build a vector from those basis vectors
3. introduce a matrix
4. show where the matrix sends each basis vector
5. point out that those destinations are the columns of the matrix
6. show that matrix-vector multiplication rebuilds the vector from the transformed basis vectors
7. use a before/after plot as the visual payoff
8. test the same idea on a second vector, ideally one with a negative coefficient
9. end with a compact summary

Useful phrasing:

> Its coordinates tell us how to build it from the standard basis vectors.

> The vector is not just an arrow. It is also a set of instructions.

> The first column is where $\mathbf{e}_1$ lands.

> The second column is where $\mathbf{e}_2$ lands.

> Matrix-vector multiplication rebuilds the vector using the transformed basis vectors.

> The coefficients stay the same; the basis vectors change.

Use “recipe” sparingly. “Vector as a recipe” can be a useful heading or intuition, but do not force the metaphor into every plot title or summary line.

## Named transformation notebooks

For notebooks about named 2D transformations, keep the basis-vector reading central.

Scaling, reflection, shear, and rotation should not feel like unrelated formula lists.

They should feel like recognisable patterns in where the basis vectors land.

A useful structure is:

1. state the named transformation
2. show the matrix
3. read its columns as $A\mathbf{e}_1$ and $A\mathbf{e}_2$
4. show one example vector
5. plot the original basis/vector faintly and the transformed basis/vector clearly
6. summarise the visual signature

For example:

- uniform scaling: both basis vectors keep direction and change length by the same factor
- non-uniform scaling: both basis vectors keep direction, but scale by different factors
- reflection: one basis direction flips
- horizontal shear: $\mathbf{e}_1$ stays fixed, $\mathbf{e}_2$ gains an x-component
- vertical shear: $\mathbf{e}_2$ stays fixed, $\mathbf{e}_1$ gains a y-component
- rotation: both basis vectors turn together while keeping length $1$ and remaining at right angles

Avoid presenting these only as “one input vector goes in, one output vector comes out”.

## Rotation notebooks

For rotation matrices, explicitly connect sine and cosine to the rotated basis vectors.

For a counter-clockwise rotation by angle $\theta$:

```markdown
$$
R_\theta =
\begin{bmatrix}
\cos(\theta) & -\sin(\theta) \\
\sin(\theta) & \cos(\theta)
\end{bmatrix}
$$

$$
R_\theta\mathbf{e}_1 =
\begin{bmatrix}
\cos(\theta) \\
\sin(\theta)
\end{bmatrix}
\qquad
R_\theta\mathbf{e}_2 =
\begin{bmatrix}
-\sin(\theta) \\
\cos(\theta)
\end{bmatrix}
$$
```

Make the key ideas explicit:

- positive angles rotate counter-clockwise
- negative angles rotate clockwise
- the columns are the rotated basis vectors
- a pure rotation preserves vector length
- the transformed basis vectors stay length $1$ and remain at right angles

A plot of the same vector rotated through several angles can be useful after the basis-vector mechanics have landed.

## Summary sections

Summary sections should be compact and readable.

Avoid mixing bullet points with display maths in a way that creates lots of vertical whitespace.

A good summary shape is:

```markdown
## Summary

The standard basis vectors are:

$$
\mathbf{e}_1 =
\begin{bmatrix}
1 \\
0
\end{bmatrix}
\qquad
\mathbf{e}_2 =
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

A vector with coordinates $x$ and $y$ can be read as:

$$
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
x\mathbf{e}_1 + y\mathbf{e}_2
$$

For a matrix $A$:

- the first column is where $\mathbf{e}_1$ lands
- the second column is where $\mathbf{e}_2$ lands
- matrix-vector multiplication rebuilds the vector using the transformed basis vectors
- the coefficients stay the same; the basis vectors change

The central idea is:

$$
A
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
x(A\mathbf{e}_1) + y(A\mathbf{e}_2)
$$

So a matrix is not just a grid of numbers. In this notebook, we can read it as a transformation that moves the basis vectors, then rebuilds every other vector from those transformed basis vectors.
```

For a parent notebook or section overview, the summary may be slightly broader, but should still be concise and should not duplicate the full child notebooks.

## Code style in notebooks

Keep code simple and readable.

Prefer explicit intermediate variables when they support learning:

```python
Ae1 = A @ e1
Ae2 = A @ e2
Av = A @ v
```

For rotation notebooks, similarly prefer:

```python
Re1 = R @ e1
Re2 = R @ e2
Rv = R @ v
```

Printed output should be compact and notebook-friendly:

```python
def print_vector(name, vector):
    print(f"{name} = [{vector[0]: .2f}, {vector[1]: .2f}]")
```

When a later cell should be rerunnable independently, it is okay to restate small definitions:

```python
w = np.array([-1, 2])
Aw = A @ w
```

Do not make code clever if simple code teaches better.

## Run top-to-bottom consistency

Notebooks should run cleanly from top to bottom without the prose drifting away from the current variable state.

Avoid reusing generic variable names such as `a`, `b`, `v`, or `w` for different teaching examples if later markdown still refers to earlier values.

Prefer example-specific names when a notebook contains more than one scenario:

```python
axis_a = np.array([4, 3])
axis_b = np.array([5, 0])

general_a = np.array([3, 4])
general_b = np.array([5, 1.2])
```

When reviewing, check that every markdown explanation, printed result, and plot still matches the current values if the notebook is executed from a fresh kernel.

## Generated notebook QA

After generating or editing a notebook, inspect the markdown source for common rendering failures:

- no accidental control characters caused by unescaped LaTeX, such as broken `\times`, `\theta`, or `\frac`
- no raw `\[ ... \]` display maths unless specifically requested
- no unintended `\( ... \)` inline maths
- balanced `$$` display maths delimiters
- no markdown prose that contradicts the executed outputs
- no references to retired notebooks in parent notebooks or README files
- no stale “next step” text pointing to a notebook that has been removed or reordered

If a notebook contains code, execute it where practical before handing it over.

If execution is not practical, say so explicitly.

## Review checklist

When reviewing a notebook, check:

- Is the notebook still bite-sized?
- Does each section introduce one clear idea?
- Does the notebook have a unique role in the wider sequence?
- Does it move the learner forward, consolidate intentionally, or duplicate material?
- Would a cleaner learning path result from merging, archiving, or deleting it?
- Are there any orphaned or redundant plots?
- Are all display maths blocks using `$$ ... $$`?
- Are inline maths expressions using `$...$` consistently?
- Are any bullet lists broken by display maths?
- Are plots compact without unnecessary dead space?
- Do comparison plots share axis limits wherever practical?
- Are labels readable and manually nudged where necessary?
- Are plot titles plain and not over-metaphorical?
- Is there any “arrow soup” that should be split into before/after plots?
- Do variable names and markdown explanations remain consistent when the notebook is run top-to-bottom from a fresh kernel?
- Are important mathematical edge cases mentioned without derailing the notebook?
  - Example: cosine similarity is undefined for zero vectors.
  - Example: projection onto the zero vector is undefined.
- Has the markdown source been checked for broken LaTeX escaping, control characters, and balanced `$$` delimiters?
- Does the final summary reinforce the central intuition without becoming too long?
- Do parent notebooks and README files reflect the current notebook sequence?
- Are replacement notebooks ready to take canonical filenames once accepted?

## Preferred overall feel

The notebook should feel polished but not overproduced.

It should look like careful learning material from someone who understands the topic, not like auto-generated notes.

The ideal balance is:

- enough maths to be precise
- enough prose to be intuitive
- enough code to be reproducible
- enough plotting to make the geometry visible
- enough restraint to keep the notebook readable

The ideal sequence is:

- clear enough for learning
- compact enough for revision
- polished enough for a public GitHub repo
- intentional enough that every notebook earns its place
