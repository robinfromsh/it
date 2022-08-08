1. Check the Git status
    $ git status

        No branchs master
        NO commites yet
        nothing to commit (create/copy files and use "git add" to track)

2. add to the cache
    $ git add

3. submit to the local repo
    $ git commit

4. Example

    1. Create a new file & check the status
        $ vim A.txt
        
        $ git status

            on branch master
            No commits yet
            untracked files:
            (use "git add <file>..."to inclue in what will be committed)
                A.text
            nothing added to commit but untracked files present (use " git add" to track)

    3. Add the file & & check the status
        $ git add A.text
        
        $ git status

            on branch master
            No commits yet
            Changes to be committed:
                (use "git rm --cached <file>..." to unstage)
                    new file: A.text

    4. If return to unadd the file
        $ git rm --cached A.text
        rm 'A.text'

        $ git status

            on branch master
            No commits yet
            untracked files:
            (use "git add <file>..."to inclue in what will be committed)
                A.text
            nothing added to commit but untracked files present (use " git add" to track)

    5. Commit the file to the lock repo.
        $ git commit A.state

        $ git status 
            On branch master
            nothing to commite,working tree clean
        


        