# Lab 02 – Git Advanced

## 🎯 Objective:
Learn how to handle common advanced Git tasks including stashing, rebasing, resolving conflicts, reverting commits, and we will introduce automations with GitHub Actions.

---

## 🧭 Exercises

1. **Save your work temporarily using `git stash`**

Modify a file in your repository (e.g., `README.md`) without committing. Then stash the change:

```bash
echo "Work in progress..." >> README.md
git stash
```

> 💬 *Question: What happens to the modified file after stashing? How can you verify the stash is saved?*

Now recover your changes:
```bash
git stash pop
```

> 💬 *Question: What’s the difference between `git stash pop` and `git stash apply`?*

---

2. **Create and resolve a merge conflict (in pairs)**

For this part, work in pairs of two students.

#### 👥 Steps:
- Choose one student to host the GitHub repo and add the other as a **collaborator**.
- Both students **clone** the repository and **create a new branch**:
```bash
git checkout -b student-branch
```
- On their own branch, each student modifies the same line in the `main.py` script.
- Each commits and pushes their changes to their respective branch.

#### 🌀 Merge time:
- The repo owner creates a **Pull Request** and merges their branch into `main`.
- The collaborator then attempts to merge their branch into `main`.

> 💬 *Question: What’s happening? What kind of error appears?*

✅ **Resolve the conflict manually**:
- Git will mark the conflict inside the file using `<<<<<<<`, `=======`, `>>>>>>>`.
- Edit the file to resolve the issue.
- Stage the change and commit the resolution.

> 💬 *Question: Why do these kinds of conflicts occur? How can you reduce their frequency in team projects?*

---

3. **Rebase instead of merge**

Create a new feature branch:
```bash
git checkout -b feature-branch
echo "New Feature" > feature.txt
git add .
git commit -m "Add new feature"
```

Make sure `main` has new commits, then run:
```bash
git checkout feature-branch
git rebase main
```

> 💬 *Question: What does `git rebase` do compared to `merge`? Why might rebase be preferred?*

---

4. 🤖 **GitHub Actions (Bonus)**

Create the file `.github/workflows/hello.yml`:
```yaml
name: Hello Bootcamp

on:
  push:
    branches: [ "main" ]

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - name: Display greeting
        run: echo "👋 Hello from GitHub Actions!"
```

> 💬 *Question: What triggers this action? Where can you see the result?*

---

## 🎯 Bonus Challenge

- Create a branch `feature-hello`
- Add a new script `hello.py` that prints your name
- Rebase it onto `main` instead of merging
- Introduce a bug, commit it, then revert it with `git revert`

---

