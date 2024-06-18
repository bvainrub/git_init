# How to push to Remote
Quick Manual to pull push

# Step 1: Install GitHub CLI
type -p curl >/dev/null || sudo apt install curl -y
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh -y

# Step 2: Authenticate GitHub CLI
gh auth login

# Step 3: Initialize local Git repository
cd /path/to/your/local/project  # Change to your project directory
git init
git add .
git commit -m "Initial commit"

# Step 4: Create a new GitHub repository and push to remote
gh repo create GoldBusinessSolutionWebUpdate --public --source=. --remote=origin
git push -u origin master





git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bvainrub/rearrange.git
git push -u origin main
