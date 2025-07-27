# Celebal_Assignments_8
Celebal_Technologies




✅ 1. Stage All Changes and Commit with a Meaningful Message
To stage all the changes in your Git repository, including modified, added, and deleted files, you can use the git add . command, which stages everything in the current directory recursively. After staging, you can commit the changes with a meaningful message using the git commit -m "Your commit message" command. The commit message should clearly describe the purpose or nature of the changes made so that others (or your future self) can easily understand the history and context of the commit.

❌ 2. Committed Changes to the Wrong Branch — How to Move Commits to the Correct Branch
If you mistakenly commit changes to the wrong branch, you can move those commits to the correct branch by first creating a new branch from the current (incorrect) state using git branch correct-branch-name. Then, switch to the actual target branch (e.g., main) with git switch main, and use the git cherry-pick <commit-hash> command to apply the specific commits from the wrong branch. If needed, you can remove the mistaken commits from the wrong branch by switching back to it and using git reset --hard HEAD~1, replacing 1 with the number of commits you want to undo.

🌿 3. Create a New Branch, Make Changes, and Push to Remote
To work on a new feature or task, you should first create a new branch using git checkout -b branch-name, which also switches you to the new branch. After making your changes, you can stage them using git add . and commit them with git commit -m "Descriptive message". Finally, to share your branch with others or back it up, push it to the remote repository using git push origin branch-name. This workflow helps keep your work organized and separate from the main codebase.

💡 4. Contribute to an Open-Source Project via Fork, Edit, and Pull Request
To contribute to an open-source project on GitHub, start by forking the repository to your own GitHub account. Clone your fork locally using git clone, then navigate into the project folder. Create a new branch using git checkout -b feature-name to make your changes. After editing, stage and commit the changes using standard Git commands (git add . and git commit -m). Push the branch to your GitHub fork using git push origin branch-name. Finally, go to the original repository and create a pull request from your branch. Collaborate with maintainers by responding to review comments and making necessary adjustments until your changes are merged.

⚔️ 5. Resolve Merge Conflicts Between Your Branch and Main
When working in a team, merge conflicts can occur if multiple developers modify the same parts of the code. To resolve them, first ensure your local main branch is up to date using git fetch origin. Then switch to your feature branch and merge main into it using git merge origin/main. If there are conflicts, Git will mark the conflicting sections in the affected files. Open each file and manually resolve the conflicts by choosing the correct code and removing conflict markers (<<<<<<<, =======, >>>>>>>). Once resolved, stage the files with git add and finalize the merge with git commit. This process ensures your branch integrates well with the latest main code.

🌱 6. Create a Feature Branch Based on the Latest Main Branch
To create a new feature branch that includes the latest changes from the main branch, first switch to the main branch using git checkout main, and then pull the latest changes from the remote using git pull origin main. After your local main is updated, create a new branch and switch to it using git checkout -b feature-branch-name. This ensures your new branch starts with the most recent code from main, reducing the chances of merge conflicts later.

⏪ 7. Revert to a Specific Commit, Discarding All Changes Made After
If you discover that a change introduced in recent commits caused issues and you want to discard all commits after a specific point, you can use the git reset --hard <commit-hash> command. This will reset your working directory and history to that exact commit, removing all subsequent changes. If these changes have already been pushed to a remote repository, you’ll also need to use git push origin HEAD --force to overwrite the remote history. Be cautious with this, especially when collaborating, as it rewrites commit history.

🗃️ 8. Restore a Deleted File from a Previous Commit
If you accidentally deleted a file and committed the change, you can restore the file from a previous commit using the command git checkout HEAD^ -- path/to/file. This retrieves the file as it was in the previous commit. After restoring it, you can stage the file again using git add and commit it with a message like "Restored deleted file" to bring it back into your project. This method is very useful for recovering important files without reverting your entire repository.

