## Math Olympiad Repository — Quick Guide

This repository contains the full LaTeX setup for our team math competition (lower and upper divisions).

### Repository structure
.
├── preamble.tex
├── main/
│   ├── lower/
│   │   ├── problems.tex
│   │   └── solutions.tex
│   └── upper/
│       ├── problems.tex
│       └── solutions.tex
├── problems/
│   ├── algebra/           # a1–a7.tex
│   ├── combinatorics/     # c1–c7.tex
│   ├── geometry/          # g1–g7.tex
│   └── number_theory/     # nt1–nt7.tex
└── solutions/
    ├── algebra/           # a1–a7.tex
    ├── combinatorics/     # c1–c7.tex
    ├── geometry/          # g1–g7.tex
    └── number_theory/     # nt1–nt7.tex

### How to add or edit problems
	1.	Find the correct category and level (e.g. Algebra, level 3 → problems/algebra/a3.tex).
	2.	Open that file and paste only the problem description — properly LaTeX formatted.
	•	Do not add titles or numbering like “Problem 1”.
	•	Just the math and text body.
	3.	Add the matching solution to the same subfolder in solutions/ (e.g. solutions/algebra/a3.tex).
	•	Again, no headers or numbering — just the solution text and equations.

### How the compilation works
	•	The main/ folder contains the actual print-ready LaTeX files:
	•	lower/problems.tex and upper/problems.tex for problem booklets.
	•	lower/solutions.tex and upper/solutions.tex for solution booklets.
	•	These files handle:
	•	Sectioning (\section{Algebra}, etc.)
	•	Automatic numbering using \Problem and \ProblemWithSolution
	•	Layout between problems and solutions.

If you change which problems belong to a division or category, simply reorder the relevant \input or \ProblemWithSolution lines in the main/ files.

### ⚙️ Formatting or layout changes
	•	Global formatting commands and macros (e.g. \Problem, \ProblemWithSolution, \Lausn) are defined at the end of preamble.tex.
	•	Edit that file only if you need to adjust numbering, spacing, or header styles.

### Summary
	•	Each problem = two small .tex files, one in problems/, one in solutions/.
	•	No titles or numbering inside those files.
	•	The main/ folder controls ordering and printing.
	•	The preamble.tex controls formatting.
