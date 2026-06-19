---
title: "Jupyter Notebook"
teaching: 30 # teaching time in minutes
exercises: 15 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions

- What is a Jupyter Notebook and why is it useful for data science?
- How do I create and run code in a notebook?
- What are cells, and how do they work?
- What does it mean for a notebook to be "stateful"?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Open a Jupyter Notebook using Google Colab
- Distinguish between code cells and Markdown cells
- Write and execute simple Python code in a notebook
- Understand how variables persist across cells (statefulness)
- Apply best practices for organizing notebooks

::::::::::::::::::::::::::::::::::::::::::::::::

## 1. What Is a Jupyter Notebook?

A **Jupyter Notebook** is an interactive computing environment that allows you to combine:

- Code (Python)
- Text explanations
- Mathematical equations
- Tables and visualizations
- Results and outputs

All in a single document.

Jupyter Notebooks are especially useful for:

- Data exploration and analysis
- Teaching and learning Python
- Prototyping models
- Sharing reproducible research

Instead of writing a script and running it all at once, you work in **small, executable blocks called cells**.

---

## 2. Why Data Scientists Use Jupyter Notebooks

Jupyter Notebooks support an **iterative workflow**:

1. Write a few lines of code
2. Run them immediately
3. Inspect the output
4. Modify and rerun as needed

### Key Advantages

- Immediate visualization of data
- Easy experimentation
- Built-in documentation using Markdown
- Reproducible analysis
- Simple sharing with collaborators

---

## 3. Getting Started: Opening a Notebook

You can use Jupyter Notebooks in several ways:

- Through [Anaconda Navigator](https://www.anaconda.com/products/navigator). Install the application, create an account, and launch *Jupyter Notebook*.

- Through [Google Colab](https://colab.research.google.com). You will need a Google account. Then create a new notebook in Drive.

### Quick Start in Google Colab (easiest for beginners)

1. Go to https://colab.research.google.com
2. Click **File → New notebook**
3. You're ready! No installation needed.

Colab runs in the cloud — you only need a Google account and internet access.

**Tip:** The interface looks almost identical to classic Jupyter.

---

## 4. Understanding Cells

A Jupyter Notebook is composed of cells. Each cell performs a specific role.

### 4.1 Code Cells

- Used to write and execute Python code
- Output appears directly below the cell

```python
x = 10
y = 5
x + y
```

### 4.2 Markdown Cells

- Used for formatted text, headings, lists, and links
- Supports standard Markdown syntax

### 4.3 Raw Cells

- Used infrequently
- Mostly for advanced formatting or export purposes

**Note:** Raw cells are not important for this workshop.

#### Try it now (in a new notebook):

**Code cell 1**
```python
message = "Hello, welcome to Jupyter!"
print(message)
```

**Code cell 2**
```python
print(message + " We're going to have fun!")
```

---

## 5. Running Cells

You can execute cells using keyboard shortcuts:

* `Shift + Enter` → Run cell and move to the next
* `Ctrl + Enter` → Run cell and stay in place
* `Alt + Enter` → Run cell and insert a new one below

**Important:** Cells do not need to be run from top to bottom, but execution order matters. Running cells out of order can lead to unexpected variable values.

---

## 6. The Notebook Kernel

The **kernel** is the computational engine that runs your code.

For Python notebooks, the kernel:

* Executes Python code
* Stores variables in memory
* Can be restarted or interrupted

### Common Kernel Actions

* `Restart Kernel` – Clears all variables from memory
* `Interrupt Kernel` – Stops long-running code

**Best practice:** Restart the kernel and run all cells before sharing a notebook. This ensures your code runs correctly from top to bottom.

---

## Exercise 1: Python Coding

This exercise teaches you how to do basic coding in a Python Jupyter Notebook.

Proceed to the activity: <a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Introduction_Python.ipynb" target="_blank">Here</a>

---

## 7. Variables and Statefulness

Jupyter remembers variables **across cells** as long as the kernel is running.

This is very powerful, but also the source of most beginner frustration.

### Demo – run these cells one by one

**Cell A**
```python
temperature = 20
print("Temperature is", temperature, "°C")
```

**Cell B**
```python
temperature = temperature + 5
print("New temperature:", temperature, "°C")
```

**Cell C**
```python
print("What is the temperature now?", temperature)
```

:::::::::::::::::::::::::::::::::::: challenge

### Challenge — Variable State

1. Create 3 new code cells
2. In cell 1: `count = 0`
3. In cell 2: `count = count + 1; print(count)`
4. In cell 3: `print("Final count:", count)`
5. Run all three cells in order — cell 3 should print `1`
6. Now run **only cell 2** five more times
7. Run cell 3 again — what happened?

You just experienced statefulness in action! The variable `count` persisted across cell executions, accumulating changes each time you ran cell 2.

::::::::::::::::::::::::::::::::::::::::::::::::

---

## Exercise 2: Variable Handling

This exercise teaches you how data is stored and updated for a given variable in a Python Jupyter Notebook.

Proceed to the activity: <a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Variables_Intro.ipynb" target="_blank">Here</a>

---

## 8. Working with Data in Jupyter

Most data science workflows start by importing libraries and loading data.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

### Loading Data

```python
df = pd.read_csv("data.csv")
df.head()
```

---

## 9. Visualization Inside Notebooks

Plots are displayed inline, directly below the code cell.

```python
plt.plot([1, 2, 3, 4], [10, 20, 25, 30])
plt.xlabel("X values")
plt.ylabel("Y values")
plt.title("Simple Line Plot")
plt.show()
```

This makes exploratory analysis fast and interactive.

---

## Exercise 3: Python Plotting

This exercise teaches you how to create plots in a Python Jupyter Notebook.

Proceed to the activity: <a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Intro_Ploting.ipynb" target="_blank">Here</a>

---

## 10. Using Markdown for Documentation

Well-written notebooks tell a **story**.

Use Markdown cells to:

- Explain your approach
- Describe datasets
- Interpret results
- Organize sections with headings

### Example Notebook Structure

1. Title and Introduction
2. Dataset Overview
3. Data Cleaning
4. Visualization
5. Key Findings

This improves readability for both technical and non-technical audiences.

---

## 11. Best Practices and Common Pitfalls

### Organizing Your Notebook

- Keep notebooks focused on a single task
- Use clear section headers with Markdown cells
- Put all `import` statements in the first code cell
- Keep cells short (5–15 lines each) — one logical step per cell
- Use descriptive file names
- Move reusable code into `.py` files as projects grow

### Avoiding Common Mistakes

- **Running cells out of order** can give variables unexpected values. Fix this by selecting **Kernel → Restart & Run All** regularly.
- **Forgetting to import libraries** after restarting the kernel causes `NameError`. Always keep imports in the first cell.
- **No Markdown explanations** makes notebooks difficult to revisit. Add context before and after important code blocks.
- **Sharing without restarting** means collaborators may see missing variables or wrong results. Always do **Kernel → Restart & Run All** before sharing or exporting.
- **Assuming outputs are permanent** — outputs disappear on kernel restart. Rely on your code, not on saved output.

---

## Troubleshooting

- **Colab:** Plots not showing? Add `%matplotlib inline` at the top of your notebook (usually automatic in Colab).
- **Local Jupyter:** "Package not found" error? Open a terminal or a code cell and run `!pip install package_name`.
- **Need help?** Raise your hand during the workshop.

---

::::::::::::::::::::::::::::::::::::: keypoints

- Jupyter Notebooks let you combine code, output, and documentation in a single interactive document.
- Notebooks are made up of cells — code cells run Python, Markdown cells hold formatted text.
- The kernel remembers variables across cells (statefulness), so execution order matters.
- Always restart the kernel and run all cells before sharing a notebook.
- Good notebooks use short cells, clear headings, and Markdown explanations to tell a story.

::::::::::::::::::::::::::::::::::::::::::::::::