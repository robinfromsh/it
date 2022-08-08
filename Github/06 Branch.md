1. create
    $ git branch < branch name >


2. check the branch
    $ git branch -v

3. switch the branch
    $ git chechout < branch name >

4. merge the branch
    1. checkout to the branch need to merge(main branch)

    2. merge
        $ git merge <merging branch name>

5. conflict of the branch
    after merging 
         xxx mingw64 ~xxx(branch A / branch B)

    in the file:
        xxxxx
        xxxx
        <<<<<head 
        xxxxx edit by branch A
        =============
        vvvvvv edit by branch B
        >>>>> branch B

    $ git add <file name>

    $ git commit -m "comments"  (No file naem)

