#example 
## `git merge`

1. Performing a basic merge:
   - Example 1: Merge the changes from a branch named "feature-branch" into the current branch: `git merge feature-branch`. This command integrates the changes made in the specified branch into the current branch, combining the commit history and incorporating the changes made in the feature branch.
   - Example 2: Suppose you have been working on a separate branch named "bug-fix" to fix a specific issue. Run `git merge bug-fix` while on the target branch (e.g., main or develop) to merge the bug fix changes into the main branch.
   - Example 3: If you are collaborating with a team and someone else has made changes on a branch called "new-feature," run `git merge new-feature` to incorporate their changes into your current branch.

2. Resolving merge conflicts:
   - Example 1: During a merge, if Git encounters conflicts between the changes made in different branches, it pauses the merge process and prompts you to resolve the conflicts manually. After resolving the conflicts, use `git add` to mark the resolved files, then run `git merge --continue` to continue with the merge process.
   - Example 2: Suppose you and another team member have made conflicting changes to the same file in separate branches. When you attempt to merge the branches, Git detects the conflicts and asks you to resolve them. Use a text editor to edit the conflicted file, then stage the resolved changes using `git add` and continue the merge process with `git merge --continue`.
   - Example 3: If you encounter merge conflicts during a merge operation, you can use `git status` to identify the conflicted files. Resolve the conflicts manually by editing the conflicting parts within the file, save the changes, and stage the resolved files using `git add`. Finally, run `git merge --continue` to complete the merge.

3. Merging with a specific strategy:
   - Example 1: Merge a branch using the "ours" merge strategy: `git merge --strategy=ours branch_name`. This strategy discards all changes from the merging branch and keeps the version from the current branch. This can be useful when you want to incorporate changes from a branch but want to override them with the current branch's version.
   - Example 2: Suppose you have a branch named "experimental" where you've made significant changes, but you want to merge them using the "theirs" merge strategy. Run `git merge --strategy=theirs experimental` to merge the changes from the "experimental" branch, favoring the changes from that branch over the current branch.
   - Example 3: If you want to use a custom merge strategy, you can specify it using the `-s` or `--strategy` flag followed by the desired strategy name. For example, `git merge -s recursive-ours branch_name` uses the "recursive-ours" merge strategy to merge the branches, favoring the current branch's version.

Remember to carefully review the changes and resolve any conflicts that arise during the merge process to ensure a successful and accurate integration of the branches.