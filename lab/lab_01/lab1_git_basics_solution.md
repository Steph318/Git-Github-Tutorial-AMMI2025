# ✅ Solution – Lab 01 Git Basics

Here are the expected commands and answers to the reflection questions:

---

1. **Open VSCode, create a new folder and rename it**
```bash
mkdir name_of_your_project
```

---

2. **Initialize a local Git repository inside that folder**  
```bash
cd name_of_your_project/
git init
```

> 💬 *What does `git init` actually do under the hood? What changes in your folder structure?*  
✅ `git init` creates a hidden `.git/` directory in your folder. This is where Git stores all version control data (commits, branches, tags, etc.). It turns the folder into a Git repository.

---

3. **Create the first file of your project: a `README.md`**  
```bash
echo "# My first GitHub project" > README.md
```

> 💬 *What are some advantages of having a `README.md` in a project?*  
✅ A `README.md` provides documentation for the project. It often includes a description, installation steps, usage instructions, and contributor guidelines. It helps others (and your future self) understand the purpose of the project.

---

4. **Check the status of the project**
```bash
git status
```

> 💬 *What do you notice? What do the colors mean in VSCode's source control view?*  
✅ Git shows that `README.md` is an untracked file. After adding it, it appears as staged.  
In VSCode:
- Green = staged changes
- Blue = modified but not staged
- Red = deleted

---

5. **Add and commit your file**
```bash
git add README.md
git commit -m "Initial commit"
```

> 💬 *Why is the commit message important? What are some good practices for writing them?*  
✅ Commit messages describe **why** a change was made. They help teammates (and yourself) understand the project history.  
**Best practices**:
- Keep it short and descriptive
- Use the imperative mood (e.g., "Add new feature", not "Added...")
- Avoid vague messages like "update" or "fix"

> 💡 `git commit -am` is a shortcut for staging and committing modified files — but it won’t include newly created files (those still untracked).

---

6. **Explore your Git log history**
```bash
git log
git log --oneline
git log --graph --oneline
```

> 💬 *How could reading the log help during debugging or teamwork?*  
✅ Git logs help track changes and understand what happened when. During debugging, you can find when bugs were introduced. In teams, logs help identify who changed what and why.

---

7. **Create a remote repository on GitHub and connect your local one to it**
```bash
git remote add origin https://github.com/user-name/my-project.git
git push -u origin main
```

> 💬 *What does `-u` mean in the `git push` command?*  
✅ The `-u` (or `--set-upstream`) flag links your local `main` branch to the remote `origin/main`.  
This way, future pushes and pulls can be done with just `git push` or `git pull`, without specifying the branch every time.

---

## 🎯 Bonus
```bash
echo "Python script" > main.py
git add main.py
git commit -m "Push my python script"
git push
```

✅ You can now view `main.py` directly in your GitHub repository online.
