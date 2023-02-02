## Create pull requests

Before creating a pull request you shoulod create a ticket on our [issue tracker](https://github.com/dbeaver/dbeaver/issues). You can leave a commentthatyou are going to implement this feature(or fix a bug) by yourself. DBeaver dev/qa team will reply you with some comments and then you can start working on imlementation.  

You can use the [standard GitHub instruction](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork). 
Generally you need to create a fork of `dbeaver/dbeaver` repository, create a new branch, commit your changes and then create a pull request in upstream repository.  

Imprtant: when you commit changes in your branch add ticket number in the commit comment.  
Like this: `dbeaver/dbeaver#issue-number Initial commit for my super-duper feature`.  
You can make any number of commits. We usually perform squash before merging changes in the main repository.  

## Can I fix a bug by myself?

If you think that some bug on our [board](https://github.com/dbeaver/dbeaver/issues) has to be fixed and for some reason it is not in the nearest milestone then you could try to fix it by yourself. It makes sense to ask about it in the ticket because sometimes we don't resolve tickets for a reason.  

After all if you decided that you want to fix the bug then you make a pull request (see above), the team will review it and write a PR review if necessary. If PR is merged then the fix will appear in the next version of DBeaver community (which is realeased every two weeks).

## What types of new features are acceptable

Generally you could suggest anything you think is usefull in database management tool. However we usually do not implement features too specific for your development process or specific to your internal company processes.  
Good options:
- Add new database or driver support
- Extend database metadata read/modify (e.g. add triggers read it a specific database)
- Add new SQL generator
- Add new data export format
- Localize DBeaver interface (extend existing localization or add a new language)
- Add new database-specific tool (e.g. table analyze for a specific database)

There are samples of all these features in our codebase (TBD).

## Code guidelines

## Code style

