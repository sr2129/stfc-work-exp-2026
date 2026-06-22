# STFC Work Experience Project

This repository contains a one-week, hands-on Python project prepared for STFC work experience. The project uses real scientific examples, mostly from particle physics, to explore Python, arrays, plotting, data analysis, performance, and scientific computing. It ends with an additional astronomy notebook on the mathematical rediscovery of Neptune.

[Click here to start reading!](https://hsf-training.github.io/array-oriented-programming/)

## Status of daily deployments

(The version you read online is from the last _successful_ deployment.)

<a href="https://github.com/hsf-training/array-oriented-programming/actions/workflows/deploy.yml">
	<img src="https://github.com/hsf-training/array-oriented-programming/actions/workflows/deploy.yml/badge.svg" alt="Check deploy.yml" height="40">
</a>

Most of the material lives in the notebooks folder. The project is structured around five lessons, each with a guided workbook and a follow-up project notebook.

## Project at a glance

The project is built around these themes:

| Lesson | Main idea | Main notebooks |
| --- | --- | --- |
| Lesson 1 | Python basics for scientific work: variables, functions, imports, plotting, and particle-physics-flavored calculations | `notebooks/lesson-1-workbook.ipynb`, `notebooks/lesson-1-project.ipynb` |
| Lesson 2 | Array-oriented programming with NumPy and HDF5 data | `notebooks/lesson-2-workbook.ipynb`, `notebooks/lesson-2-project.ipynb` |
| Lesson 3 | Ragged and nested data with Awkward Array, plus combinatorics for Higgs reconstruction | `notebooks/lesson-3-workbook.ipynb`, `notebooks/lesson-3-project.ipynb` |
| Lesson 4 | Making Python faster with scaling, compiled code, and JIT compilation with Numba | `notebooks/lesson-4-workbook.ipynb`, `notebooks/lesson-4-project.ipynb` |
| Lesson 5 | Python on GPUs with CuPy and CUDA-style workflows | `notebooks/lesson-5-workbook.ipynb`, `notebooks/lesson-5-project.ipynb` |
| Extension | Mathematical astronomy: rediscovering Neptune from orbital deviations | `notebooks/Neptune_discovery_Problem.ipynb` |

Across the week, the work repeatedly returns to the same scientific question in different computational forms: finding and reconstructing Higgs decays from data stored as JSON, HDF5, ragged arrays, and GPU-friendly arrays.

## How the material is organized

- `notebooks/`: the main project material.
- `notebooks/lesson-*-workbook.ipynb`: guided lesson notebooks with examples, prompts, and space to experiment.
- `notebooks/lesson-*-project.ipynb`: application notebooks where the lesson ideas are used on larger scientific problems.
- `notebooks/Neptune_discovery_Problem.ipynb`: a separate extension notebook that uses Fourier analysis, Kepler's third law, and Newtonian gravity to infer the presence of an unseen planet.
- `solutions-NO-PEEKING/`: reference solutions for the project notebooks.
- `array-oriented-programming/`: the source for the accompanying Jupyter Book notes.

## Suggested flow for the week

1. Start with `notebooks/lesson-1-workbook.ipynb`.
2. Complete the matching project notebook before moving to the next lesson.
3. Continue in order through lessons 2 to 5.
4. Use `notebooks/Neptune_discovery_Problem.ipynb` as an extension, enrichment task, or final discussion notebook.

This structure works well for a five-day work experience project: workbook first, project second, then discussion or review.

## Running the project locally

The repository includes a Conda environment file with the core scientific Python stack used throughout the project.

```bash
conda env create -f environment.yml
conda activate array-oriented-programming
jupyter lab
```

Then open the `notebooks/` folder and begin with `lesson-1-workbook.ipynb`.

You can also use VS Code with the Python and Jupyter extensions if you prefer that workflow.

## Software notes

- Lessons 1 to 4 use the packages listed in `environment.yml`.
- Lesson 5 is optional on machines without an Nvidia GPU.
- To run the GPU material fully, you will need a compatible Nvidia driver plus CUDA-compatible packages such as `cupy` in addition to `numba`.

## Online notes

The companion Jupyter Book linked above is useful as reference material, but the main day-to-day project work in this repository is the notebook sequence in `notebooks/`.
