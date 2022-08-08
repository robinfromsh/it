1. setting the link
    $ git remote add <link address>

2. check the link 
    $ git remote -v

3. push the file
    $ git push origin master

4. clone the file
    $ git clone <file link>
    
    the people could not push if not a member in the team

5. pull the file
    pull = fetch + merge
    $ git fetch <link nickname> <branchname>
        $ git fetch origin master
    $ git merge <link nickname / branchname>
        $ git merge origin/master
    $ git pull <link nickname> <branchname>

    if the conflicts happen, github not allow you to push the edit,
    only pull first.
    the way to solve the conflicts is similar the merge in the local.

    
