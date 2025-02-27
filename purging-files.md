# Removing all traces of a file (purging)

Sometimes we make a mistake and include a file with sensitive information, or one that is bigger than the maximum allowed by GitHub.
Even if it is removed in a following commit, the file can be found within the commit history, and so more effort is needed to completely remove it.
Follow the instructions here to completely remove it: <https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository>.
If it doesn't make sense, ask Sasha or someone else running Linux to do this, then delete your local repo and clone from GitHub again.

Note to whoever does the work: you may need a newer version of git-filter-repo than what is available in the normal channels.
It is easiest to just download the Python script itself (git-filter-repo, not no extension) from <https://github.com/newren/git-filter-repo> and put in `$PATH` (e.g., "/usr/bin").


