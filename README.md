# WAVE 3 | Template and requirements repository

Template repository and requirements for projects in WAVE3.

# Project Requirements

### Obligatory Tech Requirements


| ID | **Requirement**                                                                           | **Technology**                                                                                                 | **Resources**                                                                                                                                                                                           | **Size** | **Why Should I Care?**                                                                                                                                               | 
|----|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| 1  | Type checking                                                                             | Mypy                                                                                                           | [MyPy Documentation](https://mypy.readthedocs.io/en/stable/)                                                                                                                                            | M        | It's used for static type checking in Python, helping developers catch type errors and improve code reliability before runtime.                                      |
| 2  | Linting and formatting                                                                    | The Ruff Formatter                                                                                             | [The Ruff Formatter Documentation](https://docs.astral.sh/ruff/formatter/)                                                                                                                              | S        | It's used for fast, automated linting and code formatting in Python, enforcing style and quality standards across codebases.                                         |
| 3  | Automating CI/CD workflows                                                                | Pipelines in GitHub Actions                                                                                    | [Quickstart for GitHub Actions](https://docs.github.com/en/actions/writing-workflows/quickstart), [pyproject.toml Documentation](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/) | M        | It automates workflows for building, testing, and deploying code directly from a GitHub repository, streamlining CI/CD processes.                                    |
| 4  | Track dependencies and use consistent Python version. Semantic versioning of the project. | `pip` / `conda` / `poetry` and respective files: `requirements.txt`, `pyproject.toml`.                         | [Semantic Versioning](https://semver.org/), Real Python tutorial on [Poetry](https://realpython.com/dependency-management-python-poetry/)                                                               | M        | While cooperation it is crucial to able to reproduce your python environment.                                                                                        |
| 5  | Simplify project installation, testing and running.                                       | `Makefile`                                                                                                     | Checkout the Makefile from this repository! [Makefile in python tutorial](https://earthly.dev/blog/python-makefile/)                                                                                    | S        | Using Makefiles makes it clear and easy to run projects. This comes in handy especially when programmers not involved in your project want to run it.                |
| 6  | Use .gitignore to exclude unnecessary files.                                              | `.gitignore`                                                                                                   | [.gitingore documentation](https://git-scm.com/docs/gitignore), [GitHub .gitignore Templates](https://github.com/github/gitignore)                                                                      | S        | Prevents clutter in your repository by ignoring files that don't need to be version-controlled, such as temporary files, build artifacts, and environment files.     |
| 7  | Modular Structure (it is not possible to have everything in one notebook or .py file)     | Python, OOP principles, modular design, Python, PyTorch Lightning.                                             | [File structure guide](https://www.suitefiles.com/guides/folder-structures-guide/).[PyTorch Lightning Documentation](https://pytorch-lightning.readthedocs.io/en/latest/).                              | M        | Dividing code into logical modules helps to manage complexity, reusability, and clarity.                                                                             |
| 8  | High quality README                                                                       | Markdown                                                                                                       | [Markdown Guide](https://www.markdownguide.org/)                                                                                                                                                        | S        | A good README should contain the aim of the project, instructions on how to install and run it, project members, and references to external resources if applicable. |
| 9  | Link to a deployed demo                                                                   | Gradio / Streamlit                                                                                             | [Gradio quickstart](https://www.gradio.app/guides/quickstart)                                                                                                                                           | M        | A demo allows users to quickly test the project without setting it up locally, improving accessibility and feedback.                                                 |
| 10 | Theoretical notes and research references                                                 | Markdown                                                                                                       | Papers                                                                                                                                                                                                  | M        | It explains a phenomenon which you are dealing in project and acts as a conceptual base for understatement how it works.                                             |
| 11 | Usage of pathlib.Path                                                                     | Python PathLib Module                                                                                          | [Datacamp Tutorial](https://www.datacamp.com/tutorial/comprehensive-tutorial-on-using-pathlib-in-python-for-file-system-manipulation)                                                                   | S        | It ensures that projects remain platform-independent and provides a structured representation of file system paths.                                                  |
| 12 | Datacard                                                                                  | For **writing**: Markdown, Jupyter Notebook, Hugging Face Datacard. For **plots**: Matplotlib, Seaborn, Pandas | [Hugging Face Datacard](https://huggingface.co/docs/datasets/dataset_card)                                                                                                                              | M        | To implement a model that really works, it's crucial to understand the data we are working with.                                                                     |

### Obligatory Presentation Requirements
**Formatting requirements**
- Use [Czarna magia Template](https://www.canva.com/design/DAGRrlE2mOI/sw7SnAlhf-atPrbI34m5Sg/edit?utm_content=DAGRrlE2mOI&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton,).
- Don't use two of the same backgrounds from template in a row.
- Don't put too much text on the slide. 
- Don't make slides with just text. Always add some image or gif (may be a meme).
- The text on the slides must be clearly visible on the projector (we ususally use a header size of 92 and a text size of 34)
- Add transitions to slides, we use `Match & Move` on canva.

**Content requirements**
- Problem Statement
- Introduce your Team.
- Dataset Selection
- Feature Engineering and Data Preprocessing
- Research and model selection
- Model Training and Hyperparameter Tuning
- Evaluation Metrics and Model Performance
- Error Analysis and Model Limitations
- Demo Application
- Conclusions

### Optional (Comming soon!)

- Demo containerized in Docker
- ...

## Knowledge Sources

What should I know to get the most out of WAVE projects? The framework is designed to create ambitious projects while
giving candidates the opportunity to learn from their more experienced colleagues. However, you will benefit more if you
have prior knowledge or invest extra time in learning during the WAVE project. In this section, you will find a list of
helpful resources.

## Review protocol
- Create task with listed requirements that describes its goal
- Name of task should be concise and clear
- Commit message template: `scope | short_description`, eg. `fix | user auth`. Scope Keywords: Use the following keywords to categorize the commit:
    - `feature`: New feature or functionality.
    - `fix`: Bug fix.
    - `docs`: Documentation changes.
    - `format`: Code style changes (formatting, linting).
    - `refactor`: Code refactoring (no functional changes).
    - `test`: Adding or modifying tests.
- PR name template: same as commit
- Add labels to PR: start/end date
- Person that open PR should close it
- Branch naming: `feat/user-authentication`
- Commits have to pass CI/CD checks before they can be merged
- All change requests have to be resolved before merge
- More than half of assigned people should approve to PR would be merged (eg. 5 assigned -> min. 3 people should approve)