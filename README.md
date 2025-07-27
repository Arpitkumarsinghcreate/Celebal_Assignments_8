# Celebal_Assignments_8
Celebal_Technologies




✅ What commands would you use to stage all the changes and commit them with a meaningful commit message?
To stage all changes made to multiple files in your Git repository, you would use the git add . command. This stages all modified, new, and deleted files in the current directory and its subdirectories. Once all changes are staged, you can commit them using the git commit -m "Your meaningful commit message" command. The commit message should be clear and descriptive, explaining the purpose of the changes made, such as fixing a bug, adding a feature, or updating documentation.

❌ You have committed changes to a wrong branch. How would you move these commits to the correct branch?
If you have accidentally committed changes to the wrong branch, you can safely move them to the correct one by first creating a new branch from the current (incorrect) branch using git branch correct-branch-name. This saves the current state. Then, switch to the intended branch using git switch main (or whichever branch is correct). From there, you can apply the previous commit(s) using git cherry-pick <commit-hash> to selectively move changes. Finally, if needed, go back to the wrong branch and remove the commit(s) using git reset --hard HEAD~1 to keep the history clean.

🌿 You want to create a new branch, make changes, and push the branch to the remote repository. Outline the steps you would take to create a new branch, commit changes, and push the branch to GitHub.
To begin working on a new feature or task, start by creating a new branch using the command git checkout -b feature-branch-name. This both creates and switches to the new branch. Make your changes to the code, and once satisfied, stage them with git add . and commit them using git commit -m "Added feature XYZ". After committing, push your branch to the remote repository using git push origin feature-branch-name. This ensures your work is backed up on GitHub and can be shared or reviewed by others.

💡 You want to contribute to an open-source project hosted on GitHub. What are the steps you would follow to fork the repository, make changes, create a pull request, and collaborate with the original project?
To contribute to an open-source project on GitHub, first fork the repository to your own GitHub account using the "Fork" button on the project’s page. Then, clone your fork to your local system using git clone https://github.com/your-username/repo-name.git. Navigate into the project directory and create a new branch with git checkout -b feature-name where you’ll make your changes. After making and testing your changes, stage and commit them using git add . and git commit -m "Describe your contribution", followed by git push origin feature-name to push the branch to your fork. Then, go to your GitHub repository and open a pull request to the original project’s main branch. Collaborate with maintainers by responding to any requested changes until your contribution is accepted.

⚔️ You are working on a team project, and there are conflicts between your branch and the main branch. How would you resolve these merge conflicts? Provide the necessary commands and steps.
To resolve merge conflicts between your branch and the main branch, first ensure your local main branch is up to date using git fetch origin. Then, switch to your feature branch using git checkout your-branch-name and merge the updated main branch into it using git merge origin/main. If conflicts arise, Git will highlight the conflicting files and insert markers (<<<<<<<, =======, >>>>>>>) showing the differences. Open the files, resolve the conflicts manually by choosing or combining the correct changes, and then remove the conflict markers. After resolving all conflicts, stage the fixed files using git add <filename> and commit the merge with git commit. This successfully integrates the changes from main into your branch while preserving both sets of contributions.

🌱 You want to create a feature branch based on the latest changes in the main branch. What commands would you use to create a new branch and automatically switch to it, ensuring it's up to date with the latest changes from the main branch?
To create a new feature branch based on the latest main branch, first ensure you are on the main branch by running git checkout main, and then update it with the latest changes from the remote using git pull origin main. After that, you can create and switch to a new branch using git checkout -b feature-branch-name. This will ensure that your new branch starts from the latest state of the main branch, helping avoid potential merge conflicts later on.

⏪ You have made a series of commits, but you realize that a change made several commits ago is causing issues in your application. How would you revert to a specific commit, discarding all changes made after that commit?
If you discover that a specific commit from earlier in the history introduced a problem and want to discard all changes made afterward, you can use the git reset --hard <commit-hash> command. This command resets your branch to the specified commit and removes all commits that came after it in your history. Be cautious: this action also discards uncommitted changes. If you've already pushed the problematic commits to the remote, you'll need to run git push origin HEAD --force to overwrite the remote branch with the correct history. This approach is effective for rolling back to a known working state in development.

🗃️ You have accidentally deleted a file in your Git repository and committed the change. What commands would you use to restore the deleted file from the previous commit?
If you’ve accidentally deleted a file and committed the deletion, you can restore the file from the previous commit using git checkout HEAD^ -- path/to/file. This command fetches the file as it was in the commit before the most recent one. After restoring, you can stage and commit it again using git add path/to/file and git commit -m "Restored accidentally deleted file". This allows you to bring back the lost file without undoing other recent changes.


