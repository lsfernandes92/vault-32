2025-04-11 20:38

Status: #adult 

Tags: [[howto]] [[windows]] [[dev]]

# how to edit my global git configs
git stores all the global configurations on a `.gitconfig` file.

you can set configs globally with the `--global` option.

if you omit the `--global` option the configs will apply to the current git repo.



## set configs
you can access the git configs with the following command:
```
git config --global --edit
```

you can access my personal `.gitconfig` [here](https://github.com/lsfernandes92/dotfiles/blob/master/git/gitconfig.symlink)


## set username
```
git config --global user.name "<MY_USER_NAME>"
```

## set email
```
git config --global user.email "<MY_EMAIL>"
```



## view configs
you can also view the list by running the following:
```
git config --list
```

# References
- [[how to install git on windows]]
- [[how to set vscode as default editor for git]]