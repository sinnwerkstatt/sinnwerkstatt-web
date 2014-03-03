# SSH

## Login with SSH Keys
* Generate SSH keys:
    * ssh-keygen -t rsa -b 4096 -C <username> -f ./id_rsa_<project_name>
* Copy the generated public key on the SSH host:
    * ssh-copy-id -i id_rsa_<project_name> <ssh_loginname>@<ssh_host>
* Add the following to the ~/.ssh/config file:
<pre>
HOST <proj_ssh_shortname>
    HostName <ssh_host>
    User <ssh_loginname>
    IdentityFile <absolute_path_to_private_ssh_key>
</pre>

## Commands
* View fingerprint: ```ssh-keygen -lf /path/to/key.pub```

## Copy file via SSH
```
scp <path_to_local_file> <proj_ssh_shortname>:<empty_or_path_on_the_server>
```
