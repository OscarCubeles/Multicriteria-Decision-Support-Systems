# Multicriteria Decision Support Systems

Coursework and research projects exploring **multicriteria decision analysis (MCDA)** methods through practical decision problems. The repository covers Logic Scoring of Preference (LSP), the Weighted Sum Model (WSM), Ordered Weighted Averaging (OWA), ELECTRE III, and a literature study of Data Envelopment Analysis (DEA) in healthcare.

The work was completed for the *Multiple Criteria Decision Support Systems* course in the master's programs in Artificial Intelligence and Computer Security & Artificial Intelligence at Universitat Rovira i Virgili (URV).

## Repository contents

| Deliverable | Method | Decision problem | Main files |
| --- | --- | --- | --- |
| **Task 1** | Logic Scoring of Preference (LSP) | Recommend TV shows from preferences about duration, action, science fiction, and comedy | [`T1/data.csv`](T1/data.csv), [`T1/oscar_cubeles.pkl`](T1/oscar_cubeles.pkl), [report](T1/oscar_cubeles_Task1.pdf) |
| **Task 2** | Weighted Sum Model (WSM) and Ordered Weighted Average (OWA) | Rank virtual restaurants using six criteria and compare aggregation policies | [notebook](T2/Task2_OWA_virtual_restaurants.ipynb), [report](T2/PMCDSS__TASK_2___OWA.pdf) |
| **Task 3 / Research project** | ELECTRE III | Rank 12 exchange universities using academic, financial, quality-of-life, career, and distance criteria | [notebook](T3/TASK_7_PMCDSS_Research_Project_v2.ipynb), [report](T3/TASK_7_PMCDSS_Research_Project_v2.pdf) |
| **Research report** | Data Envelopment Analysis (DEA) | Review DEA methods, tools, extensions, and healthcare applications published between 2015 and 2025 | [report](oscar_cubeles_queralt_benito.pdf) |

## Project highlights

### Task 1 - LSP TV-show recommendation

This task builds a hierarchical preference model for evaluating TV shows. Five elementary criteria are grouped into **Duration** and **Content**, then aggregated into an overall suitability score. The experiments examine how criterion importance and conjunctive, neutral, and disjunctive aggregation affect the ranking.

The supplied `.pkl` model was created with the LSP software developed by the ITAKA research group at URV. The accompanying CSV contains the evaluated alternatives, and the PDF documents the model, utility functions, tests, and results.

### Task 2 - WSM and OWA restaurant ranking

The notebook compares two numerical aggregation approaches:

- **WSM** assigns importance directly to criteria such as food, personnel, atmosphere, category, location, and terrace.
- **OWA** assigns weights after criterion values are ordered, making it possible to model optimistic/disjunctive and conservative/conjunctive decision policies.

It also studies OWA descriptors including balance, divergence, entropy, and orness. In the evaluated dataset, **Barhaus** remains the strongest restaurant under the principal weighting scenarios.

### Task 3 - ELECTRE III exchange-university ranking

The research project models exchange-university selection as a partial-ranking problem. ELECTRE III compares 12 universities using:

- world ranking;
- available scholarships;
- cost of living;
- life expectancy;
- expected salary after graduation; and
- distance from Barcelona.

Indifference, preference, and veto thresholds capture the decision maker's tolerance for differences between alternatives. Two experiments test a balanced preference profile and a profile focused more heavily on long-term financial and quality-of-life outcomes. **Technical University of Munich** leads the balanced scenario, while **Technical University of Munich and Aalto University** emerge as the principal recommendations when long-term benefits receive greater emphasis.

### DEA in healthcare

The standalone research report introduces DEA, surveys its use in healthcare, and reviews publication trends, influential authors and institutions, geographical patterns, common applications, software, and extensions such as super-efficiency, fuzzy, network, and stochastic DEA.

## Getting started

### Prerequisites

- Python 3.9 or newer
- JupyterLab or Jupyter Notebook

Clone the repository and create a virtual environment:

```bash
git clone https://github.com/OscarCubeles/Multicriteria-Decision-Support-Systems.git
cd Multicriteria-Decision-Support-Systems
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Or on macOS/Linux:

```bash
source .venv/bin/activate
```

Install the notebook dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install jupyterlab pandas numpy matplotlib
```

Then start JupyterLab:

```bash
jupyter lab
```

Open either executable notebook from the file browser. Each notebook includes a cell that installs the version of [`mcda`](https://py-mcda.readthedocs.io/) used for that exercise:

- Task 2 uses `mcda==0.4.0`.
- Task 3 uses `mcda==0.4.1`.

Because the notebooks use different package versions, run the installation cell when switching tasks or use a separate virtual environment for each notebook if exact reproducibility is important.

## Reproducing the analyses

1. Start JupyterLab from the repository root.
2. Open the relevant `.ipynb` file.
3. Run the cells from top to bottom.
4. Compare the generated performance tables, matrices, rankings, and plots with the corresponding PDF report.

Task 1 is provided as an LSP model, input dataset, and report rather than a Jupyter workflow. The DEA deliverable is a literature review and does not include executable analysis code.

## Authors

- **Oscar Cubeles Ollé** - Tasks 1 and 2; co-author of the ELECTRE III and DEA research projects
- **Queralt Benito Martín** - Co-author of the ELECTRE III and DEA research projects

## Acknowledgements

- Universitat Rovira i Virgili (URV)
- ITAKA research group
- [`py-mcda`](https://py-mcda.readthedocs.io/) contributors

## License

No license has been specified for this repository. Unless a license is added, the materials remain subject to standard copyright restrictions.
