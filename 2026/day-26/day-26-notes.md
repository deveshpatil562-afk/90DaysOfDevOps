# Day 26 – Mastering GitHub CLI (gh)

## 🚀 Overview

Today I explored how to manage GitHub completely from the terminal using the **GitHub CLI (`gh`)**.  

This helped me understand how real DevOps engineers automate repository management, issue tracking, pull requests, and CI/CD workflows directly from the command line.

---

## 🔐 Task 1: Install & Authenticate

- Installed GitHub CLI
- Authenticated using:
  ```
  gh auth login
  ```
- Verified active account:
  ```
  gh auth status
  ```

### 📝 Authentication Methods Supported by `gh`

- Browser-based OAuth login
- Personal Access Token (PAT)
- SSH authentication
- Environment variable (`GH_TOKEN`)
- GitHub Enterprise authentication

---

## 📦 Task 2: Repository Management from Terminal

### Create a Public Repository with README
```
gh repo create test-gh-cli --public --add-readme --clone
```

### Clone a Repository
```
gh repo clone username/repo-name
```

### View Repository Details
```
gh repo view repo-name
```

### List All Repositories
```
gh repo list
```

### Open Repository in Browser
```
gh repo view --web
```

### Delete Repository (Be Careful ⚠️)
```
gh repo delete repo-name
```

---

## 🐞 Task 3: Managing Issues

### Create an Issue
```
gh issue create --title "Fix README" --body "Improve formatting" --label documentation
```

### List Open Issues
```
gh issue list
```

### View Specific Issue
```
gh issue view 1
```

### Close an Issue
```
gh issue close 1
```

### 📝 Automation Use Case

`gh issue` can be used in scripts to automatically create issues when:
- CI/CD pipeline fails
- Deployment errors occur
- Monitoring alerts trigger

---

## 🔁 Task 4: Pull Requests Workflow

### Create Branch
```
git checkout -b feature/update-readme
```

### Push Changes
```
git add .
git commit -m "Update README"
git push origin feature/update-readme
```

### Create Pull Request
```
gh pr create --title "Improve README" --body "Updated structure"
```

### List Open PRs
```
gh pr list
```

### View PR Details
```
gh pr view 1
```

### Merge PR
```
gh pr merge 1 --merge
```

### 📝 Merge Methods Supported

- `--merge` (merge commit)
- `--squash` (squash commits)
- `--rebase` (rebase and merge)
- `--auto` (auto-merge)

### Review Someone Else’s PR
```
gh pr checkout 5
gh pr review 5 --approve
```

---

## ⚙️ Task 5: GitHub Actions (Preview)

### List Workflow Runs
```
gh run list
```

### View Specific Workflow Run
```
gh run view <run-id>
```

### 📝 CI/CD Use Case

`gh run` and `gh workflow` help to:
- Monitor pipeline status
- Re-run failed workflows
- Trigger deployments from terminal
- Automate CI/CD processes

---

## 🛠 Task 6: Useful `gh` Commands

### Make Raw API Calls
```
gh api repos/username/repo
```

### Manage Gists
```
gh gist create file.sh --public
```

### Create Releases
```
gh release create v1.0.0 --notes "Initial release"
```

### Create Command Aliases
```
gh alias set co "pr checkout"
```

### Search GitHub Repositories
```
gh search repos devops
```

---

## 🎯 Key Takeaway

GitHub CLI is not just a tool — it’s a DevOps accelerator.

Managing repositories, issues, pull requests, and workflows from the terminal improves productivity, enables automation, and builds real-world engineering skills.

---

✅ Day 26 Completed  
#DevOps #GitHub #GitHubCLI #90DaysOfDevOps #Automation #LearningInPublic
