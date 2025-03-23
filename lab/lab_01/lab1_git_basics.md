# Lab 01 – Git Basics 

## 🎯 Objective:
Explore fundamental Git and GitHub commands by completing a series of hands-on tasks.

---

## 🧭 Exercise :

1. **Open VSCode, create a new folder, and rename it**  
   You will use this as your working project directory.


2. **Initialize a local Git repository inside that folder**  
   Use the integrated terminal inside VSCode.

   > 💬 *Question: What does `git init` actually do under the hood? What changes in your folder structure?*


3. **Create the first file of your project: a `README.md`**  
   Add a small description of your project.

   > 💬 *Question: What are some advantages of having a `README.md` in a project?*  

4. **Check the status of the project**
   Use `git status` to inspect the state of your working directory.

   > 💬 *Question: What do you notice? What do the colors mean in VSCode's source control view?*

5. **Add and commit your file**

   - Use `git add README.md` and `git commit -m "Add initial README"`
   - You can also try `git commit -am "..."` and observe the difference.

   > 💬 *Question: Why is the commit message important? What are some good practices for writing them?*

6. **Explore your Git log history**

   Try different options:
   ```bash
   git log
   git log --oneline
   git log --graph --oneline
   ```

   > 💬 *Question: How could reading the log help during debugging or team work?*

7. **Create a remote repository on GitHub and connect your local one to it**

   - Use `git remote add origin <URL>` and `git push -u origin main`

   > 💬 *Question: What does `-u` mean in the `git push` command?*

---

## 🎯 Bonus

- Create a new file `main.py` and write a small script (e.g., print your name or a simple calculator).
- Add and commit it.
- Push the changes to GitHub.

---
