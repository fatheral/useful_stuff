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
- Also refer to [link](https://github.com/microsoft/Git-Credential-Manager-for-Windows/issues/749)

### Add existing ssh key (MacOS)

- Run `ssh-add -l`. If don't have it, then
- Run `ssh-add -K ~/.ssh/<id_private_key>`

### Generate new ssh key (MacOS)

- Run `ssh-keygen -t ed25519 -C "your_email@example.com"` and store it to `id_new_key`
- Add to the `~/.ssh/config`:
```
Host *
    AddKeysToAgent yes
    UseKeychain yes
    IdentityFile ~/.ssh/id_ed25519
```
- Add to kechain `ssh-add -K ~/.ssh/<id_private_key>`
