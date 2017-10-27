#A Brief Introduction of Git Workflow
---
![](http://a2.qpic.cn/psb?/V13Ti98m05LW5b/wdUTgWXi46p7z5ctjgUJOhQUXy0gQjpTsNhdY7TujhU!/b/dD8BAAAAAAAA&bo=yAFPAQAAAAADB6U!&rf=viewer_4)



##Ⅰ. Overview


  - Concept
  - Mutiple Git Workflows    
     + Centralized Workflow
     + Feature Branch Workflow
     + Gitflow
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

