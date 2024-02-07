# Repository creation
This guide is on creating a new repo.
It is meant to be a general guide.
For paper repos in particular, be sure to check out the [paper-repos guide](https://github.com/AU-BCE-EE/GitHub-guidance/blob/main/paper-repos.md).

# Getting started
Create a new repo by browing to [AU-BCE-EE repositories](https://github.com/orgs/AU-BCE-EE/repositories) and clicking "New repository".
You can start from scratch or else use one of the available templates.

# Repo name
Our current convention is `Lastname-year-topic`, using the last name of the first author or main contributor and the year that the work was released. 
For example: [Pedersen-2022-dynamic-chambers](https://github.com/AU-BCE-EE/Pedersen-2022-dynamic-chambers).
You can always change the name later (see section on this topic below).

# Repo access
New repos should generally be created as *private*, and then shared with the public by changing to *public* later (if appropriate--not all repos will ultimately be made public).
AU-BCE-EE members only have access to public AU-BCE-EE repos or repos they have been granted access to. 
(This is set by the admin team, and could be changed so that all members have access to all repos. But we opted for this safer approach to minimize the risk of accidentally sharing private repo contents.)
AU-BCE-EE owners have write (really admin) access to all of this account's repos.
Regardless of whether you are working with owners or other members, it makes sense to explicitly add repo collaborators.
See the table below for more information.

| Person status      | Read access         | Write access|
|---------------     |-------------        |-------------|
| AU-BCE-EE *owner*  | Always              | Always      |
| AU-BCE-EE *member* | If repo is *public* or if user is added or if member created repo | If added or if member created repo   |
| Everyone else      | If repo is *public* or if user is added | If added    |

Any AU-BCE-EE member can create new repos and give themselves and others access (read or write). 
In the table above "added" means a user has been added as a collaborator to a repo by an AU-BCE-EE owner (reach the owners through the team name [@AU-BCE-EE/admin](https://github.com/orgs/AU-BCE-EE/teams/admin)) or anyone with admin access to the repo (e.g., any member who creates a repo).
(Note that this default behavior of no access to private repos by members can be changed.
We (owners) have taken a conservative approach for now at least.)

To grant someone access, click "Settings" at the top right of a repo page, then "Collaborators and teams", click the green "Add people" (or teams) button the right, and finally search for people with the user names above or email addresses:

![image](https://user-images.githubusercontent.com/35272876/206227003-3fdc3dd5-641d-4fcd-845f-54e0d67888b3.png)

# File organization
Development of templates (or at least more detailed guidelines) is an important task that many of us members will need to contribute to in the coming months.
For now, consider using the [R-template repo](https://github.com/sashahafner/R-template) for any R-based project. 
See the [paper-repos guide](https://github.com/AU-BCE-EE/GitHub-guidance/blob/main/paper-repos.md) and [paper repo template](https://github.com/AU-BCE-EE/template-paper) for some suggestions for paper repos.
While it might show a different approach than what you are used to, this structure seems to work well.
You can actually create a new repo directly from it with the "Use this template" button at the top right:

![image](https://user-images.githubusercontent.com/35272876/199021638-e1ac10ec-265a-41b4-a9c0-c5ad2017ccbb.png)

See the [README.md file](https://github.com/sashahafner/R-template/blob/main/README.md) for more information.

For sharing datasets, you can find an example structure in the [BMP-kinetics-paper-2022 repo](https://github.com/sashahafner/BMP-kinetics-paper-2022).
Text files are probably best (comma-delimited, or "csv" are convenient) and variables should be defined, e.g., in README.md.

# README file
Each repo should have a file named README.md or similar for explaining the repo to users. 
For private repos (see Repo access section above), the file should have enough information for AU-BCE-EE admin to figure out what who is responsible for the repo and what it is used for.
For public repos, more detail is typically needed. 
In either case, add a Maintainer section with something like this:

```
# Maintainer
Sasha D. Hafner.
Contact information here: <https://au.dk/sasha.hafner@bce>.
```

On GitHub, that will show up like this:

![image](https://user-images.githubusercontent.com/35272876/229759816-82f71b3d-1976-4ab5-81a8-c0979beaba18.png)

Note that it is part of your AU email address at the end of <https://au.dk/> that gives you the correct link, so if you use initials it would be e.g., <https://au.dk/jk@bce>.

Public repos should typically include a description of the repo contents, perhaps installation instructions, and maybe details on software required for use of repo contents. For repos that have data analysis for a paper, it is a good idea to include details on exactly where paper results came from (it is easy to forget). 
Here are some examples:

* <https://github.com/AU-BCE-EE/Hafner-2023-bls-wt-comp>
* <https://github.com/AU-BCE-EE/STM-applications>
* <https://github.com/sashahafner/BMP-kinetics-paper-2022/blob/main/README.md>

Also see the guidance for paper repos: <https://github.com/AU-BCE-EE/GitHub-guidance/blob/main/paper-repos.md>

# Ignoring some files
It is common to include a .gitignore file in your repo to make sure Git ignores certain files.
For example, R may create an .Rhistory or .RData file automatically.
Depending on the program, sometimes a temporary backup file is created every time a file is opened. 
Enter these files names or extensions in a text file called .gitignore in your repo to make sure they are ignored when you add or push files.
You can find quite comprehensive templates to use as a starting point at this handy repo: <https://github.com/github/gitignore>.
See [here](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files) for more information on this topic.

