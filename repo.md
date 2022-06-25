# Git Repositories

Setting up a **local** repo, requires the following steps:

## Local Repo Setup
1. Set up the project folder, first.
2. Add needed files/folders + code
3. Initialize the repository using the git command
    ```
    git init
    ```
4. Stage your project changes
    ```
    git add .
    ```
    or if you want to stage only one file, not all changes, do the following:
    ```
    git add file_name
    ```
5. Commit your staged changes
    ```
    git commit -m "Setup my local repo"
    ```
6. This is where the **remote** repo comes in.

## Connecting to Remote Repo
1. Create the remote repo on [GitHub](https://github.com/new)
2. Copy the remote repo URL
3. Connect your remote repo to your local repo
    ```
    git remote add name_of_remote inser_url_here
    ```
    example:
    ```
    git remote add origin https://github.com/AFathi/clock.git 
    ```
4. Push to remote
    ```
    git push -u remote_name branch_name
    ```
    example:
    ```
    git push -u origin master
    ```
    
## Fetching Remote Repo (or changes)

If it's the **first time** you're downloading the repo, you shall use the following command:
```
git clone insert_url_here
```

example:
```
git clone https://github.com/AFathi/clock.git 
```

Otherwise, if your repo is already connected to remote and you would like to **update** your local repo to match remote. To do so, use the following command:

```
git pull
```

## Creating a branch
Why create a branch?
- Seperation of concerns.

How do we create a branch?

1. Create a branch
    ````
    git branch insert_branch_name
    ```
    feature example:
    ```
    git branch feature/countdown
    ```
    bug example
    ```
    git branch bug/countdown
    ```
2. Check the current branch you are on:
    ```
    git branch
    ```
3. Switch into the new branch created
    ```
    git checkout branch_name
    ```
    example
    ```
    git checkout feature/countdown
    ```

**Create and Checkout into a Branch at the same time**
```
git checkout -b branch_name
```

example:

```
git checkout -b bug/countdown
```

## Merging branches
1. Go to the parent branch (e.g. `feature/countdown`)
```
git checkout branch_name

git checkout feature/countdown
```
2. Merge the child branch (e.g. `bug/countdown`)
```
git merge branch_name

git merge bug/countdown
```

## Delete local branch
```
git branch -D branch_name

git branch -D bug/countdown
```