2025-04-11 20:45

Status: #adult 

Tags: [[howto]] [[windows]] [[dev]]

# how to submit a new package to winget
## install wingetcreate
```
winget install wingetcreate
```




## install dependencies(if needed)

when I ran the command from the step above I get the following:
```
This package requires the following dependencies:
  - Packages
      Microsoft.VCRedist.2015+.x64
      Microsoft.VCLibs.Desktop.14
```



## setup github token

as an alternative of using passwords for authentication to github you can use personal access token(pat)

follow [this](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic) instructions which is the same as:

1. [Verify your email address](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/verifying-your-email-address), if it hasn't been verified yet.
    
2. In the upper-right corner of any page on GitHub, click your profile photo, then click
    
3. **Settings**.
    
4. In the left sidebar, click
    
5. **Developer settings**.
    
6. In the left sidebar, under
    
7. **Personal access tokens**, click **Tokens (classic)**.
    
8. Select **Generate new token**, then click **Generate new token (classic)**.
    
9. In the "Note" field, give your token a descriptive name.
    
10. To give your token an expiration, select **Expiration**, then choose a default option or click **Custom** to enter a date.
    
11. Select the scopes you'd like to grant this token. To use your token to access repositories from the command line, select **repo**. A token with no assigned scopes can only access public information. For more information, see [Scopes for OAuth apps](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/scopes-for-oauth-apps#available-scopes).
    
12. Click **Generate token**.
    
13. Optionally, to copy the new token to your clipboard
    
14. in the terminal run `wingetcreate.exe token --store --token <YOUR_GITHUB_PAT_TOKEN>` 



## find the proper .exe/.msi link



## wingetcreate new
```
wingetcreate new <THE_URL_TO_THE_EXE>
```
obs: it works with links that ends with ".zip" as well

follow the instructions, but ==not submit the manifest==



## enable local manifest to run
```
winget settings --enable LocalManifestFiles
```



## test the generated manifest

1. go to the manifest location
2. on the powershell terminal run `winget install --manifest <PATH_TO_THE_MANIFEST>`
3. it ==should== install silently ==without any user interaction== besides UAC(popups that usually from windows telling you accept)



## submit the package
```
wingetcreate submit <PATH_TO_THE_MANIFEST>
```
obs: it may need some github authentication



## review and open the PR

just follow the instructions presented on the PR



## toubleshootings
### Installer failed with exit code: 0x80070520 : A specified logon session does not exist. It may already have been terminated.

#### solution 1. reset windows credentials
1. Open **Credential Manager** (`Win + R` → `control /name Microsoft.CredentialManager`)
    
2. Go to **Windows Credentials** → Remove any entries related to **Microsoft Store** or **Windows Package Manager**
    
3. Retry the installation
    
4. Open **Credential Manager** (`Win + R` → `control /name Microsoft.CredentialManager`)
    
5. Go to **Windows Credentials** → Remove any entries related to **Microsoft Store** or **Windows Package Manager**
    
6. Retry the installation.

#### solution 2. repair/reset windows package manager

run as administrator the following using powershell and try the installation:
```
winget uninstall Microsoft.Winget.Source
winget source reset --force
winget install wingetcreate
```

#### solution 3. update winget
```
winget upgrade Microsoft.Winget.Source
```

#### solution 4. restart windows

# References
- [managing github pat(personal access token)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic)
- [thiojoe - how to submit a new package](https://youtu.be/uxr7m8wDeGA?si=IzvcWOA5RsvomEwS&t=579)

