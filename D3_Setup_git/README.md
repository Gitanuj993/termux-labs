# Setup git in Termux

## Process/Architecture/Pipeline
```txt
1. Download git.
2. Add Identity.
3. Connect git to Github or other hosts.
```

### 1. Download ``git``
```bash
pkg update
pkg upgrade
pkg install git
```
### verify
```bash
git --version
```
Expected : 
```txt
git version 2.x.x
```

### 2. Set Git Identity

```bash
git config --global user.name "Anuj Tanwar"
git config --global user.email "YOUR_GITHUB_EMAIL"
```
Verify using : 
```bash
git config --global --list
```

### Make ``main`` default branch : optional

```bash
git config --global init.defaultBranch main
```



### Connect git to Github

Generate your ssh key : Recommended
```bash
ssh-keygen -t ed25519 -C "YOUR_GITHUB_EMAIL"
```

then enter, enter ...

#### want to verify

Go to ``ls -la ~/.ssh``` ans see ``id_ed25519`` or ``id_ed25519.pub``.


### Start your SSH key agent 
```bash
eval "$(ssh-agent -s)"
```

then execute
```bash
ssh-add ~/.ssh/id_ed25519
```

### Copy the Public Key :copy its  output

```bash
cat ~/.ssh/id_ed25519.pub
```
Expected :

```txt
ssh-ed25519 AAAAC3... YOUR_GITHUB_EMAIL
```

### Add the public key to github

```txt
GitHub → Settings → SSH and GPG keys → New SSH key
```
Add title : ``Termux Android``

## Test your connection
```bash
ssh -T git@github.com
```

All Done


## Conclusion

```txt
pkg install git
git config --global user.name "Anuj Tanwar"
git config --global user.email "YOUR_GITHUB_EMAIL"

ssh-keygen -t ed25519 -C "YOUR_GITHUB_EMAIL"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

cat ~/.ssh/id_ed25519.pub
ssh -T git@github.com
```


> Git runs locally in Termux; GitHub is the remote hosting service.

