# Problems merging versions
What happens if you are a collaborator are working on the repo files at the same time--will there be a problem when one of you commits or pushes?
There might be, but usually there is not.
And if there is, the solution is to follow the GitHub Desktop prompts, which will guide you through a merge.

# Working on separate files
If you and a collaborator are edit different files, and your collaborator pushes first, you have a simple merge conflict.

If you are using GitHub Desktop, and try to push *your* commit, you will see a notice that pushing is not possible because of a commit in the remote repo that you do not have.
No problem, because it prompts you to fetch (download the repo history, including this new commit), then pull (download the new commit, and in this case, automatically combine it with your commit), and finally, push your merged version to the remote repo.
So that is easy.

In the command line, it is nearly as simple--just use `$ git pull --rebase`.

# Working on the same file
If you and a collaborator both make changes to the same version of a file, and your collaborator pushes changes first, you have a different merge issue.
But, if the changes were made in two different locations, following the GitHub Desktop prompts results in a merge of the two different versions, just like with two different files (see above section).
No problem.

Now, if you both make changes in the same line of the file, it is a bit more complicated.
Even so, follow the GitHub Desktop prompts, including opening the file to manually fix the conflict.
You should see some `>>>>>` and `======` symbols in the file showing the different changes.
Change the file however you want (merge, keep both, delete one as appropriate), save it, and finally finish with the GitHub Desktop prompts.

In the command line, the process is not so different, but with some more manual steps.

