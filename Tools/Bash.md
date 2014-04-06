# Bash

## Make sh file [executable](https://help.ubuntu.com/community/Beginners/BashScripting#Scripting)

```
chmod a+x /where/i/saved/it/hello_world.sh   #Gives everyone execute permissions
# OR
chmod 700 /where/i/saved/it/hello_world.sh   #Gives read,write,execute permissions to the Owner
```

## Processes

* ``ps aux | grep firefox`` (find the firefox process)
* ``sudo kill firefox`` (kill the firefox process) ([learn more](http://www.cyberciti.biz/faq/kill-process-in-linux-or-terminate-a-process-in-unix-or-linux-systems/))
* ``sudo kill -9 firefox`` (stronger kill)

## Shutdown

``sudo shutdown -h 18:45``
