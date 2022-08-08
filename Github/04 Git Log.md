1. check the history of the git
    1. $ git log

        commit 1001...123(HEAD -> master)
        AUthor: xxx <123@123.com>
        Date: ...
            Sencond... A.text
        
        commit 2001...456
        AUthor: xxx <123@123.com>
        Date: ...
            First... A.text

    2. $ git log --pretty=oneline

        1001...(HEAD -> master) Sencond... A.text
        2001... First... A.text   

    3. $ git log --oneline

        1001...(HEAD -> master) Sencond... A.text
        2001... First... A.text

    4. $ git reflog
        1001...(HEAD -> master) HEAD(0): commit: Sencond... A.text
        2001 ... HEAD(1): commit:First... A.text

2. Log operation
    1. Using the Index num : git reset --hard <index num>
        $ git reset --hard <2001...>

    2. Using the ^ mark : get reset --hard HEAD^ (Only for back)
    the amount of ^ means backwards how many steps

    3. Using the ~ mark : get reset --hard HEAD~<num> (Only for back)
    the <num> means backwards how many steps
        $ git reset --hard HEAD~3 
        = $ git reset --hard HEAD^^^

3. reset hard &  soft
    1. --soft 
        only for moving the head in the git repository
                git repository = Rev 2
                staging area = Rev 2
                working directory =  Rev 2
            After
                git repository = Rev 1
                staging area = Rev 2
                Working directory =  Rev 2
            staging area and working directory looks like new modified         
    
    2. --mixed
        moving the head in the git repository
        reset the stageing area
        
                git repository = Rev 2
                staging area = Rev 2
                working directory =  Rev 2
            After
                git repository = Rev 1
                staging area = Rev 1
                Working directory =  Rev 2
            working directory looks like new modified 

    3. --hard
        moving the head in the git repository
        reset the stageing area
        reset working directory

                git repository = Rev 2
                staging area = Rev 2
                working directory =  Rev 2
            After
                git repository = Rev 1
                staging area = Rev 1
                Working directory =  Rev 1
            working directory looks like new modified 
    
        





4. File recovery
    if already commit to the repo,
    jump to the time before deleting, Using the git --hard HEAD <index num> 

    if just add to stagin area
    Using the git --hard HEAD

