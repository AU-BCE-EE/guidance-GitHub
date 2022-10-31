# GitHub-guidance
Guidance for use of AU-BCE-EE account for members

# Creating a new repo
## Repo name
Our current convention is `Lastname-year-topic`, using the last name of the first author or main contributor and the year that the work was released. 
For example: [Pedersen-2022-dynamic-chambers](https://github.com/AU-BCE-EE/Pedersen-2022-dynamic-chambers).
You can always change the name later (see section on this topic below).

## Repo access
New repos should generally be created as *private*, and then shared with the public by changing to *public* later.
All AU-BCE-EE members have view access to all AU-BCE-EE repositories and owners have write access.
Regardless of whether you are working with owners or other members, it probably makes sense to explicitly add repo collaborators.
See the table below for more information.

| Person status      | Read access         | Write access|
|---------------     |-------------        |-------------|
| AU-BCE-EE *owner*  | Always              | Always      |
| AU-BCE-EE *member* | Always              | If added    |
| Everyone else      | If repo is *public* | If added    |

## File organization
Development of templates (or at least more detailed guidelines) is an important task that many of us members will need to contribute to in the coming months.
For now, consider using the [R-template repo](https://github.com/sashahafner/R-template) for any R-based project. 
While it might show a different approach than what you are used to, this structure seems to work well.
You can actually create a new repo directly from it with the "Use this template" button at the top right:

![image](https://user-images.githubusercontent.com/35272876/199021638-e1ac10ec-265a-41b4-a9c0-c5ad2017ccbb.png)

See the [README.md file](https://github.com/sashahafner/R-template/blob/main/README.md) for more information.

For sharing datasets, you can find an example structure in the [BMP-kinetics-paper-2022 repo](https://github.com/sashahafner/BMP-kinetics-paper-2022).
Text files are probably best (comma-delimited, or "csv" are convenient) and variables should be defined, e.g., in README.md.

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

Apparently the Windows GitHub Desktop interface automatically updates the URL after making a change through GitHub online.
You can confirm this under the Repository menu (see Repository settings).

![image](https://user-images.githubusercontent.com/35272876/198268474-33f59ddc-42a2-47e1-a35c-96fd2bc57369.png)

To change the name of your local folder that stores your repo files (not necessary, but probably smart), the easiest option seems to be to simply clone the repo from GitHub again.


