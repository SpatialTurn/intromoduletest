---
title: "Jupyter Notebook Refresher"
teaching: 10
exercises: 20
---

:::::::::::::::::::::::::::::::::::::: questions

- Can I write and run Python code in a Jupyter Notebook?
- Do I understand how variables persist across cells?
- Can I create a basic plot?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Verify your Python and Jupyter skills before the workshop
- Complete three self-check exercises covering basic coding, variables, and plotting

::::::::::::::::::::::::::::::::::::::::::::::::

## Overview

This page is a quick refresher, not a full tutorial. You should already be comfortable with basic Python — variables, data types, imports, and simple operations. If any of the exercises below feel unfamiliar, please review a Python fundamentals tutorial before the workshop.

We will be using [Google Colab](https://colab.research.google.com) for all notebook activities. Colab runs in your browser and requires no installation — just a Google account.

---

## Quick Reminders

**Cells** are the building blocks of a notebook. Code cells run Python; Markdown cells hold formatted text.

**Running a cell:** `Shift + Enter` runs the current cell and moves to the next.

**Statefulness:** The notebook kernel remembers variables across cells. If you run a cell that sets `x = 5`, every cell after that can use `x` — until you restart the kernel.

**Restart & Run All:** Before sharing or submitting a notebook, always restart the kernel and run all cells from top to bottom to make sure everything works in order.

---

## Exercise 1: Python Coding

Covers basic syntax, printing, and simple operations.

<a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Introduction_Python.ipynb" target="_blank">Open Exercise 1 in Colab</a>

## Exercise 2: Variable Handling

Covers how data is stored, updated, and reused across cells.

<a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Variables_Intro.ipynb" target="_blank">Open Exercise 2 in Colab</a>

## Exercise 3: Python Plotting

Covers creating basic charts with matplotlib.

<a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Intro_Ploting.ipynb" target="_blank">Open Exercise 3 in Colab</a>

---

::::::::::::::::::::::::::::::::::::: keypoints

- Jupyter Notebooks let you run Python code in small, interactive cells.
- Variables persist across cells — execution order matters.
- If all three exercises felt comfortable, you are ready for the workshop.

::::::::::::::::::::::::::::::::::::::::::::::::