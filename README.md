# Some Notes to Clarification

__working with exists project__
- git clone __it act as if i created new dir and git init__


__Why Branching__

- Use a branch to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request.

- Develop features
- Fix bugs
- Safely experiment with new ideas

__Working With Branches__


|local  |remote   |
|---    |---      |
|    git checkout -b [branch name] | git pull origin branch name  |
|    git push --set-upstream       |  or git fetch --all, git merge|
|    git log                        |                               |                          
|    git show                      |                                |
|    git status                    |                               |
|    git rebase branch name (master) |   git merge branch name


**local**

_all I need create branch by new feature or fix bug or try new logic_

_just create new branch and test what u need before added it_

_if everything is ok and already to push_

****There some cases****

`case 1:`
> i will push to master direct
if from current branch master `<git push>`

>if from another branch and u need to push the master `<git push origin branch>`

`case 2:`

**working with remote branch**

> git fetch --all it give me access to all branches created after clone from
another team member

_this just to check code before do anything so u need switch to it by checkout_

_to see all branches after git fetch use `git branch -a`_

****Now we have 2 options****

> git merge with the target branch
`for example`

- am on f1 branch
- then i fetched --all
- git branch -a `i got new branch called f2`
- i checked out to `f2 to see the content`
- if i need merge this code i back to `f1`
- `git merge f1`

_or u can let it_

>git pull origin branch name
- it act as fetch and merge

# Trouble shooting

**conflicts**

****some cases in conflicts****
1. you write file `file_1` then you pushed it
1. your team member `pulled new update` and he wrote his own logic or anything
1. before he pushed u modified something and pushed it
1. he finished his logic and try to pushing his new modifying
1. `error please pull new update`
1. then he will get conflict
1. resolve conflict by `remove head<<<<, =====, >>>>>>`
1. then `add, commit, push new modifing`
1. conflict happened within the same file and same line
1. if you faced any problem with conflict and you couldn't know which file has conflict git status
1. file untracked has issues

1. you and your colleague working on same file and `controller file` and the same block
when try merge with your colleague branch you will faced conflict


`Note that: before push please get last update from branch`

__some points about merging__
_You can merge before pushing from local
which meant you checkout master from local and merge with you owned branch you need to push it_

_or push you branch and merging it from remote server_

>here we have some feature we can use it like restrict to push on master branch, restrict on branch like open `PR <OPEN PULL REQUEST>`

|git pull origin branch name |open pull request |
|---|---|
|get update to local branch| update remote branch `<it add reviewer on your code before merging >`|

**for example :-**

_you have a repo and you want avoid to push any code on your master or merging it you only one has access to merging any code on your master_

_you work with team member and you want your colleague see what your new code_


|get merge | get rebase|
|---|---|
|combine all comments into one comment| get set of comment out your repo and make last commit as new base on your branch|

`reabse to clear history prefer do it in your local`

# RollBack Command

|git revert| git reset --hard|
|---|---|
| get back to comment by create new comment for that and move to it |  remove head of branch|

> head pointer to last commit on branch

__if you reset your local head and try to push you will get already update to make remote repo updated with your local repo you will need `push -f`__


# history command

- git log
- git show
- git --graph

****each operation check your status****

`git status`






# __scenario__
`case 1:`
> __As new developer joined to new project I will get clone of project__

> __for new first task for me I will create new branch__

> __after finished my code i will rebase to clear history | you not optional__


>__according to my co. rules if there one has access to merge i will push and open pr__

>__if anyone can push on master open pr with me colleague to see update code then i will merge it__

> __if am only one on project i will merge localy the push to master__

`case 2:`
> __if I have task as sub tasks with my colleague and my code depend on my colleague code i will need merge his branch__

`case 3 :`
 >__if my colleague create new remote branch and I have no idea if i need it or not
 i will fetch it, checkout, see his code and decide if i need merging it or not__

 `case 4:`
 > __there is a branch I am sure I need it get pull origin branch_name__

 `Note :`


 _if co. working as git flow all commit pushing to default branch ( dev branch)
 then we will merge new release with master_

 _if co. working as workflow we create sup branch and then merging it with master_

 _if co. working as centralize we will push to master direct_


`Thank You, if anyone need to anything can send to me anytime`
