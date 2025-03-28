# Using git at the command line
Git software is actually pretty easy to use on the command line, with a couple exceptions, including merge conflicts.
Why might you do it instead of using GitHub Desktop?
It can be faster (type a few lines instead of a lot of mouse clicks and typing) and eliminates the need to install more software.
Command-line operations can be really powerful and quick on all operating systems, so git can be a good way to get started. 
Plus, you can impress coworkers by regularly doing work at the command line!

# A demo
We use git like this.
First, open up a command-line interface and browse to your repo directory.
On Windows, Power Shell is the interface of choice.
Here I found it with windows key + typing power she.

![image](https://github.com/user-attachments/assets/c0d6b83d-3164-485b-af15-f3ebff89f457)

Then I browse into the directory that contains all the repositories I have on GitHub with `cd`, and list all the subdirectories with `ls`.

![image](https://github.com/user-attachments/assets/7a345936-2740-4391-b9c2-ff7a31799a92)

I am going to work on some course material, so I'll go into the appropriate directory.
The whole time, I am using the Tab key for autocompletion--it saves a lot of time.
So I typed `cd cour` and then hit Tab once or twice to actually get `cd .\course-comp-alg-2025\`. 
Super fast.

## 0. Check
We should check the current local repo status with `git status`.
That will tell us if we have changes that need to be sorted out before pulling.
![image](https://github.com/user-attachments/assets/0d1a21c7-dc8b-4b2e-9418-26e63beecab9)

We actually do, and I don't want these new files.
We could get rid of them in git, but we can also just delete them in any way used for any other file.
I will use `git clean . -f` here.
Now `status` shows this:

![image](https://github.com/user-attachments/assets/a2aeba35-6ecb-4c5f-ae70-ee9c9a78bc15)

## 1. Pull
We could do `git fetch` then again `git status` before `git pull` but skipping the first two steps is almost always OK.
So let's try it.

![image](https://github.com/user-attachments/assets/9684bb00-270d-4d34-bd19-18779b1218db)

Git tells us we have two new files now.

## 2. Work
To make some changes, I am going to open the local repo in Windows File Explorer.
Yes, you could find and click on a shortcut, but the quickest option is to type this--remembering autocomplete!

![image](https://github.com/user-attachments/assets/3fa76a3c-e52d-46bf-a48c-b7482d508de2)

From Explorer, you can open the file however you prefer.
I have opened one of the files in a text editor and fixed some of the text, and saved it.

## 3. Add and commit
Before commiting, let's see what git stays with `git status`.

![image](https://github.com/user-attachments/assets/835582b4-d450-4507-b4b8-7e8b88b5a6b4)

It found my change (of course) and gives me some tips on the next step.
We can add all new files and changes with `git add .` or type the name of the specific file we want to add, e.g., `git add .\09_ivp\exercise_ivp.Rmd`.
Remember to use Tab for autocomplete!
I will use the first option.

Then we check, to make sure everything looks OK, and finally commit, using the `-m` option to directly add a short commit message within quotes.
![image](https://github.com/user-attachments/assets/9870b1ef-a9b8-4303-b3a1-c83469c048d5)

## 4. Push
Finally, push to the remote repo with `git push`. 
And that's it!
Now collaborators can start at step 1 above.

![image](https://github.com/user-attachments/assets/99dcb263-8402-44d2-bd72-4019ea96ae6a)

# Other tasks
* Cloning a repo
* Merge issues
