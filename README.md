# GitHub-guidance
Guidance for AU-BCE-EE members

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


