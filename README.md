# DSA homework

Course homework by Madi Zhassymbek.

Each assignment has its own numbered folder.

| Assignment | Topic |
| --- | --- |
| [HW01](hw01/) | Python types, strings, lists, and loops |

## Structure

```text
dsa-homework/
  README.md
  .gitignore
  hw01/
    hw01.ipynb
    README.md
```

Create `hw02`, `hw03`, and later folders as new assignments arrive. Save each notebook as `hwNN.ipynb` inside its matching folder.

## Working on a notebook

Open notebooks in Jupyter, VS Code with the Jupyter extension, or Google Colab. HW01 uses Python 3 built-ins and needs no third-party packages. Restart the kernel, run all cells from top to bottom, and save the notebook.

## Save and upload changes

Run these commands from the repository directory:

```powershell
git status
git add hw01
git commit -m "hw01: update notebook"
git push
```

For another assignment, replace `hw01` with its folder name. Use `git pull --ff-only` before working if the repository was updated elsewhere.
