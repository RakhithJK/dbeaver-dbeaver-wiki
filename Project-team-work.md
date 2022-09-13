DBeaver is fully integrated with the Git team work/version control system.
You can keep your project configuration, scripts, diagrams, bookmarks and other artifacts in a Git repository.

This extension is included in the EE version. It can also be installed manually to the CE version.

Marketplace URL:https://marketplace.eclipse.org/content/dbeaver-git-support

P2 repository URL:https://dbeaver.io/update/git/latest/
## Create Repository
### Share Existing Project
This includes three main steps:
1) creating a local git repository
2) creating a remote git repository
3) sharing your project

Here is how to do these steps in detail:

1. Open **Projects tab**, then choose the Project that you need to share and choose `Team - Share project` from the context menu:

![image](https://user-images.githubusercontent.com/31996417/106870275-f93aff00-66e1-11eb-9a78-08cf2b3305a4.png)

2. Create a new local repository or choose an existing one:

![image](https://user-images.githubusercontent.com/31996417/106871019-d4935700-66e2-11eb-8fce-1fae7b5de90c.png)

3. Create a new GitHub repository. Make sure to pay attention to the security. The repository should not be **public** as there are credentials to the databases you are working with. Here you fill in the `Repository name`, `Description`, `Accessibility` and click **Create repository**: 

![image](https://user-images.githubusercontent.com/49681450/189151679-b963497e-5277-4444-bbe8-37fabd06076d.png)

4. Then, on the page of the repository at GitHub, click on the **Code** button and copy the URL:
![image](https://user-images.githubusercontent.com/49681450/189152796-cad7251a-5684-48b9-919c-5d25cb8c26c3.png)


5. Paste the URL of the GitHub repository on DBeaver's side. You have to specify the GitHub `User` and `Password`. You have to use your GitHub username. However, instead of a password you have to specify the GitHub **access token**. We also recommend ticking `Store in Secure Store` in DBeaver below:

![image](https://user-images.githubusercontent.com/49681450/189149843-ca95761f-cac9-4de9-aa9f-6f2520a225ac.png)

6. The GitHub access token is located at `Settings/Developer Settings/Personal access tokens`. You need to generate the new one and tick some options: all from the `‘repo’` section (`repo:status`, `repo_deployment`, etc.). You should also tick `‘read:org’` in section `admin:org`. You will see the **only once** token:

![image](https://user-images.githubusercontent.com/49681450/189156244-99b0327c-e883-40e8-86c0-da167a852273.png)

7. When you click **Finish** on the Source Git Repository form, you will have to generate a password for all the secure data in DBeaver. You must remember this password.


8. Commit the project by right-clicking the project node and selecting `Team - Commit…` or `Ctrl+#` from the context menu. Enter a commit message (the first line should be headline-like, as it will appear in the history view) and hit the **Commit** button. If the commit was successful, the question icons will have turned into repository icons:

![image](https://user-images.githubusercontent.com/31996417/106871822-b548f980-66e3-11eb-9a00-1ddc4329c29e.png)

9. Then push changes to a remote repository using **Push HEAD** button:

You can learn more [here](https://wiki.eclipse.org/EGit/User_Guide#GitHub_Tutorial)

### Cloning existing repositories


You need to have a GitHub account.

1. Choose **Create Project from Git** button at **Projects** Tab or `File - Git - Create Project` in the Main menu:

![image](https://user-images.githubusercontent.com/31996417/122201593-da752200-cea4-11eb-9175-e131e3fb45e4.png)

2. On the first page of the wizard, enter the location of the remote repository. Make sure the repository's owner has given you access to it. Here you have to specify the GitHub `User` and `Password`. You have to use your GitHub username, but instead of a password, you specify the GitHub **access token**. We also recommend ticking `Store in the Secure Store` in DBeaver below: 

![image](https://user-images.githubusercontent.com/31996417/106876474-c9dbc080-66e8-11eb-9db2-b152ebaaf9a4.png)

3. The remote repository's location comes from the repository's page at GitHub. Click on the **Code** button and copy the URL:

![image](https://user-images.githubusercontent.com/49681450/189152796-cad7251a-5684-48b9-919c-5d25cb8c26c3.png)

4.  The GitHub access token is located at `Settings/Developer Settings/Personal access tokens`. You need to generate the new one and tick some options. Please, tick all from `‘repo’` section (`repo:status`, `repo_deployment`, etc.). You should also tick `‘read:org’` in the `admin:org` section. You will see the **only once** token:

![image](https://user-images.githubusercontent.com/49681450/189156244-99b0327c-e883-40e8-86c0-da167a852273.png)


5. On the next page, choose which branches should be cloned from the remote repository:

![image](https://user-images.githubusercontent.com/31996417/106876529-d7914600-66e8-11eb-900d-267769a535b7.png)

6. On the next page in DBeaver define where you want to store the repository on the local file system and define some initial settings:

![image](https://user-images.githubusercontent.com/31996417/106876376-ae70b580-66e8-11eb-945b-269954600385.png)

7. Choose the type of wizard you want to use and then finish the repository cloning. The project should now appear in the Navigator/Project Explorer:

![image](https://user-images.githubusercontent.com/31996417/122201831-1dcf9080-cea5-11eb-8adb-d0e527fe352c.png)

More information can be found [here](https://wiki.eclipse.org/EGit/User_Guide#Cloning_Remote_Repositories)

### Work with Project (Connections, Scripts, etc.)

If some changes were made, e.g., Connection, Script or ERD was created, deleted or changed and you want to update your remote repository, you should:

1. Go to the Context menu of the project (**Projects** tab) and choose `Team - Commit`:

![image](https://user-images.githubusercontent.com/31996417/122196400-e3172980-ce9f-11eb-9f37-a8f226e3cfc6.png)

2. **Git Staging** tab is opened at the bottom of the screen. **Unstaged Changes** are shown here. Add needed changes to the index using **Add Selected files to the index** or **Add all files to the index** button (highlighted at the picture), input commit message and then Commit changes (**Commit** button or `Ctrl+Enter`). Commit appears on the History tab (Main menu: `Window - Show view - Other - Version Control(Team) - History`): 

![image](https://user-images.githubusercontent.com/31996417/122196920-5caf1780-cea0-11eb-849b-b81b010078b0.png)

3. The `Commit and Push` button can also be used. In case you need to Push changes, it can be done from the Project context menu (`Team - Remote - Push`) or from the **History** tab if all commits do not need to be pushed (right click at needed commit - Push commit). The changes will appear in your git repository.

More information can be found [here](https://wiki.eclipse.org/EGit/User_Guide#Committing_Changes)

### Pulling New Changes from Upstream Branch

Right-click on a project in the **Project** Tab and select `Team - Pull` or right-click on a repository in the Git Repositories view and select **Pull** to pull new changes from the upstream branch that your local branch is tracking. 

If no local change was made or you want to discard your local changes, use `Team - Reset`


