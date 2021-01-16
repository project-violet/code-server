# Settings for violet project code-server

## Command line

### Install nginx

```console
violet.dev.master@code-server:~$ sudo apt install nginx
violet.dev.master@code-server:~$ curl https://raw.githubusercontent.com/project-violet/code-server/main/default default
violet.dev.master@code-server:~$ sudo mv default /etc/nginx/sites-available/default
violet.dev.master@code-server:~$ sudo service nginx reload
```

### Install code-server

```console
violet.dev.master@code-server:~$ curl -fsSL https://code-server.dev/install.sh | sh
# Check your password
violet.dev.master@code-server:~$ vim ~/.local/share/code-server
# Start server
violet.dev.master@code-server:~$ code-server
```
