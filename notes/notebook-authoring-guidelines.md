# Notebook Authoring Guidelines

Internal working notes for keeping notebooks consistent and useful.

## Completion checklist

A notebook is not considered useful for future reference until it includes:

- the core idea in plain English
- a small manual or visual example
- a Python / NumPy / pandas implementation
- a short note explaining why the concept matters for machine learning
- at least one tiny exercise, variation or self-check

## Suggested notebook structure

```markdown
# Notebook Title

## Purpose

What this notebook is trying to make clear.

## Concept

Plain-English explanation of the maths or machine learning idea.

## Tiny Manual Example

A small hand-checkable example before code.

## Python Implementation

NumPy / pandas / scikit-learn implementation.

## Visualisation

A simple plot if it helps.

## Why This Matters for ML

Where this concept reappears in the course or in practical machine learning.

## Exercises

Small variations to test understanding.
```

## Style notes

- Prefer short notebooks over sprawling ones.
- Split a topic when the notebook starts to become a reference chapter.
- Keep plots readable and purposeful.
- Use markdown to explain why the code matters, not just what it does.
- Avoid treating exploratory scratch work as polished course material.
