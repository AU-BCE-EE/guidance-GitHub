# GitHub-guidance
Guidance for AU-BCE-EE members

# Creating a new repo
## Repo access
New repos should generally be created as *private*, and then shared with the public by changing to *public* later.
All AU-BCE-EE members have view access to all AU-BCE-EE repositories and owners have write access.
Regardless of whether you are working with owners or other members, it probably makes sense to explicitly add repo collaborators.

| Person status | Read access | Write access|
|---------------|-------------|-------------|
| AU-BCE-EE owner | Always    | Always      |
| AU-BCE-EE member | Always    | If added   |
| Public        | If repo is public | If added |

# Changing a repo name
It is common to change a repo name at some point after creating it.
Repo owners can change the name of a repo through the Settings option that can be found near the top of the repo main page:

![image](https://user-images.githubusercontent.com/35272876/198266746-9840a595-e71a-4775-bd54-808b1e5f1535.png)

Although the old URLs will still work, it is safer to update URLs wherever they are used.
Your local version of Git should still look for the correct location to find repo files even after the change, but here too it is better to update the URL with this command:

```
$ git remote set-url origin NEW_URL
```

For more details see this GitHub page: <https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository>

Apparently the Windows GitHub Desktop interface automatically updates the URL after making a change through GitHub online!
You can confirm this under the Repository menu (see Repository settings).

![image](https://user-images.githubusercontent.com/35272876/198268474-33f59ddc-42a2-47e1-a35c-96fd2bc57369.png)

To change the name of your local folder that stores your repo files (not necessary, but probably smart), the easiest option seems to be to simply clone the repo from GitHub again.


