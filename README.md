# icaps2025.github.io

Website for the ICAPS 2025 conference held in Melbourne, Australia - November 9-14, 2025.

This site is published via a GH Action workflow to the following GH-pages: 

https://icaps25.github.io/

## Instructions for submitting updates

### Clone the ICAPS2024 repository and set up your local repository ###
1. Sign up for Github
2. Go to https://github.com/icaps2025/icaps2025.github.io and click the 'Fork' button in the upper right.  This should create and bring you to your own copy of the ICAPS website repository.
3. Use git to clone your repository. After successfully clonning the repository you should end up with a directory called `icaps2025.github.io`. This directory will be refered to as *website root*.

### Set up a remote tracking branch ###
After you've cloned the ICAPS on GitHub and set it up on your local machine, you should run the following command from the *website root* to add a remote repository for tracking changes to the main site:
 ```
$ git remote add icaps git@github.com:icaps2025/icaps2025.github.io.git
```
You only need to do this once for your local repository.

### Branch to make your edits ###
Use git-fetch to update the remote repository, and then create a new branch for the pull request you plan to make:
```
$ git fetch icaps
$ git checkout -b <branch-name> icaps/master
```
Edit your files normally.

If you add a new file or make some edits to existing files, remember to add it with `git add`.  Commit your changes with `git commit`,  and push it back to GitHub with `git push`:
```
$ git add <path-to-new-file>
$ git status // optional step to verify what exactly is going to be committed
$ git commit -am <useful but terse change description>
$ git push origin
```
You should repeat this part of the procedure for each new pull request.

## Testing changes
The site is built with [HUGO](https://gohugo.io) framework for automated generation of static web content.
If you have [hugo installed](https://gohugo.io/getting-started/installing) on your system, you can test your changes by running
`hugo server` in the *website root*.
This will start a webserver on http://localhost:1313.

### Creating your pull request ###
Use https://github.com/icaps2025/icaps2025.github.io/pulls to create a "Pull request", which will notify us that your changes are ready to apply, and we'll log on to merge them into the main site.

The website maintainers will be notified and (hopefully) approve the changes to the site, at which point they'll go live.

If you have future edits to make, you can restart the process at "[Branch to Make your Edits](https://github.com/icaps2025/icaps2025.github.io#branch-to-make-your-edits)"

## Development Framework New ICAPS web: Hugo + Deployment to GH-pages via GH Actions

[This information](deployment.md) is useful for those setting up a new webpage for future ICAPS iterations.

