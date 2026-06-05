# What is Git Repository and how can we use it
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

 



   
