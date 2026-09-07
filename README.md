# Running the Notebook Locally

This guide explains how to set up and run the `.ipynb` file on your own machine using Jupyter Notebook.

## Prerequisites

- Python 3.8 or higher installed on your system
- `pip` (Python package manager)

Check your Python version:

```bash
python --version
```

## 1. Create a Virtual Environment (Recommended)

It's good practice to isolate dependencies in a virtual environment.

**macOS / Linux**
```bash
python -m venv venv
source venv/bin/activate
```

**Windows**
```bash
python -m venv venv
venv\Scripts\activate
```

## 2. Install Jupyter

```bash
pip install notebook
```

If your notebook uses additional libraries (e.g., `pandas`, `numpy`, `matplotlib`), install them as well:

```bash
pip install pandas numpy matplotlib
```

> Tip: If a `requirements.txt` file is included in this project, install everything at once with:
> ```bash
> pip install -r requirements.txt
> ```

## 3. Launch Jupyter Notebook

Navigate to the folder containing the `.ipynb` file, then run:

```bash
jupyter notebook
```

This will open a new tab in your default web browser showing the Jupyter file interface.

## 4. Open the Notebook

- In the browser window that opens, click on the `.ipynb` file to open it.
- Run cells individually with `Shift + Enter`, or run all cells via **Cell > Run All** in the menu.

## 5. (Optional) Using JupyterLab Instead

If you prefer the JupyterLab interface:

```bash
pip install jupyterlab
jupyter lab
```

## 6. Deactivating the Virtual Environment

When you're done working:

```bash
deactivate
```

## Troubleshooting

- **"jupyter: command not found"** → Make sure your virtual environment is activated and Jupyter was installed inside it.
- **Kernel errors / missing packages** → Ensure all required libraries are installed in the same environment the notebook's kernel is using. You can check installed packages with `pip list`.
- **Port already in use** → Run `jupyter notebook --port 8889` (or any other free port).

## Notes

- Replace `venv` with any name you'd like for your virtual environment.
- If working with sensitive data, avoid committing outputs or data files to version control (add them to `.gitignore`).
