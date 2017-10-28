A Brief Introduction of Git Workflow
-

![](http://a2.qpic.cn/psb?/V13Ti98m05LW5b/wdUTgWXi46p7z5ctjgUJOhQUXy0gQjpTsNhdY7TujhU!/b/dD8BAAAAAAAA&bo=yAFPAQAAAAADB6U!&rf=viewer_4)


---
Ⅰ. Overview
=
  - Concept
  - Mutiple Git Workflows    
     + Centralized Workflow
     + Feature Branch Workflow
     + Git flow
     + Forking Workflow
     + Github Flow
  - Reference

Ⅱ. What is a Git Workflow
=
> flow - the act of flowing or streaming; continuous progression 
 
A Git Workflow is a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner. Git workflows encourage users to leverage Git effectively and consistently.

Ⅲ. Multiple Git workflows
=
1.Centralized Workflow
-
>the Centralized Workflow uses a central repository to serve as the single point-of-entry for all changes to the project. 

---
1.1 Features
-
The default development branch is called `master` and all changes are committed into this branch. 
<br>
This workflow doesn’t require any other branches besides master.
<br>
1.2 Procedure
-
![](http://a2.qpic.cn/psb?/V13Ti98m05LW5b/Cq2M0BH0aeT83gdmzCrf1gnq3lyyDNg*pCOZumUm2Gs!/b/dD8BAAAAAAAA&bo=WQPCAQAAAAADALw!&rf=viewer_4)

- Create the central repository on a server
- Each developer creates a local copy of the entire project
- Developers can make changes using the standard Git commit process: edit, stage, and commit.
- Fetch the updated central commits and rebase changes on top of them to resolve a merge conflict
- Push changes to the central repository,

<br>
2. Feature Branch Workflow
-
>The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated **feature branch** instead of the master branch.

---
2.1 Procedure
-
![](http://a1.qpic.cn/psb?/V13Ti98m05LW5b/tM1MW0ssJqXiTQqpvuqcFcK*5PR9XxBk1lFYsJYONOI!/b/dPMAAAAAAAAA&bo=ZgIZAgAAAAADAFo!&rf=viewer_4)

- `master` represents the official project history
- Developers create a new branch every time they start work on a new feature.
- Developers can edit, stage, and commit changes to a `feature branch`.
- `Pull request` to Resolve feedback
- Merge the pull request to server

<br>
3. Git flow
-
>The Gitflow Workflow defines a strict branching model designed around the project **release**.

>In addition to feature branches, it uses **individual branches** for preparing, maintaining, and recording releases.

---
![](http://a1.qpic.cn/psb?/V13Ti98m05LW5b/PMUjFL*8QXWXZNgCLYo0aNChyoJJWmHC0rpa8zTMblA!/b/dPMAAAAAAAAA&bo=gAJQAwAAAAADAPQ!&rf=viewer_4)
<br>
3.1 Two long-term branches
-
Instead of a single master branch, this workflow uses two branches to record the history of the project.
 
- `master branch` stores the official release history

- `develop branch` serves as an integration branch for features.


3.2 Three short-term branches
-
<br>
###3.2.1 feature branches
<br>Each new feature should reside in its own branch, which can be pushed to the central repository for backup/collaboration.
<br>But, instead of branching off of master, feature branches use `develop` as their parent branch. When a feature is complete, it gets merged back into develop. Features should never interact directly with master.
###3.2.2 release branches
<br>release branches are based on the `develop` branch. 
<br>Once develop has acquired enough features for a release (or a predetermined release date is approaching), developer can fork a release branch off of develop.
<br>Once the release is ready to ship, it will get merged it into `master `and `develop`, then the release branch will be deleted.
### 3.2.3 hotfixes

<br>Maintenance or hotfix branches are based on `master` instead of develop. As soon as the fix is complete, it should be merged into both master and develop (or the current release branch), and master should be tagged with an updated version number.

<br>
4.Forking Workflow
-
>Instead of using a single server-side repository to act as the “central” codebase, it gives every developer their own server-side repository. This means that each contributor has not one, but two Git repositories: a **private local one** and a **public server-side one**.

![](http://a3.qpic.cn/psb?/V13Ti98m05LW5b/mMHlI*8JZ8ozPRqNEX5tDxPvvHrNeC8f4y98lFCHsB0!/b/dPIAAAAAAAAA&bo=kAFYAQAAAAADAO0!&rf=viewer_4)
<br>
Procedure
-
- A developer 'forks' an 'official' server-side repository as their own server-side copy.
- The new server-side copy is cloned to their local system.
- The developer makes changes on the new branch and then push the commit to his own public repository
- The developer opens a pull request from the new branch to the 'official' repository.
- The pull request gets approved for merge and is merged into the original server-side repository
<br>
5. Github flow
-
>GitHub Flow is a lightweight, branch-based workflow that supports teams and projects where **deployments** are made regularly.

---
![](http://a1.qpic.cn/psb?/V13Ti98m05LW5b/gt3H413IzZ63i4nUPMM2tdi3x.UUNec8hciUQaEqMFU!/b/dPMAAAAAAAAA&bo=YATOAAAAAAADAI8!&rf=viewer_4)
<br>
Procedure
-
- Create a branch to experiment and commit changes
- Add, edit, or delete a file, then make a commit, and add them to branch.
- Open a `Pull Request` at any point during the development process to initiate discussion about the commits
- Discuss and review code to fix bugs in the branch and push up the change
- Once the pull request has been reviewed and the branch passes all tests,  `deploy` changes to verify them in production and merge the code into the master branch
<br>
Ⅳ. Reference
-
- [深入理解学习Git工作流](https://segmentfault.com/a/1190000002918123#articleHeader20)
- [A successful Git branching model » nvie.com ](http://nvie.com/posts/a-successful-git-branching-model/?utm_source=qq&utm_medium=social)
- [Understanding the GitHub Flow · GitHub Guides]( https://guides.github.com/introduction/flow/?utm_source=qq&utm_medium=social)
- [git-workflow-tutorial]( https://www.atlassian.com/git/tutorials/comparing-workflows)
- [Git 工作流程](http://www.ruanyifeng.com/blog/2015/12/git-workflow.html)



