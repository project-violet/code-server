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
# Start server
violet.dev.master@code-server:~$ code-server
# Check your password
violet.dev.master@code-server:~$ vim ~/.local/share/code-server
```

### Install Fira Code Font

```console
violet.dev.master@code-server:~$ sudo apt update
violet.dev.master@code-server:~$ sudo apt install fonts-firacode
violet.dev.master@code-server:~$ sudo sed -i 's/<\/head>/<link type="text\/css" href="https:\/\/fonts.googleapis.com\/css2?family=Fira+Code:wght@300;400;500;600;700\&display=swap" rel="stylesheet"><\/head>/g' /usr/lib/code-server/src/browser/pages/vscode.html
violet.dev.master@code-server:~$ sudo sed -i 's/font-src/font-src fonts.gstatic.com/g' /usr/lib/code-server/src/browser/pages/vscode.html
violet.dev.master@code-server:~$ sudo sed -i 's/style-src/style-src fonts.googleapis.com/g' /usr/lib/code-server/src/browser/pages/vscode.html
```

### Install C/C++

```console
# Download vsix file manually
violet.dev.master@code-server:~$ curl -L https://github.com/microsoft/vscode-cpptools/releases/download/1.1.3/cpptools-linux.vsix -o cpptools-linux.vsix
# Then Ctrl+Shift+P => ext install vsix
```
