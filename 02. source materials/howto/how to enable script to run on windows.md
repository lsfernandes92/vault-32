2025-04-11 20:34

Status: #adult

Tags: [[howto]] [[windows]] [[dev]]

# how to enable script to run on windows
## solution 1: allow running the script temporarily for the current session (recommended)

run this command as Administrator in PowerShell:

```
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```



## solution 2: change execution policy permanently for the current user

if you trust scripts on your system, run as Administrator:
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

# References

