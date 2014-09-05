gdocker
=======

gandi.cli poc for a remote vm docker wrapper 

experimental unstable proof of concept attempt at a buggy code snippet

examples
========

    pb@foo:~$ gandi vm delete docker
    Are you sure to delete Virtual Machine 'docker'? [yN]: y
    Deleting your Virtual Machine.
    Progress: [###################################################################] 100.00%  00:00:09  

    pb@foo:~$ gdocker version
    Sorry to bother you, exit the shell when docker is ready
    Creating your Virtual Machine.
    Progress: [###################################################################] 100.00%  00:00:49  
    Your Virtual Machine docker have been created.

    (...)

    pb@foo:~/code/gd$ gdocker version
    Client version: 0.9.0
    Go version (client): go1.2.1
    Git commit (client): 2b3fdf2
    Server version: 1.2.0
    Git commit (server): fa7b24f
    Go version (server): go1.3.1
    Last stable version: 1.2.0, please update docker

    pb@foo:~$ gdocker run -i -t debian bash
    (..)
    root@4da291c57905:/# exit
    pb@foo:~$ 

    pb@foo:~$ gandi vm stop docker
    Stopping your Virtual Machine.
    Progress: [###################################################################] 100.00%  00:01:00  

    pb@foo:~$ gdocker ps
    Starting your Virtual Machine.
    Progress: [###################################################################] 100.00%  00:01:10  
    __init__.pyc                                                             100% 5305     5.2KB/s   00:00    
    channel 3: open failed: connect failed: Connection refused
    2014/09/05 14:10:30 unexpected EOF

    pb@foo:~$ gdocker ps
    CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
