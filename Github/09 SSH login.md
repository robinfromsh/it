1. root directory
    $ cd ~

2. delete current ssh diretory
    $ rm -rvf .ssh/

3. create ssh key
    $ ssh-keygen -t rsa -C <account email>
        $ ssh-keygen -t rsa -C abc@123.com

4. review ssh
    $ ssh -v abc@123.com
    if it's 1st time,it shows
        No more quthentication methods to try
        Permission denied(publickey)
    if not, it shows:
        ssh:Could not resolve hostname abc@123.com: Name or service not known

5. (if needed,use ssh-agent)
    $ ssh-agent -s
    shows:
    SSH_AUTH_SOCK=/tmp/ssh-resfsfafa/agent.678;export SSH_AUTH_SOCK
    SSH_AGENT_PID=679; export SSH_AGENT_PID
    echo Agent pid 679

6. copy the content of id_rsa.pub,paste to the website ssh setting.
    $ cd .ssh/
    $ cat id_rsa.pub