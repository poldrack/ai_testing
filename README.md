### AI-assisted coding and testing

This is a simple demo of using AI-assisted coding to generate code for a Python project and then develop tests for the code.

#### Setup

1. Clone this repository: `git clone https://github.com/poldrack/ai_testing.git`
2. Install [uv](https://docs.astral.sh/uv/getting-started/installation/)
3. run `uv sync` with repo directory

#### Initial prompt

Using Claude Sonnet 4 within VSCode Chat in Agent Mode.

- Make sure that README.md is not in context - otherwise it will receive the testing instructions.
- create and check out a new dev branch: `git checkout -b dev/claude`

> Generate a Python module to perform multiple regression using ordinary least squares.  Do not use a pre-existing package; implement the code from scratch using linear algebra. Create a class called RegressionOLS. Use a scikit-learn style interface, with .fit(), .fit_transform(), and .transform(), and .predict() methods.  Check whether the design (X) matrix includes an intercept, and automatically include one if it does not, unless the fit_intercept argument is set to false. Check whether the design matrix is full rank, and raise an exception if it is not.  Use uv for package management and ruff for linting. Write clean code with concise numpy-style docstrings.  Do not place any code in __init__.py files.  Place the module within src/ai_testing directory and tests within tests/ directory.  Outline your plan first before generating any code. Do not generate any tests yet.

- save chat transcript to claude_chat_transcript1.md

#### Test generation

- add multiple_regression.py and claude_chat_transcript1.md to context

> Generate tests for the class defined in multiple_regression.py.  Use the pytest testing framework.  generate tests for all methods.  also generate tests to compare the results to the scikit-learn LinearRegression method.