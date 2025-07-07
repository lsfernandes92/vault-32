2025-06-22 14:45

Status: #adult

Tags: [[dev]] [[git]]

# what's the difference between `git pull upstream main` vs `git fetch upstream`

## git fetch upstream main

downloads all the tags, commits and history from the upstream to the local .git database

doesn't modify current working branch

you have more controle bc you can merge things later




## git pull upstream main

this actually downloads and merge upstream/main changes into the current branch

runs `git fetch upstream` + `git merge upstream/main` into the current branch

does modify the current working branch




# References

