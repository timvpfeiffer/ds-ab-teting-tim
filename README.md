# A/B Testing: Frequentist, Bayesian, and Experiment Design

A hands-on introduction to A/B testing on a real e-commerce conversion dataset. You work through analysing a finished experiment with both frequentist and Bayesian methods, then planning a new experiment (sample size, runtime, and minimum detectable effect), and finally guided practice that rehearses the full workflow.

## Learning Objectives

By the end of this repository, you should be able to:

- Design an A/B test by defining the hypothesis, the control and treatment groups, and the success metric.
- Clean experimental data by removing contaminated and duplicated group assignments.
- Run a frequentist chi-square test and interpret the resulting p-value against a significance level.
- Estimate each variant's conversion probability with a Bayesian Beta-Binomial model and compare the posteriors.
- Calculate the required sample size, expected runtime, and minimum detectable effect (MDE) for a planned experiment.
- Recommend a launch decision by weighing the frequentist and Bayesian evidence against realistic business scenarios.

## Learning Path

Work through the notebooks in this order:

| File / Folder | Description |
|---|---|
| [**01 - A/B Testing**](01_AB_testing.ipynb) | Clean the data, explore it, and evaluate a finished A/B test with both frequentist (chi-square) and Bayesian (Beta distribution) approaches. |
| [**02 - Experiment Design**](02_AB_testing_experiment_design.ipynb) | Estimate the baseline conversion rate, then plan a future test: required sample size, expected runtime, and detectable lift. |
| [**03 - Practice**](03_AB_testing_practice.ipynb) | Rehearse the full workflow through guided exercises focused on interpretation and business decision-making. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Data**](data/) | The e-commerce conversion dataset (`ab_data.csv`) used across the notebooks. |
| [**Assets**](assets/) | Diagrams used in the notebooks (statistical inference pipeline, frequentist vs Bayesian). |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it, including the `< >` brackets, with your own value. For example, `cd <repo-name>` becomes `cd ds-ab-testing`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in (`.venv/`).

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**SciPy: chi2_contingency**](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.chi2_contingency.html): The chi-square test of independence used for the frequentist analysis.
- [**statsmodels: NormalIndPower**](https://www.statsmodels.org/stable/generated/statsmodels.stats.power.NormalIndPower.html): Power and sample-size calculations for two-sample tests.
- [**An Intuitive Explanation of Bayes' Theorem**](https://betterexplained.com/articles/an-intuitive-and-short-explanation-of-bayes-theorem/): A plain-language walkthrough of the theorem behind the Bayesian approach.
- [**Statistical Power and Power Analysis in Python**](https://machinelearningmastery.com/statistical-power-and-power-analysis-in-python/): Practical power analysis with statsmodels, useful for the experiment-design notebook.
- [**A/B Test Calculator (ABTestGuide)**](https://abtestguide.com/calc/): An interactive calculator for checking significance and observed power on real test counts.
- [**Are You Bayesian or Frequentist? (Cassie Kozyrkov)**](https://www.youtube.com/watch?v=GEFxFVESQXc): A short talk contrasting the two schools of inference.
