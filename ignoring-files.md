# Making Git ignore some files in your repo
If you have data files that are too big for GitHub, if the data analysis software you use creates files that you don't want to include (.RData, .Rproj, __pycache__), or if you just want to exclude some files, you can do so with a special file in your repository called `.gitignore`.
It is just a plain text file with file or directory name patterns (or just names) to exclude. 
You can find templates for different types of repos here: <https://github.com/github/gitignore>.
And GitHub will ask if you want to select and include a template when you create a new repo.
Usually it makes sense to start with the most relevant template and then edit it over time if needed.

It is easiest to set up a .gitignore file at the start, when creating a repo.
If you want it to apply to files that are already present and committed, you must first delete the files and commit.
Then create or update .gitignore and commit.
The next time the files are created they will be ignored.

# Related guidance
This topic is discussed in:
* [repo-creation.md](https://github.com/AU-BCE-EE/GitHub-guidance/blob/main/repo-creation.md)
* [issue #12](https://github.com/AU-BCE-EE/GitHub-guidance/issues/12)

The [paper](https://github.com/AU-BCE-EE/template-paper/) template repo includes a `.gitignore` file for R.

