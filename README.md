# Git Simple Lab --- Main & Dev Branch + Pull Request Workflow

This lab teaches you how to work with two branches (`main` and `dev`),
push changes to `dev`, and create a Pull Request (PR) to merge into
`main`.

------------------------------------------------------------------------

## Prerequisites

-   Git installed\
-   GitHub account\
-   A new or existing GitHub repository

------------------------------------------------------------------------

## 1. Clone the repository

``` bash
git clone git@github.com:YOUR-USER/YOUR-REPO.git
cd YOUR-REPO
```

------------------------------------------------------------------------

## 2. Create `dev` branch (if not created yet)

``` bash
git switch -c dev
git push -u origin dev
```

------------------------------------------------------------------------

## 3. Set branch protection (GitHub UI)

Go to your repository → **Settings** → **Branches** → **Branch
protection rules** →\
Add a rule for **main**:

-   Require a pull request before merging\
-   Require status checks (optional)\
-   Prevent direct pushes (optional)

------------------------------------------------------------------------

## 4. Workflow: Make changes in `dev` branch

### Step 1 --- Switch to dev

``` bash
git switch dev
```

### Step 2 --- Make changes

``` bash
echo "New feature" >> feature.txt
```

### Step 3 --- Stage & commit

``` bash
git add .
git commit -m "Add new feature"
```

### Step 4 --- Push to dev

``` bash
git push
```

------------------------------------------------------------------------

## 5. Create Pull Request (from dev → main)

1.  Go to GitHub repository\
2.  Click **Compare & Pull Request**\
3.  Select:
    -   base: main\
    -   compare: dev\
4.  Write title + description\
5.  Click **Create Pull Request**

------------------------------------------------------------------------

## 6. Merge the Pull Request

After review:

-   Click **Merge Pull Request**
-   Click **Confirm merge**

------------------------------------------------------------------------

## 7. Sync your local main branch

``` bash
git switch main
git pull
```

------------------------------------------------------------------------

## 8. Optional: Delete dev branch locally and remotely

``` bash
git branch -d dev
git push origin --delete dev
```

------------------------------------------------------------------------

## 9. Essential Git Commands (Cheat Sheet)

### Branch

``` bash
git branch
git branch name
git switch name
git switch -c new-branch
```

### Staging & Commit

``` bash
git add .
git commit -m "message"
```

### Push

``` bash
git push
git push -u origin branch-name
```

### Update local repo

``` bash
git pull
git fetch --all
```

### Delete branches

``` bash
git branch -d branch
git push origin --delete branch
```
