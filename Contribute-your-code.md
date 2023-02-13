## Create pull requests

Before creating a pull request you shoulod create a ticket on our [issue tracker](https://github.com/dbeaver/dbeaver/issues). You can leave a comment that you are going to implement this feature (or fix a bug) by yourself. DBeaver dev/qa team will reply you with some comments and then you can start working on implementation.  

You can use the [standard GitHub instruction](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork). 
Generally you need to create a fork of `dbeaver/dbeaver` repository, create a new branch, commit your changes and then create a pull request in upstream repository.  

Important: when you commit changes in your branch, add ticket number in the commit comment.  
Like this: `dbeaver/dbeaver#issue-number Initial commit for my super-duper feature`.  
You can make any number of commits. We usually perform squash before merging changes in the main repository.  

## Can I fix a bug by myself?

If you think that some bug on our [board](https://github.com/dbeaver/dbeaver/issues) has to be fixed and for some reason it is not in the nearest milestone, then you could try to fix it by yourself. It makes sense to ask about it in the ticket, because sometimes we don't resolve tickets for a reason.  

After all if you decided that you want to fix the bug, then you make a pull request (see above), the team will review it and write a PR review if necessary. If PR is merged, then the fix will appear in the next version of DBeaver community (which is released every two weeks).

## What types of new features are acceptable

Generally you could suggest anything you think is useful in database management tool. However we usually do not implement features too specific for your development process or specific to your internal company processes.  

Good options:
- Add new database or driver support
- Extend database metadata read/modify (e.g. add triggers read it a specific database)
- Add new SQL generator
- Add new data export format
- Localize DBeaver interface (extend existing localization or add a new language)
- Add new database-specific tool (e.g. table analyze for a specific database)

There are samples of all these features in our codebase.

```
TBD
```

## Code guidelines

Main rule: use the same codestyle, which is already used in a particular source file.  

- Historically there are several slightly different code styles in our codebase, but if you modify an old file, it is better to use the same codestyle, which used in this file.  
- Do not reformat code or optimize all imports in a file you are changing. It is very hard to review your commits otherwise (because of big number of changes)
- Use our automatic codestyle checks in PRs (every PR you will make in `dbeaver/dbeaver` repository will be checked and you can see the report of the check list)

IntelliJ IDEA code style can be taken here: https://github.com/dbeaver/dbeaver-idea-project

## Code style

