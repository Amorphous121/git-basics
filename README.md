
# GitHub Commands

1. **[Initialize a GitHub Repository Locally](https://git-scm.com/docs/git-init)**

2. **[Configure Git Username and Email](https://git-scm.com/docs/git-config)**

3. **[Add Files to Staging Area](https://git-scm.com/docs/git-add)**

4. **[Create a Branch](https://git-scm.com/docs/git-branch)**

5. **[Change Branches](https://git-scm.com/docs/git-checkout)**

6. **[Delete a Local Branch](https://git-scm.com/docs/git-branch#_delete_branch)**

7. **[Delete a Remote Branch](https://git-scm.com/docs/git-push#_deleting_a_remote_branch)**

8. **[See Working Tree Status](https://git-scm.com/docs/git-status)**

9. **[View Git Logs](https://git-scm.com/docs/git-log)**

10. **[Create a New Branch and Checkout to It](https://git-scm.com/docs/git-checkout#_switching_branches)**

11. **[Amend the Latest Commit Message](https://git-scm.com/docs/git-commit#_amend)**

12. **[Add Files to Staging and Commit Directly](https://git-scm.com/docs/git-commit#_options)**

13. **[Revert a Commit](https://git-scm.com/docs/git-revert)**

14. **[Undo Changes Using `git reset`](https://git-scm.com/docs/git-reset)**

15. **[List Branches](https://git-scm.com/docs/git-branch)**

16. **[Switch Branch Using `git switch`](https://git-scm.com/docs/git-switch)**

17. **[Merge a Branch with Squashing Commits](https://git-scm.com/docs/git-merge#_squash)**

18. **[Squash/Rebase Commits into a Branch](https://git-scm.com/docs/git-rebase)**

19. **[Git Tags](https://git-scm.com/docs/git-tag)**



## Initialize a GitHub Repository Locally

To initialize a new GitHub repository locally, use the following command:

```bash
git init
```

[Learn more](https://git-scm.com/docs/git-init)

## Configure Git Username and Email

To add your username and email to your Git configuration, use the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

[Learn more](https://git-scm.com/docs/git-config)

## Add Files to the Staging Area

To add files to the staging area, use the following commands:

- To add a single file:

  ```bash
  git add filename
  ```

  Replace `filename` with the name of the file you want to add.

- To add all files in the current directory:

  ```bash
  git add .
  ```

  [Learn more](https://git-scm.com/docs/git-add)

## Create a Branch

To create a new branch, use the following command:

```bash
git branch branch-name
```

Replace `branch-name` with the name of the branch you want to create. This command creates a new branch from the current branch but does not switch to it.

[Learn more](https://git-scm.com/docs/git-branch)

## Change Branches

To switch to a different branch, use the following command:

```bash
git checkout branch-name
```

Replace `branch-name` with the name of the branch you want to switch to. This command changes the current working branch to the specified branch.

[Learn more](https://git-scm.com/docs/git-checkout)

## Delete a Local Branch

To delete a local branch, use the following command:

```bash
git branch -d branch-name
```

Replace `branch-name` with the name of the branch you want to delete. If the branch has not been fully merged, you can force delete it with:

```bash
git branch -D branch-name
```

[Learn more](https://git-scm.com/docs/git-branch#_delete_branch)

## Delete a Remote Branch

To delete a remote branch, use the following command:

```bash
git push origin --delete branch-name
```

Replace `branch-name` with the name of the remote branch you want to delete. This command removes the branch from the remote repository.

[Learn more](https://git-scm.com/docs/git-push#_deleting_a_remote_branch)

## See Working Tree Status

To see the status of your working tree, use the following command:

```bash
git status
```

[Learn more](https://git-scm.com/docs/git-status)

## View Git Logs

To view the commit history, use the following commands:

- For a concise, one-line-per-commit format:

  ```bash
  git log --oneline
  ```

- For the standard, detailed format:

  ```bash
  git log
  ```

[Learn more](https://git-scm.com/docs/git-log)

## Create a New Branch and Checkout to It

To create a new branch and switch to it immediately, use the following command:

```bash
git checkout -b branch-name
```

Replace `branch-name` with the name of the new branch you want to create.

[Learn more](https://git-scm.com/docs/git-checkout#_switching_branches)

## Amend the Latest Commit Message

To modify the most recent commit message, use the following command:

```bash
git commit --amend -m "New commit message"
```

Replace `"New commit message"` with the updated message you want to use.

[Learn more](https://git-scm.com/docs/git-commit#_amend)

## Add Files to Staging and Commit Directly

To add files to the staging area and commit them in a single command, use:

```bash
git commit -am "Commit message"
```

Replace `"Commit message"` with your commit message. This command stages all tracked files and commits them with the provided message.

[Learn more](https://git-scm.com/docs/git-commit#_options)

## Revert a Commit

To revert a specific commit, use the following command:

```bash
git revert commit-hash
```

Replace `commit-hash` with the hash of the commit you want to revert. This command creates a new commit that undoes the changes made by the specified commit.

[Learn more](https://git-scm.com/docs/git-revert)

## Undo Changes Using `git reset`

To undo changes using `git reset`, use the following commands:

- **Soft Reset**:

  ```bash
  git reset --soft commit-hash
  ```

- **Mixed Reset** (default):

  ```bash
  git reset commit-hash
  ```

- **Hard Reset**:

  ```bash
  git reset --hard commit-hash
  ```

[Learn more](https://git-scm.com/docs/git-reset)

## List Branches

To list branches, use the following commands:

- **List Local Branches**:

  ```bash
  git branch
  ```

- **List Remote Branches**:

  ```bash
  git branch -r
  ```

- **List All Branches (Local and Remote)**:

  ```bash
  git branch -a
  ```

[Learn more](https://git-scm.com/docs/git-branch)

## Switch Branch Using `git switch`

To switch branches using `git switch`, use:

- **Switch to an Existing Branch**:

  ```bash
  git switch branch-name
  ```

- **Create and Switch to a New Branch**:

  ```bash
  git switch -c new-branch-name
  ```

[Learn more](https://git-scm.com/docs/git-switch)

## Merge a Branch with Squashing Commits

To merge a branch and squash commits:

1. **Switch to the Target Branch**:

   ```bash
   git switch target-branch
   ```

2. **Merge the Source Branch with Squashing**:

   ```bash
   git merge --squash source-branch
   ```

3. **Commit the Squashed Changes**:

   ```bash
   git commit -m "Commit message for the squashed changes"
   ```

[Learn more](https://git-scm.com/docs/git-merge#_squash)

## Squash/Rebase Commits into a Branch

To squash/rebase commits into a branch:

1. **Switch to the Branch with Commits**:

   ```bash
   git switch branch-name
   ```

2. **Start an Interactive Rebase**:

   ```bash
   git rebase -i HEAD~n
   ```

3. **In the Interactive Rebase Editor**:

   - Change `pick` to `squash` for the commits you want to squash.
   - Save and close the editor.

4. **Edit the Commit Message**:

   - Save and close the editor.

5. **Resolve Conflicts (if any)**:

   ```bash
   git rebase --continue
   ```

   - To abort the rebase:

     ```bash
     git rebase --abort
     ```

6. **Push the Rebased Branch**:

   ```bash
   git push --force
   ```

[Learn more](https://git-scm.com/docs/git-rebase)

## Git Tags

- **Create a Lightweight Tag**:

  ```bash
  git tag tag-name
  ```

- **Create an Annotated Tag**:

  ```bash
  git tag -a tag-name -m "Tag message"
  ```

- **List All Tags**:

  ```bash
  git tag
  ```

- **Show Tag Details**:

  ```bash
  git show tag-name
  ```

- **Delete a Tag Locally**:

  ```bash
  git tag -d tag-name
  ```

- **Push a Tag to Remote**:

  ```bash
  git push origin tag-name
  ```

- **Push All Tags to Remote**:

  ```bash
  git push --tags
  ```

- **Delete a Tag from Remote**:

  ```bash
  git push origin --delete tag-name
  ```

[Learn more](https://git-scm.com/docs/git-tag)

---

Feel free to let me know if there’s anything else you need!
