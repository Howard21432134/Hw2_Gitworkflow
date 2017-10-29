# Hw2 Git Workflow#

## 1.What is Git Workflow?##

​     GitHub Flow is a lightweight, **branch**[^branch]-based workflow that supports teams and projects where deployments are made regularly. 

* Anything in the `master` branch is deployable


* To work on something new, create a descriptively named branch off of `master` 


* Commit to that branch locally and regularly push your work to the same    named branch on the server


* When you need feedback or help, or you think the branch is ready for merging, open a [pull request](http://help.github.com/send-pull-requests/)


* After someone else has reviewed and signed off on the feature, you can merge it into master*


* Once it is merged and pushed to ‘master’, you can and *should* deploy immediately



## 2.Why we choose Git Workflow?

### Issues with git-flow###

​     One of the bigger issues is that it’s more complicated than most developers and development teams actually require. It’s complicated enough that a big [helper script](https://github.com/nvie/gitflow) was developed to help enforce the flow.  Though this is cool, the issue is that it cannot be enforced in a Git GUI, only on the command line, so the only people who have to learn the complex workflow really well, because they have to do all the steps manually, are the same people who aren’t comfortable with the system enough to use it from the command line. 

### So why don't use git-flow at GitHub?###

​     Firstly, if you deploy every few hours, it’s almost impossible to introduce large numbers of big bugs.  Little issues can be introduced, but then they can be fixed and redeployed very quickly.  Normally you would have to do a ‘hotfix’ or something outside of the normal process, but it’s simply part of our normal process - there is no difference in the GitHub flow between a hotfix and a very small feature.

​     Another advantage of deploying all the time is the ability to quickly address issues of all kinds.  We can respond to security issues that are brought to our attention or implement small but interesting feature requests incredibly quickly, yet we can use the exact same process to address those changes as we do to handle normal or even large feature development.  It’s all the same process and it’s all very simple.



## 3.How to use Git Workflow?##

### Create a branch##  

​    When you're working on a project, you're going to have a bunch of different features or ideas in progress at any given time – some of which are ready to go, and others which are not. Branching exists to help you manage this workflow.

​    When you create a branch in your project, you're creating an environment where you can try out new ideas. Changes you make on a branch don't affect the `master` branch, so you're free to experiment and commit changes, safe in the knowledge that your branch won't be merged until it's ready to be reviewed by someone you're collaborating with.

### Add commits###

​      Once your branch has been created, it's time to start making changes. Whenever you add, edit, or delete a file, you're making a **commit**[^tip]., and adding them to your branch. This process of adding commits keeps track of your progress as you work on a feature branch.

​     Commits also create a transparent history of your work that others can follow to understand what you've done and why. Each commit has an associated commit message, which is a description explaining why a particular change was made. Furthermore, each commit is considered a separate unit of change. This lets you roll back changes if a bug is found, or if you decide to head in a different direction.

### Open a Pull Request###

​    **Pull Requests**[^tips] initiate discussion about your commits. Because they're tightly integrated with the underlying Git repository, anyone can see exactly what changes would be merged if they accept your request.

​     You can open a Pull Request at any point during the development process: when you have little or no code but want to share some screenshots or general ideas, when you're stuck and need help or advice, or when you're ready for someone to review your work. By using GitHub's @mention system in your Pull Request message, you can ask for feedback from specific people or teams, whether they're down the hall or ten time zones away.

### Discuss and review your code###

​     Once a Pull Request has been opened, the person or team reviewing your changes may have questions or comments. Perhaps the coding style doesn't match project guidelines, the change is missing unit tests, or maybe everything looks great and props are in order. Pull Requests are designed to encourage and capture this type of conversation.

​     You can also continue to push to your branch in light of discussion and feedback about your commits. If someone comments that you forgot to do something or if there is a bug in the code, you can fix it in your branch and push up the change. GitHub will show your new commits and any additional feedback you may receive in the unified Pull Request view.

### Deploy###

​    Once your pull request has been reviewed and the branch passes your tests, you can deploy your changes to verify them in production. If your branch causes issues, you can roll it back by deploying the existing master into production.

### Merge###

​     Now that your changes have been verified in production, it is time to merge your code into the master branch.Once merged, Pull Requests preserve a record of the historical changes to your code. Because they're searchable, they let anyone go back in time to understand why and how a decision was made.

[^branch]: Branching is a core concept in Git, and the entire GitHub Flow is based upon it. There's only one rule: anything in the master branch is always deployable.

## 



[^tip]:  Commit messages are important, especially since Git tracks your changes and then displays them as commits once they're pushed to the server. By writing clear commit messages, you can make it easier for other people to follow along and provide feedback.
[^tips]: If you're using a Fork & Pull Model, Pull Requests provide a way to notify project maintainers about the changes you'd like them to consider. If you're using a Shared Repository Model, Pull Requests help start code review and conversation about proposed changes before they're merged into the master branch.