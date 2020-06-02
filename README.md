# useful_stuff
Just different useful stuff in order not to forget it

## Git 

### Different account on the same machine (Win)

- Install Windows credential manager [Git Credential Manager for Windows](https://github.com/microsoft/Git-Credential-Manager-for-Windows)
- Run GCM and delete "github.com" entry
- Run `git config --global credential.helper manager`
- Run `git config --global credential.github.com.useHttpPath true` 
  - For all sites do `git config --global credential.useHttpPath true`
- When cloning do `git clone https://CLONINGUSER@github.com/user/repo.git`
