#example 

## `git branch`

1. Creating a new branch:
   - Example 1: Create a new branch named "feature-branch": `git branch feature-branch`. This command creates a new branch based on the current commit, but does not switch to it immediately. You can continue working on your current branch and switch to the new branch later using `git checkout`.
   - Example 2: Suppose you're working on a project and want to create a separate branch for a specific feature. Run `git branch feature-branch` to create a new branch dedicated to implementing that feature. This keeps your changes isolated from the main branch until you're ready to merge them.
   - Example 3: If you want to create a branch from a specific commit, use `git branch feature-branch commit_hash`. This creates a new branch named "feature-branch" starting from the specified commit, identified by its unique commit hash.

2. Listing branches:
   - Example 1: List all branches in the repository: `git branch`. This command displays a list of all local branches in your repository. The currently checked-out branch is highlighted with an asterisk (*).
   - Example 2: Suppose you want to see a concise summary of the available branches. Run `git branch --list` to display a list of branch names without additional information. This is useful when working with many branches or when parsing the branch names programmatically.
   - Example 3: To view both local and remote branches, use `git branch --all`. This command shows a list of all local and remote branches, providing a comprehensive overview of the available branches in your repository.

3. Deleting a branch:
   - Example 1: Delete a branch named "feature-branch": `git branch -d feature-branch`. This command deletes the specified branch if it has been merged into the current branch. If the branch contains unmerged changes, Git will prevent you from deleting it to avoid data loss.
   - Example 2: Suppose you have completed work on a feature branch and merged it into the main branch. Run `git branch -d feature-branch` to delete the feature branch. This keeps your branch list clean and removes branches that are no longer needed.
   - Example 3: To force-delete a branch, even if it contains unmerged changes, use `git branch -D feature-branch`. Exercise caution when using the `-D` option, as it irreversibly deletes the branch and its commits.

Remember to create branches to work on new features or isolate changes, regularly list branches to keep track of your branch structure, and delete branches once they are no longer needed to maintain a tidy repository.