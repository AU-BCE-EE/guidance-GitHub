# Guidance on creating a paper repository 
In the Environmental Engineering section we now typically have a designated repo for each paper we publish.
The repo is a place to include all data, scripts, and output associated with the paper.
It allows readers or our future self access and understand the data, analysis, and results.

# Initial steps
1. Create the new repo based on [this template](https://github.com/AU-BCE-EE/template-paper.git). To do that, browse to [AU-BCE-EE repositories](https://github.com/orgs/AU-BCE-EE/repositories), click "New repository", and select "template-paper" from the list.
2. Keep the new repo private, unless you are comfortable immediately and irreversibly sharing all its contents with the world.
3. Create two issue in your new repo: 1. Finalize repo and 2. Create a release. Keep these issues open until the paper has been published and you have completed both of them.
4. Edit this README.md file, including deleting any notes to you (new repo creator).

# Repo use
Use the new paper repository as any other that you might use for data analysis.
Put data in the `data` directory, analysis scripts in the `scripts` directory, and add other directories and files as appropriate. 
See the other AU-BCE-EE templates for more detailed data analysis examples that can be copied.
See GitHub-Git-workflow document for more details.

# First and subsequent submissions
Complete these steps when you are ready to submit your paper.

1. Make sure your repo is complete before submission (except for the paper details of course).
2. Make your repo public under setttings, at the bottom ("Change repository visibility"). (If you are worried about releasing your data and code before the paper has been accepted, you might postpone this step until the paper has been accepted, but that means reviewers cannot test your repo URL and see the repo files.)
3. Include the repo URL in the paper in an appropriate location, e.g., data availability statement.
4. Create a release and give it a name like "v1". You may want to set it as a "pre-release", because the paper and therefore the underlying work has not yet been finalized. Include a description that includes something like "Associated with first submission to Journal of Great Stuff 5 Jan 2024".
5. You may want to use the URL for the release as a permanent link to this particular version of the data analysis, but it isn't necessary to do so--the main URL and the list of releases should be clear enough. This is where the description can help.

# Once the paper has been published
1. Update this README.md file with information on the paper.
2. Check, address, and close all remaining issues. (If there is important information in some issue even though it is actually resolved, you could move the relevant text to "discussions" instead.)
3. Create a new release, with a helpful description.

# If you make corrections
If you make changes to any of the files, you should create a new release and in the associated description, make it clear that the new release differs from the work presented in the paper (e.g., in the README.md file and release description).
