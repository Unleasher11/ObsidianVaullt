#example 
## `git pull`

1. Basic `git pull`:
   - Example 1: Run `git pull` in your local repository to fetch changes from the remote repository and merge them into your current branch. This updates your local branch with the latest changes from the remote repository.
   - Example 2: Suppose you are working on a team project, and your teammate has made some updates. Run `git pull` to synchronize your local branch with the remote repository and incorporate those changes into your working directory.
   - Example 3: If you have multiple branches in your local repository, running `git pull` while on a specific branch will fetch changes from the remote repository for that particular branch and merge them into your local branch.

2. `git pull` with remote branch:
   - Example 1: Fetch changes from a specific remote branch and merge them into the current local branch: `git pull origin branch_name`. This updates your current branch with the latest changes from the specified remote branch.
   - Example 2: Suppose you want to update your local `main` branch with changes from the remote `develop` branch. Run `git pull origin develop` while on the `main` branch to fetch the latest changes and merge them into your local `main` branch.
   - Example 3: Pull changes from a remote branch and create a new local branch: `git pull origin branch_name:new_branch_name`. This fetches changes from the remote branch and creates a new local branch with the specified name, incorporating the pulled changes.

3. `git pull` with rebase:
   - Example 1: Perform a `git pull` with a rebase to incorporate remote changes while maintaining a linear commit history: `git pull --rebase`. This applies your local commits on top of the fetched changes, resulting in a cleaner commit history without unnecessary merge commits.
   - Example 2: Pull changes from the remote repository and automatically perform a rebase: `git pull --rebase origin branch_name`. This fetches changes from the remote branch and applies your local commits on top of them, eliminating potential conflicts and keeping a linear history.
   - Example 3: Suppose you have local commits that you want to apply on top of the fetched changes. Use `git pull --rebase` to fetch changes from the remote repository and rebase your local commits on top of them, resulting in an updated branch with a linear commit history.