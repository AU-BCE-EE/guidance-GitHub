# GitHub-guidance
Guidance for use of AU-BCE-EE account for members

# Maintainer
Sasha D. Hafner.

# Getting help
AU-BCE-EE members can always get help by sending a message to the "admin" team or any member by email: <https://github.com/orgs/AU-BCE-EE/teams/admin>.
Email [Sasha](mailto:sasha.hafner@bce.au.dk) or other team members or send a notification to the admin team by tagging ("mentioning") `@AU-BCE-EE/Admin` in any issue or discussion.

# Members
Current (7 December 2022) members of this account are listed below.
You can add any member to a repo using their user name, or add everyone by adding the team "members".

| Name                   | User name       |
|--------                |-----------      |
| Johanna Pedersen       | JohannaPedersen |
| Jesper Nørlem Kamp     | J-Kamp          |
| Frederik Dalby         | fdalby          |
| Yolanda Lemes Perschke | YoLemes         |
| Anders Feilberg        | afeilberg       |
| Marcel Buehler         | mabuehler       |
| Anna Holm Støckler     | Stoeckler       |
| Anders Peter Adamsen   | anders-adamsen  |
| Sasha D. Hafner        | sashahafner     |

You can tag any member in an issue, discussion, or comment with their user name, e.g., `@sashahafner`, or all members using `@AU-BCE-EE/members`.

# Creating a new repo
## Repo name
Our current convention is `Lastname-year-topic`, using the last name of the first author or main contributor and the year that the work was released. 
For example: [Pedersen-2022-dynamic-chambers](https://github.com/AU-BCE-EE/Pedersen-2022-dynamic-chambers).
You can always change the name later (see section on this topic below).

## Repo access
New repos should generally be created as *private*, and then shared with the public by changing to *public* later (if appropriate--not all repos will ultimately be made public).
AU-BCE-EE members only have access to public AU-BCE-EE repos or repos they have been granted access to. 
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

To grant someone access, click "Settings" at the top right of a repo page, and then "Access":

![image](https://user-images.githubusercontent.com/35272876/206227003-3fdc3dd5-641d-4fcd-845f-54e0d67888b3.png)

## File organization
Development of templates (or at least more detailed guidelines) is an important task that many of us members will need to contribute to in the coming months.
For now, consider using the [R-template repo](https://github.com/sashahafner/R-template) for any R-based project. 
While it might show a different approach than what you are used to, this structure seems to work well.
You can actually create a new repo directly from it with the "Use this template" button at the top right:

![image](https://user-images.githubusercontent.com/35272876/199021638-e1ac10ec-265a-41b4-a9c0-c5ad2017ccbb.png)

See the [README.md file](https://github.com/sashahafner/R-template/blob/main/README.md) for more information.

For sharing datasets, you can find an example structure in the [BMP-kinetics-paper-2022 repo](https://github.com/sashahafner/BMP-kinetics-paper-2022).
Text files are probably best (comma-delimited, or "csv" are convenient) and variables should be defined, e.g., in README.md.

## README file
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

You can add your AU email address at the end of <https://au.dk/> to get a short link to your AU PURE page.

Public repos should typically include a description of the repo contents, perhaps installation instructions, and maybe details on software required for use of repo contents. 
Here are some examples:

* <https://github.com/AU-BCE-EE/Hafner-2023-bls-wt-comp>
* <https://github.com/AU-BCE-EE/STM-applications>
* <https://github.com/sashahafner/BMP-kinetics-paper-2022/blob/main/README.md>

## Ignoring some files
It is common to include a .gitignore file in your repo to make sure Git ignores certain files.
For example, R may create an .Rhistory or .RData file automatically.
Depending on the program, sometimes a temporary backup file is created every time a file is opened. 
Enter these files names or extensions in a text file called .gitignore in your repo to make sure they are ignored when you add or push files.
You can find quite comprehensive templates to use as a starting point at this handy repo: <https://github.com/github/gitignore>.
See [here](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files) for more information on this topic.

# Issues and Discussion
Use GitHub issues through the "Issues" page for each repo to document and discuss any type of problem related to a repo you contribute to.
The basic idea (remember the code development roots of GitHub) is that an issue is identified, documented, and progress on addressing it is documented all under an issue.
You can tag contributors with "@", other issues with "#", and commits with the hash. 
Visibility of issues follows the repo in general but **it is good practice to think of discussion under issues as public**.
Why use GitHub Issues when you can just send a message by email or Teams?
Here are some reasons:

* Issues don't disappear or get lost, so you can add an issue and come back to it months later
* Issues provide a record of discussion and decisions, so repo creators can remember (and anyone can understand) why something was done a particular way 
* Tasks can be assigned to particular people 

GitHub has something called "Discussions" which is similar to Issues but more for topics that don't really describe problems that need to be addressed.
Discussions need to be turned on for each repo for use.

# Changing a repo name (moving a repo)
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

To change the name of your local folder that stores your repo files (not necessary, but probably smart), the easiest option seems to be to simply delete the local directory used by Git and clone the repo from GitHub again.

# Removing all traces of a file (purging)
Sometimes we make a mistake and include a file with sensitive information.
Even if it is removed in a following commit, the file can be found within the commit history.
Follow the instructions here to completely remove it: <https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository>.
If it doesn't make sense, ask Sasha or someone else running Linux to do this, then delete your local repo and clone from GitHub again.

# Problems in using GitHub Desktop
On Windows, it may be necessary to run GitHub as an administrator to avoid problems accessing or editing files.

1. Find the location of the file that runs GitHub Desktop (Windows key, GitHub, right-click, open location)
2. Right-click on file, select Properties
3. Select Advanced then check "Run as administrator"

More info here <https://www.windowscentral.com/how-set-apps-always-run-administrator-windows-10> and elsewhere online.

See [issue #2](https://github.com/AU-BCE-EE/GitHub-guidance/issues/2) for discussion.
