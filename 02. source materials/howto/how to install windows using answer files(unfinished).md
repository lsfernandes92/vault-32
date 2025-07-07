
2025-04-29 18:14

Status: #child 

Tags: [[dev]] [[howto]] [[writing]]

# how to install windows using answer files
## draft
yes, i'm still that person that have an windows pc at home and windows still is that OS that requires you to format the whole system from time to time. and what's is more boring than install windows from the scratch? 😪

i found a video showing a technique widely used on linux called `cloud-init`. `cloud-init` is a tool used for setup machine instances(where virtual machines or bare-metal servers) during their first boot. with that, you can, for example, create accounts; set passwords; setup the network configuration, pre-install packages, run custom scripts, skip initial setup steps, fresh install without bloatwares, etc... 

### how to?
amazing isn't it? on windows you can set those initial configuration using the [answer files](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/update-windows-settings-and-scripts-create-your-own-answer-file-sxs?view=windows-11).





## what is the cloud-init widely used in linux?
is a tool widely used for setup the machine instances(whether virtual machines or bare-metal servers) during their first boot



## what are the cloud-init features?
- create accounts
- set passwords
- network configuration
- package installation
- run custom scripts
- format/mount disks



## what are the `unattend.xml` or `aunattend.xml` files or the answer files per se?
are files primarily intended to be used on windows setup to perform a clean installation rather than upgraded version with all apps pre-installed and needed configurations


# References
- https://www.youtube.com/watch?v=JzZM0h8_8T8&t=933s&ab_channel=Diolinux
- https://schneegans.de/windows/unattend-generator/
- https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/update-windows-settings-and-scripts-create-your-own-answer-file-sxs?view=windows-11