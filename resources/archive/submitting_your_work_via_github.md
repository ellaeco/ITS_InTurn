# Submitting your work via Github
**[Home](../README.md)** 
___

As software professionals, Git :tm: and GitHub :tm: are tools that you will use every day. We will be using GitHub to submit your work for the program. Git is a version control system that allows you to track changes to your code. GitHub is a web-based hosting service that enables collaborative development of software projects. We use both extensively in the program.

# How to Submit Your Work

We will be using github to submit and review most of our work. 

## Setting your Github user 

When you begin a coding session, you will want to use the commands to log yourself and your pair in. 

To set your github user name and email address **globally:**
```bash
git config --global user.name ""
git config --global user.email "< your email>"
``` 

To set your github user name and email address **locally:**
```bash
# From within the root directory of your local repository:
git config --local user.name ""
git config --local user.email "< your email>"
```

##  Submission Workflow

When submitting work, you will need to create a new branch ```git checkout -b username_reflection``` and push it to github. It is important that you use meaningful names for your branches, as well as meaningful commit messages. (This is an exercise in communication, after all.)

### Working solo

When submitting assignments/reflections solo, use the following format:

```git checkout -b username_name_of_assignment```

### Working with a pair
When working with a pair it is slightly different. You can attribute a commit to more than one author by adding one or more Co-authored-by trailers to the commit's message. [Co-authored commits are visible on GitHub](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors).

```bash

0. Use the commands to set your github user names for log. 

1. Create a folder for you and your pair on the Desktop and clone the repository:

  ```shell
  git clone REPOSITORY_PATH
  ```

2. Use the following command to checkout a new branch with the proper naming convention.

  ```shell
  `git checkout -b pair-githubuser1,githubuser2`
  ```

3. Complete your challenge. Commit early and often with meaningful commit messages.

  ```shell
  git add filename
  git commit -m "ADD: test code for featureX"
  ```

4. When you have a completed challenge, push your branch to github

  ```shell
  git push -u origin pair-githubuser1,githubuser2
  ```

5.  Go to github and submit a pull request to main from your branch.  **DO NOT MERGE THE REQUEST INTO MAIN.**

## Challenge Review and Refactor Workflow

When completing a challenge review, you will need to get the existing code from a branch on github so the workflow is slightly different.


1.  If you don't already have a local copy of the repository, clone the repository into your local repository

  ```shell
  git clone REPOSITORY_PATH
  ```

  If you do already have a local copy of the repository, make sure the main branch is up to date.

  ```shell
  git checkout main
  git pull origin main
  ```

2. You now need to checkout the branch you are reviewing. This branch is available to checkout even if you don't see it in the list of branches (you may need to look on github to see the name).

  ```shell
  git checkout BRANCH_NAME
  ```

3. From this branch, create a new branch for your review and refactor. Use this naming format:

  ```shell
  git checkout -b refactor-githubuser1,githubuser2
  ```

4. Complete your challenge. Commit early and often with meaningful commit messages.

  ```shell
  git add filename
  git commit -m "ADD: test code"
  ```

5. When you have a completed challenge, push your branch to github

  ```shell
  git push origin refactor-githubuser1,githubuser2
  ```

6. Go to github and submit a pull request to the branch you are reviewing (`pair-githubuser1,githubuser2`) from your branch (`refactor-githubuser1,githubuser2`).  **DO NOT MERGE THE REQUEST.**
