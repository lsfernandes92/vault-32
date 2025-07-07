2025-04-11 20:41

Status: #adult 

Tags: [[howto]] [[windows]] [[dev]]

# how to install git on windows
## requirements

- make sure the winget is installed and updated



## via winget

`winget` the new package manager for newer versions of windows.

open the "cmd" on windows and run the following:
```
winget install Microsoft.Git
```



## config git name and email

see [[how to edit my global git configs]]


and


see [[how to set vscode as default editor for git]]



## setting up git with ssh keys
### **1. Generate an SSH Key**
```
ssh-keygen -t ed25519 -C "<MY_EMAIL_ACCOUNT>"
```



### 2. Add the SSH Key to the SSH Agent
```
Get-Service ssh-agent | Set-Service -StartupType Automatic
Start-Service ssh-agent
```

and

```
Start-Service ssh-agent  # Ensures the SSH agent is running
ssh-add  %USERPROFILE%/.ssh/id_ed25519
```



### 3. Copy the Public Key
```
type %USERPROFILE%\.ssh\id_ed25519.pub
```




### **4. Add the SSH Key to Your Git Account**

on github go to **Settings** → **SSH and GPG keys** → **New SSH key**.

and paste your public key and save.

now try to clone a repository.

# References
- [[how to edit my global git configs]]
- [[how to set vscode as default editor for git]]