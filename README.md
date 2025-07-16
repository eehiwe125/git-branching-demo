# 🔀 **Mini Project: Git Branching and Merging**

This project simulates a team-based Git workflow using two feature branches (from Tom and Jerry), showcasing how to create branches, edit files, push updates, create pull requests, and merge changes into the main branch.

---

## ✅ **Part 1: Project Initialization**
![alt text](img/01.github-new-repository-created.png)
### 1. **Create a New GitHub Repository**
- Go to [GitHub](https://github.com) and log in.
- Click `+` → **New repository**
- Name it something like: `git-branching-demo`
- Check “Initialize with a README”
- Click **Create repository**
![alt text](img/02.Project_initialisation_with_clone_repository.png)
---

## 💻 **Part 2: Local Setup**

### 2. **Clone the Repository**
```bash
git clone https://github.com/your-username/git-branching-demo.git
cd git-branching-demo
```
![alt text](img/02.Project_initialisation_with_clone_repository.png)
### 3. **Create Base File**
```bash
echo "This is the Admin creating an index.html file for Tom and Jerry." > index.html
git add index.html
git commit -m "Initial commit with index.html"
git push origin main
`img/03.Base_index.html_file_created.png``
![alt text](img/04.Base_file-commited-staged-pushed.png)
---

## 👤 **Part 3: Tom’s Workflow**

### 4. **Create a Feature Branch**
```bash
git checkout -b update-navigation
```

### 5. **Edit the File**
```bash
nano index.html
```
➡ Add this line:
```
This is Tom adding Navigation to the AI-website
```

Save with `Ctrl + O`, `Enter`, and exit with `Ctrl + X`

### 6. **Stage, Commit, and Push**
```bash
git add index.html
git commit -m "Tom added navigation section"
git push origin update-navigation
```

### 7. **Create Tom’s Pull Request**
- On GitHub, go to your repo.
- Switch to the `update-navigation` branch.
- Click **“Compare & pull request”**
- Add a title and description.
- Click **“Create pull request”**

---

## 👤 **Part 4: Merge Tom’s Changes**

### 8. **Review and Merge Pull Request**
- Read the diff in GitHub and verify changes.
- Click **“Merge pull request”**
- Confirm with **“Confirm merge”**

Now Tom's changes are integrated into the `main` branch.
![alt text](img/05.Ton's-workflow-stage-commit-pushed.png)
---

## 👤 **Part 5: Jerry’s Workflow**

### 9. **Create a New Branch for Jerry**
```bash
git checkout -b add-contact-info
```

### 10. **Update Your Branch with Latest Changes**
```bash
git pull origin main
```

This ensures Jerry has Tom’s updates.

### 11. **Edit the File**
```bash
nano index.html
```
➡ Add this line:
```
Jerry’s contact info update
```

Save and exit as before.

### 12. **Stage, Commit, and Push**
```bash
git add index.html
git commit -m "Jerry added contact info"
git push origin add-contact-info
```

---

## 🔁 **Part 6: Jerry’s Pull Request & Merge**

### 13. **Create a Pull Request for Jerry**
- On GitHub, switch to the `add-contact-info` branch.
- Click **“Compare & pull request”**
- Fill out the title/description.
- Click **“Create pull request”**

### 14. **Merge Jerry’s PR**
- Review and **Merge the PR** on GitHub
- Click **“Confirm merge”**
![alt text](img/06.Jerry's-workflow-pull-stage-commit-push.png)
---

## ✅ **Final State**

Your `index.html` file on the `main` branch should now contain:

```
This is the Admin creating an index.html file for Tom and Jerry.
This is Tom adding Navigation to the AI-website
Jerry’s contact info update
```
![alt text](img/07.Final-state-index.html-file-github.png)
---
