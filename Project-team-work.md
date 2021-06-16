DBeaver is fully integrated with the Git team work/version control system.
You can keep your project configuration, scripts, diagrams, bookmarks and other artifacts in a Git repository.

This extension is included in the EE version. Also it could be installed to CE version manually.

Marketplace URL:https://marketplace.eclipse.org/content/dbeaver-git-support

P2 repository URL:https://dbeaver.io/update/git/latest/
## Create Repository
### Share Existing Project
1. Open **Projects tab**, then choose Project that you need to share and choose `Team - Share project` from the context menu

![image](https://user-images.githubusercontent.com/31996417/106870275-f93aff00-66e1-11eb-9a78-08cf2b3305a4.png)

2. Create a new local repository or choose an existing one.

![image](https://user-images.githubusercontent.com/31996417/106871019-d4935700-66e2-11eb-8fce-1fae7b5de90c.png)

3. Create Repository at GitHub or use the URL of the existing one.

4. Commit the project by right-clicking the project node and selecting `Team - Commit…` or `Ctrl+#` from the context menu. Enter a commit message (the first line should be headline-like, as it will appear in the history view) and hit the **Commit** button. If the commit was successful, the question icons will have turned into repository icons.

![image](https://user-images.githubusercontent.com/31996417/106871822-b548f980-66e3-11eb-9a00-1ddc4329c29e.png)

Then push changes to a remote repository using **Push HEAD** button.

You can learn more [here](https://wiki.eclipse.org/EGit/User_Guide#GitHub_Tutorial)

### Cloning existing repositories
1. Choose **Create Project from Git** button at **Projects** Tab or `File - Git - Create Project` in Main menu

![image](https://user-images.githubusercontent.com/31996417/122201593-da752200-cea4-11eb-9175-e131e3fb45e4.png)

2. On the first page of the wizard enter the location of the remote repository:

![image](https://user-images.githubusercontent.com/31996417/106876474-c9dbc080-66e8-11eb-9db2-b152ebaaf9a4.png)

3. On the next page choose which branches should be cloned from the remote repository:

![image](https://user-images.githubusercontent.com/31996417/106876529-d7914600-66e8-11eb-900d-267769a535b7.png)

4. On the next page define where you want to store the repository on the local file system and define some initial settings.

![image](https://user-images.githubusercontent.com/31996417/106876376-ae70b580-66e8-11eb-945b-269954600385.png)

5. Choose the type of the wizard you want to use and then finish repository cloning. The project should now appear in the Navigator/Project Explorer.

![image](https://user-images.githubusercontent.com/31996417/122201831-1dcf9080-cea5-11eb-8adb-d0e527fe352c.png)

More information could be found [here](https://wiki.eclipse.org/EGit/User_Guide#Cloning_Remote_Repositories)

### Work with Project (Connections, Scripts, etc.)

If some changes were made, e.g., Connection, Script or ERD was created, deleted or changed and you want to update your remote repository, you should:

1. Go to the Context menu of the project (**Projects** tab) and choose `Team - Commit`

![image](https://user-images.githubusercontent.com/31996417/122196400-e3172980-ce9f-11eb-9f37-a8f226e3cfc6.png)

2. **Git Staging** tab is opened at the bottom of the screen. **Unstaged Changes** are shown here. Add needed changes to the index using **Add Selected files to the index** or **Add all files to the index** button (highlighted at the picture), input commit message and then Commit changes (`Commit` button or `Ctrl+Enter`). Commit appears at the History tab (Main menu: `Window - Show view - Other - Version Control(Team) - History`). 

![image](https://user-images.githubusercontent.com/31996417/122196920-5caf1780-cea0-11eb-849b-b81b010078b0.png)

3. At the second step also could be used `Commit and Push` button. In case you need to Push changes, it could be done from Project context menu (`Team - Remote - Push`) or from **History** tab in case it is needed to push not all commits (right click at needed commit - Push commit). Changes should appear in your git repository.

More information could be found [here](https://wiki.eclipse.org/EGit/User_Guide#Committing_Changes)

### Pulling New Changes from Upstream Branch

Right-click on a project in the **Project** Tab and select `Team - Pull` or right-click on a repository in the Git Repositories view and select **Pull** to pull new changes from the upstream branch your local branch is tracking. 

If you did no local change or want to discard your local changes, use `Team - Reset`


