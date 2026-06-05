# What is Git Repository and how we can use it
A Git repository is a virtual storage space for your project. It allows you to preserve many versions of your code that you can access, alter, and update as required. It resembles the image below:

<img width="1000" height="372" alt="image" src="https://github.com/user-attachments/assets/1ffa2c78-c7f0-4f35-8592-9d41ebdee9cd" />

First, you'll notice it's a liner graphic with branches. Each **branch** represents a version of the project at the time and point it was constructed. The purpose is to maintain a distinct feature/task without affecting the primary project, which is the **main** branch. When you've finished structuring it, you may merge it into the main branch. Working with branches allows you to work on several features/tasks at the same time. 

# How to install Git

You can download Git by using the instrunctions from [here](https://git-scm.com/install/windows).

# How to initialize a new Git repository

Navigate through the file directories and discover the path to the folder where you want to save your project. Then launch the Command Prompt using that path. You can do it with two ways:

- **First Way**:
  Navigate to the target directory by copying its path and executing `cd <path>`, such as `cd /path/to/your/existing/code`. **!IMPORTANT!**: Verify that the path already includes the Command Prompt location, then append the remaining directory path needed to reach the target folder.
- **Second Way**:
  Open the folder in File Explorer and click the address bar displaying the folder path. Replace the existing text with `cmd` and press Enter. This will open Command Prompt with the current directory set to the selected folder. Example:
 1. <img width="1903" height="158" alt="image" src="https://github.com/user-attachments/assets/7d4c6100-4fb8-477f-81a9-c1757cb50cd1" />
 2. <img width="1902" height="155" alt="image" src="https://github.com/user-attachments/assets/9b09d055-878c-402c-8554-7d71ac1b21aa" />
 3. <img width="1900" height="158" alt="image" src="https://github.com/user-attachments/assets/0dd4bf5f-e0ca-439f-949e-2cc635a22fb7" />

 Once completing the previous step, you can initialize your first Git repository by executing the following command:
 ```
 git init
 ```
# How to clone an existing Git repository

If a Git repository for the project has already been initialized and hosted by another contributor, you should clone the existing repository. To accomplish this, follow the steps to open Command Prompt in the directory where the project will be stored, then run the following command:
```
git clone <repository url>
```

# How to create a Feature Branch

The appropriate practice to ensure your changes do not affect the main branch, create a dedicated branch for your work by running the following command:

```
git branch <branch name>
```

# How to work in a Feature Branch

This section focuses on the recommended workflow for working in a feature branch that will later be merged into the main branch. Steps marked with `*` are required when multiple contributors are working on the same feature branch; otherwise, they can be omitted.

- `*` Check if other contributers have made any changes in the feature branch, such as altering existing files or adding files.
  ```
  git pull origin <branch name>
  ```
- `*` After pulling changes you may need to resolve conflicts. **Conflicts** occured when two or more contributors have changed the same lines in a file, or if a file has been deleted while another contributor was modifying it. In these cases, Git cannot automatically determine what is correct.
- Implement your changes. Your changes at the moment will be locally and will not impact the feature branch.
- Check which files have been changed before committing. **Commit** is the process of updating the branch. The bellow command will give list of changes compared the current version of the feature branch before them.
  ```
  git status
  git diff
  ```
- Stage the relevant files that you want to commit. **Stage** is a status of a change which is ready for commit. Here is some ways to do it.
  - To commit everything:
    ```
    git add .
    ```
  - To commit a specific file:
    ```
    git add <file>
    ```
- Commit changes with the following commands.
    ```
    git commit -m "Appropriate message that descripe the purpose of the major changes."
    ```
- Update the branch to the remote repository.
  ```
  git push origin <branch name>
  ```
- When your task has been finished and all the changes has been pushed to the feature branch, it is ready to be merged with the main branch.
    - First pull changes that may have happened to the main branch.
        ```
        git pull origin main
        ```
    - Resolve conflicts that may occure.
    - Once you pushed the resolve of the conflicts, the feature branch it is ready to merged with main.
        ```
        git merge origin/main
        ```
- Since it is merged with main branch, you can delete the branch
  ```
  git push origin --delete <branch name>
  ```

# Special cases

- If you need to switch to a different branch.
  ```
  git switch <branch name>
  ```
- If you are not ready to push changes you can stash them and revive them when it is needed.
    - Stash all modified code
      ```
      git stash push -m "What is the code about"
      ```
  - If you want to stash also files that just being created you should use this command instead:
    
      ```
      git stash -u
      ```
  - When you want to apply the stashed code:
      - First, check the list of you stashed code:
        ```
        git stash list
        ```
        Responce must be:
        ```
        stash@{0}: On <branch name>: What is the code about
        ```
    - Then apply the one you wanted by executing the command:
      ```
      git stash apply stash@{0}
      ```
- If accidentally commit changes that you want to revive and clear, you should follow this commands:
  ```
  git reset --soft HEAD~1
  ```
  Then you can stash the code if you need it for something else and then
  ```
  git push --force
  ```

 



   
