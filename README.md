# DSA homework

Course homework by Madi Zhassymbek.

Each assignment has its own numbered folder. This repository is private.

| Assignment | Topic | Status |
| --- | --- | --- |
| [HW01](hw01/) | Python types, strings, lists, and loops | Original attempt checked; corrections pending |

## Structure

```text
dsa-homework/
  README.md
  .gitignore
  hw01/
    hw01.ipynb
    README.md
```

Create `hw02`, `hw03`, and later folders as new assignments arrive. Save each notebook as `hwNN.ipynb` inside its matching folder and add a short README describing progress.

## Working on a notebook

Open the notebook in Jupyter, VS Code with the Jupyter extension, or Google Colab. HW01 uses Python 3 built-ins and needs no third-party packages. Restart the kernel and run every cell from top to bottom before submitting. Save the notebook after checking its output.

## Save and upload changes

Run these commands from this repository's directory:

```powershell
git status
git add hw01
git commit -m "hw01: describe the changes"
git push
```

For the next assignment, replace `hw01` with its folder name. Use `git pull --ff-only` before working if the repository was updated elsewhere. Check that the latest files appear on GitHub after pushing.

Python caches, notebook checkpoints, virtual environments, and `.env` files are excluded by `.gitignore`. Do not commit passwords, API keys, or datasets larger than 50 MB.

## Instructor access

The instructor has not been invited. Once their exact GitHub username is known, grant access through GitHub's repository settings when ready to share the work. Uploading this attempt does not mean it is ready to submit or has been graded.
