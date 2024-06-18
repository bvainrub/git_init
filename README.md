# Git Init

Created Date: June 18, 2024 11:39 AM
Type of Data: Notes
Language (Type): GitHub && Gitlab

# Create remote repo on GitHub from CLI

# Step 1: Install GitHub CLI

```bash
type -p curl >/dev/null || sudo apt install curl -y
curl -fsSL [https://cli.github.com/packages/githubcli-archive-keyring.gpg](https://cli.github.com/packages/githubcli-archive-keyring.gpg) | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] [https://cli.github.com/packages](https://cli.github.com/packages) stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh -y
```

# Step 2: Authenticate GitHub CLI

```bash
gh auth login
```

# Step 3: Initialize local Git repository

```bash
cd /path/to/your/local/project  # Change to your project directory
git init
git add .
git commit -m "Initial commit"
```

# Step 4: Create a new GitHub repository and push to remote

```bash
gh repo create GoldBusinessSolutionWebUpdate --public --source=. --remote=origin
git push -u origin master
git push
```

# Create\ push to EXISTED remote Repo on GitHub

# Follow the steps

Step1 

Create repo  - https://github.com/bvainrub/rearrange.git

Step 2 Copy link [https://github.com/bvainrub/rearrange.git](https://github.com/bvainrub/rearrange.git)

```bash
git init
git add [README.md](http://readme.md/)
git commit -m "first commit"
git branch -M main
git remote add origin [https://github.com/bvainrub/rearrange.git](https://github.com/bvainrub/rearrange.git)
git push -u origin main
```
