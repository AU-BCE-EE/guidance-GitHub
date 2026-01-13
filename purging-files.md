# Removing all traces of a file (purging)

Sometimes we make a mistake and include a file with sensitive information, or one that is bigger than the maximum allowed by GitHub.
Even if it is removed in a following commit, the file can be found within the commit history, and so more effort is needed to completely remove it.
Follow the instructions below to completely remove it.

# Option 1: File was in last commit only

Open up a shell, navigate to the local repo location, and run:

```
git rm --cached exact/path/to/file.csv
git commit --amend
git push
```

Make sure the path is correct!

Confirm it is gone with:

```
git log --all -- exact/path/to/file.csv
```

# Option 2: File was in an earlier commit

This is a bit trickier.

1. Make a copy of your local repository. This operation could destroy everything. Include the hidden .git directory unless you do not care about the history.
2. Install the git filter-repo tool with:
    ```
    brew install git-filter-repo        # macOS
    sudo apt install git-filter-repo    # Debian/Ubuntu
    ```
3. Open up a shell, navigate to the local repo location, and run:
    ```
    git remote -v
    ```
4. Then run:
    ```
    git filter-repo --path exact/path/to/file.csv --invert-paths
    ```
    Be sure of the path.
5. Run:
    ```
    git remote add origin <repo_url>
    ```
    where `<repo_url>` is the URL returned in step 3 (or copied from your GitHub page).
6. Force-push the cleaned history with:
    ```
    git push origin --force --all
    git push origin --force --tags
    ```

# If you are not sure

1. Open up a shell, navigate to the local repo location, and run:
    ```
    git log -- exact/path/to/file.csv
    ```
    If you see only one commit, got to option 1 above.
    If you see more than one, go to 2.

