# Technical | DevOps | Pull Requests

## Introduction

This document explains process of creating branch for implementing your task/bug and submiting solution in a form of Pull Request

### Work with Pull Request
---

#### Branch overview

```bash
# List branches
git branch
git branch -a

# List latest remote changes
git log -2

# List local changes
git status
```

#### Create a task/bug branch

```bash
# Make sure that you are in the right development branch
git checkout dev

# Pull the latest changes
git pull

# Confirm that you are on the righ branch and there are no changes
git status

# Create working branch as exmaple below, where NNNN is the corresponding issue number
git checkout -b feature-NNNN/task-NNNN/smal-description
```

#### Make changes to the branch and verify they are present with 

```bash
git status
```

#### Stage and commit changes

```bash
git add .
git commit -m "#NNNN- Description"
```
This will connect commit to the work item

#### Push the branch you are working on

```bash
# This will push to the original (The branch that you ran git branch -b from) branch 
git push -u feature-NNNN/task-NNNN/smal-description
```
This has to be done only first time when using **git push** afterwards simple ```git push``` is enough

#### Create Pull Request

Follow description to create Pull Request in your DevOps tool of choice. Some examples:

[Azure DevOps](https://learn.microsoft.com/en-us/azure/devops/repos/git/about-pull-requests?view=azure-devops)
[GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
[GitLab](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)

#### Update local branch

After going to review and approval process working branch ```feature-NNNN/task-NNNN/smal-description``` will be merged to ```dev``` branch. Local branch has to be updated accordingly:

```bash
git checkout dev
git pull
```

#### Delete orphan branches

It is best to delete branches that have been sucessfully merged

```bash
# Delete fully merged local branch
git branch -d feature-NNNN/task-NNNN/smal-description

# Delete fully merged remote branch
git branch -dr origin/feature-NNNN/task-NNNN/smal-description

```