# start agent and add key

```bash
 $ eval "$(ssh-agent -s)"
 $ ssh-add -K ~/.ssh/id_ed25519
 ```

 # slow logins

 https://jrs-s.net/2017/07/01/slow-ssh-logins/


 edit `etc/ssh/sshd_config`

set

```
UseDNS no
```
