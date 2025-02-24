# Using Git and GitHub
Git is a tool for computer code version control.
GitHub is a website and service that works with Git repositories.
They are commonly used together.
Both were originally created for work on software development, but together are nearly perfect for collaborating on anything that contains text files.
In the Environmental Engineering Section we use them for

* sharing files within the section and with the public
* collaborating on data analysis and model development

# An example application
All work shared through GitHub is organized into "repos", which is short for repositories.
The <https://github.com/AU-BCE-EE/Hafner-2023-bls-wt-comp> repo is a typical application.
It could be called a "research compendium", and it contains all the data, code, and output associated with a research paper.
The repo contents were developed by three of us in the section working together on a paper.
We used it to share the measurement data, model results, and results of data visualization and analysis with each other, to collaborate on these files, and now to share it with the public, all through one repo.

How did we do it?
With some version of Git running locally, each of us had a local copy (on our computer drive) of all the repo files, and could edit or add to any part, (usually) avoiding file synchronization conflicts.
Every step we took is documented in the [commit history](https://github.com/AU-BCE-EE/Hafner-2023-bls-wt-comp/commits/main/), and any of these changes could be "reverted", or undone.
When we finally finished the associated paper and it was published, we updated the README.md file that we include in every repo with the paper citation and a link, and created another [release](https://github.com/AU-BCE-EE/Hafner-2023-bls-wt-comp/releases), which is just a clear way to present a particular point in the repo time as particularly meaningful.
In this case the latest release is associated with the published paper, and because we made the repo public, any reader of the paper could download our measurements, run our R and Matlab scripts, and repeat or tweak what we did.
This makes for "reproducible research".

# First steps
Section members who want to work in GitHub need to:

1. Create a GitHub account
2. Install some version of Git locally

All local work can be done using the command line, and a search online can tell you how to install command-line git.
But for Windows and Mac OS, GitHub provides a free and quite good program called "GitHub Desktop", which has a graphical interface.
It can be downloaded from [here](https://desktop.github.com/).

Be sure to save your local files to a logical location--this may be different from the default proposed by GitHub Desktop!

# Basic workflow
Once you have been added to a repo by the owner, or have created your own repo through GitHub, you need to "clone" it, to get a local copy of its files.
This only needs to be done once.
Then, the basic workflow is:

1. "Pull" the latest version of the files from the remote repo (at GitHub) with `$ git pull` in a command line shell, or by clicking the "Pull origin" button in GitHub Desktop. This will update the local files on your computer.
2. Work on the files as you normally would, adding or editing scripts, adding data files, creating analysis output.
3. "Add" the changes (including edits, new files, and deleted files) to the Git "index" with `$ git add filename.csv` in a command line shell, or in GitHub Desktop, by checking the box to the left of the change. 
4. "Commit" the changes you previously added with `$ git commit -m 'briefly describe the changes here'` in a shell, or using the "Summary" and "Description" field in GitHub Desktop and clicking the blue "Commit to main" button. Changes shold be, ideally, grouped together so commits are mainly on one topic. See below for more discussion on this.
5. "Push" your commit or commits to the remote repo, i.e., to GitHub using the blue "Push origin" button. Once pushed collaborators can "pull" your changes so they are working on the same version.

# When and what to commit
The point of commits is to describe what you did and to provide a checkpoint that could be revisited at any time.
So try to group together related changes.
At a minimum, a commit should be made at the end of the day unless a repo has only one contributor (no collaborators).
But it is inconvenient and not very useful to make many small commits.
Ideally, a commit would be made after some significant change is made, e.g., new measurements are used, statistical analysis approach is changed, figure captions are fixed.
But in practice it is sometimes difficult to group work into discrete consistent packages.
No matter, with Git contributors can always see what changes were made in which files, by whom and when.

# Viewing commit history
There are multiple ways to see a repo's commit history, but directly through GitHub may be the best approach.
Click "Commits" to go to a list of commits that can be browsed.
Under each commit there are links to see changes or more.

# File types
Git and GitHub were built around plain text files.
Git identifies any change you make in any text file in a repo, and you can view this as a deletion and addition in your commit history.
If the focus on text files seems very limiting, remember that all scripts (R, Python, Matlab) and source code (C++, Fortran) are simply text files.
Most data files are text files as well, for example, csv files are just plain text files with a comma used to separate entries.
So Git and GitHub work very well with these types of files.
The software will detect changes in other file types that we might call "binary", including graphics or executable files, but cannot identify specific changes.
There is no way around this, and it doesn't usually cause problems.
Excel files are also tricky, because Git only sees a change, but cannot identify the particular cell that was changed or how.
This is a reason to try to use csv or other text files for data.
Other advantages include file size and easy of use in R etc.
Disadvantages include a lack of formatting and slightly more difficulty in editing.

# Editing files through a browser
Most file edits are done locally, using whatever software you prefer, e.g., Notepad++ for Python scripts and Excel for csv files.
But by clicking the pen or pencil button at the top right on GitHub pages that display file contents, it is possible to edit files directly in GitHub through your browser.
