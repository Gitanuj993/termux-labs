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




