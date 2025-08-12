### AI-assisted coding and testing

This is a simple demo of using AI-assisted coding to generate code for a Python project and then develop tests for the code.

#### Setup

1. Clone this repository: `git clone https://github.com/poldrack/ai_testing.git`
2. Install [uv](https://docs.astral.sh/uv/getting-started/installation/)
3. run `uv sync` with repo directory

#### Initial prompt

Using Claude Sonnet 4 within VSCode Chat in Agent Mode.

> Generate a Python module to perform multiple regression.  Do not use a pre-existing package; implement the code from scratch using linear algebra.  Use a scikit-learn style interface, with .fit(), .fit_transform(), and .transform(), and .predict() methods methods.  Write clean code with concise numpy-style docstrings.  Check whether the design (X) matrix includes an intercept, and automatically include one if it does not, unless the fit_intercept argument is set to false. Check whether the design matrix is full rank, and raise an exception if it is not.  Use uv for package management and ruff for linting. Outline your plan first before generating any code. Do not generate any tests until explicitly asked to do so.

