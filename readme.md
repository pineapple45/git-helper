Git Commands:

### MOST IMPORTANT COMMANDS

1.  git init // initialise git repository locally

    // After this make changes to the project like adding files, making changes to code etc.

2.  git add -A

    // instead of ‘ -A ‘ we can also use ‘ . ’ , ’ -u ’ , ‘ \* ’

    These have different meanings and their meanings can be found over here:

        [https://www.youtube.com/watch?v=tcd4txbTtAY&list=PL-osiE80TeTuRUfjRe54Eea17-YfnOOAx&index=6](https://www.youtube.com/watch?v=tcd4txbTtAY&list=PL-osiE80TeTuRUfjRe54Eea17-YfnOOAx&index=6)

3.  git commit -m &lt;your commit- message>
4.  git push origin master

    // all files of local repository will now be pushed to github online repository

    // ‘origin’ is just short to define the path to your repository online

    // if origin is not defined earlier, it can be defined as follows:

        //git remote add origin [https://github.com/](https://github.com/)&lt;repository-name>

    // similar to ‘origin’ any other name can be given such as ‘upstream’

    _(OTHER IMPORTANT COMMANDS )_

5.  git clone [https://github.com/](https://github.com/)&lt;repo-name which is to be cloned> // This provides similar functionality to download as zip on github cloud repos
6.  Git reset // undo for git add . (unstages all changes)
7.  Git status // check status of local/online repository
8.  Git log // check commit history
9.  Git log --oneline // very similar to git log but gives details in a short and precise manner
10. Git branch dev // create a new branch but not jump into it. At this stage we are not working in ‘dev’ branch , we have just initialised it.
11. Git checkout dev // Now we jump into dev and whatever we do will be saved inside in dev branch

    // Original branch is known as master branch. It is created whenever we do git init

12. Git checkout -b dev ( does 9 and 10 in single step )
13. Git merge dev ( for merging dev we should not be in dev. We should be in that branch where u want dev to be merged )

    // for ex: lets say u want to merge dev with master and you are currently on dev.

    // first do → git checkout master then git merge dev

    // also make sure to commit changes in dev branch before merging with master

14. Git merge --squash dev ( squash commits of dev and them merge )
15. Git branch -d dev ( deletes dev branch if it is merged with master at least once )
16. Git branch -D dev ( deletes dev branch if it is not merged with master even once)
17. Undoing changes. Going backwards and reviewing/updating/removing old commits

    --Git checkout commit

    --Git revert commit

    --Git reset commit

    --git reset commit --hard

    These can be better understood through this link:

    [https://www.youtube.com/watch?v=RIYrfkZjWmA&list=PL4cUxeGkcC9goXbgTDQ0n_4TBzOO0ocPR&index=7](https://www.youtube.com/watch?v=RIYrfkZjWmA&list=PL4cUxeGkcC9goXbgTDQ0n_4TBzOO0ocPR&index=7)

18. Important corner case:

    Let’s say you have forked someone else's public repository to your account and then you cloned that forked repository to your local environment. Now u make changes in that local environment and push those changes to that forked repository on your account. Now you want to create a pull request to the original someone else's repository. But some other person already created a pull request to the original repository and it was merged. Now if your pull request will not get merged due to conflicts.

    This problem can be eliminated by first pulling all those changes in the original repository to your local repository and then pushing final changes to your accounts repository along with the changes done by you itself.

    Video for reference: [https://www.youtube.com/watch?v=-zvHQXnBO6c](https://www.youtube.com/watch?v=-zvHQXnBO6c)

    git remote -v

        origin: https://github.com/pineapple45/water-tank.git(push)


        origin: https://github.com/pineapple45/water-tank.git(fetch)

    git remote add upstream https://github.com/{orignal_git_username}/water-tank.get

    git remote -v

        origin: https://github.com/pineapple45/water-tank.git(push)


        origin: https://github.com/pineapple45/water-tank.git(fetch)


        upstream: https://github.com/{orignal_git_username}/water-tank.get(push)


        upstream: https://github.com/{orignal_git_username}/water-tank.get(fetch)

    git branch -a

        *master

    git fetch upstream

    git branch -a

        *master


        upstream/master

    git merge upstream/master

    git branch -a

        *master

    git push origin master

19. Pull a specific commit:

    git fetch origin pull/ID/head:BRANCHNAME

    _(OTHER USED COMMANDS ) No need to be done now_

\_ \_

20. Git rebase ( [https://www.youtube.com/watch?v=CRlGDDprdOQ](https://www.youtube.com/watch?v=CRlGDDprdOQ) )

    // should be used locally only and carefully. Do not use this command without //experience

21. Git stash ( [https://www.youtube.com/watch?v=DeU6opFU_zw](https://www.youtube.com/watch?v=DeU6opFU_zw) )
