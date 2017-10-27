#A Brief Introduction of Git Workflow
---
![](http://a2.qpic.cn/psb?/V13Ti98m05LW5b/wdUTgWXi46p7z5ctjgUJOhQUXy0gQjpTsNhdY7TujhU!/b/dD8BAAAAAAAA&bo=yAFPAQAAAAADB6U!&rf=viewer_4)



##Ⅰ. Overview


  - Concept
  - Mutiple Git Workflows    
     + Centralized Workflow
     + Feature Branch Workflow
     + Git flow
     + Forking Workflow
     + Github Flow

##Ⅱ. What is a Git Workflow
> flow - the act of flowing or streaming; continuous progression 
 
A Git Workflow is a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner. Git workflows encourage users to leverage Git effectively and consistently.

##Ⅲ. Multiple Git workflows
###1.Centralized Workflow
>the Centralized Workflow uses a central repository to serve as the single point-of-entry for all changes to the project. 
>
>---
####1.1 Features
The default development branch is called **master** and all changes are committed into this branch. 

This workflow doesn’t require any other branches besides master.


####1.2 Procedure
![](http://a2.qpic.cn/psb?/V13Ti98m05LW5b/Cq2M0BH0aeT83gdmzCrf1gnq3lyyDNg*pCOZumUm2Gs!/b/dD8BAAAAAAAA&bo=WQPCAQAAAAADALw!&rf=viewer_4)

- Create the central repository on a server
- Each developer creates a local copy of the entire project
- Developers can make changes using the standard Git commit process: edit, stage, and commit.
- Fetch the updated central commits and rebase changes on top of them to resolve a merge conflict
- Push changes to the central repository,


###2. Feature Branch Workflow
>The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated **feature branch** instead of the master branch.

---
####2.1 Procedure
![](http://a1.qpic.cn/psb?/V13Ti98m05LW5b/tM1MW0ssJqXiTQqpvuqcFcK*5PR9XxBk1lFYsJYONOI!/b/dPMAAAAAAAAA&bo=ZgIZAgAAAAADAFo!&rf=viewer_4)

- *master* represents the official project history
- Developers create a new branch every time they start work on a new feature.
- Developers can edit, stage, and commit changes to a feature branch.
- Pull request to Resolve feedback
- Merge the pull request to server

###3. Git flow
>The Gitflow Workflow defines a strict branching model designed around the project **release**.

>In addition to feature branches, it uses **individual branches** for preparing, maintaining, and recording releases.

---
![](http://a1.qpic.cn/psb?/V13Ti98m05LW5b/PMUjFL*8QXWXZNgCLYo0aNChyoJJWmHC0rpa8zTMblA!/b/dPMAAAAAAAAA&bo=gAJQAwAAAAADAPQ!&rf=viewer_4)
####3.1 Two long-term branches

Instead of a single master branch, this workflow uses two branches to record the history of the project.
 
- **master** branch stores the official release history

- **develop** branch serves as an integration branch for features.
####3.2 Three short-term branches
#####3.2.1 feature branches
Each new feature should reside in its own branch, which can be pushed to the central repository for backup/collaboration.

 But, instead of branching off of master, feature branches use **develop** as their parent branch. When a feature is complete, it gets merged back into develop. Features should never interact directly with master.
#####3.2.2 release branches
release branches are based on the **develop** branch. 

Once develop has acquired enough features for a release (or a predetermined release date is approaching), developer can fork a release branch off of develop.

Once the release is ready to ship, it will get merged it into ****master** and develop**, then the release branch will be deleted.
##### 3.2.3 hotfixes

Maintenance or hotfix branches are based on **master** instead of develop. As soon as the fix is complete, it should be merged into both master and develop (or the current release branch), and master should be tagged with an updated version number.

---
###4.Forking Workflow
Instead of using a single server-side repository to act as the “central” codebase, it gives every developer their own server-side repository. This means that each contributor has not one, but two Git repositories: a private local one and a public server-side one.
1.	A developer 'forks' an 'official' server-side repository as their own server-side copy.
2.	The new server-side copy is cloned to their local system.
The developer makes changes on the new branch and they push the commit to their own public repository
3.	The developer opens a pull request from the new branch to the 'official' repository.
4.	The pull request gets approved for merge and is merged into the original server-side repository


