# Building the First Python Project: **PyCraft**

We’re going to create a GitHub repo, check it out, open it in PyCharm, add code, and push it back up. Step by step.

---

### Step 1: Create the GitHub Repository

1. Go to [https://github.com](https://github.com) and log in.
2. In the top-right, click the **+** sign → **New repository**.
3. For the repository name, type:

   ```
   pycraft
   ```
4. Leave it **Public**.
5. Do **NOT** add a README, .gitignore, or license — leave it empty.
6. Click **Create repository**.

---

### Step 2: Clone the Repository to Your Computer

1. On the new repo page, click the green **Code** button.
2. Select the **SSH** tab. Copy the SSH link — it looks like:

   ```
   git@github.com:YourUserName/pycraft.git
   ```
3. Open **Windows PowerShell**.
4. Choose a folder to work in (example: Documents). Run:

   ```powershell
   cd $HOME\Documents
   git clone git@github.com:YourUserName/pycraft.git
   ```
5. You now have a folder on your computer:

   ```
   Documents\pycraft
   ```

---

### Step 3: Open the Project in PyCharm

1. Open **PyCharm Community Edition**.
2. On the welcome screen, click **Open**.
3. Browse to:

   ```
   Documents\pycraft
   ```

   and click **OK**.
4. PyCharm will recognize this as a Git project automatically.

---

### Step 4: Add Your First Python File

1. In PyCharm, right-click the **pycraft** folder in the left panel.
2. Select **New → Python File**.
3. Name the file:

   ```
   hello.py
   ```
4. Paste in the following code:

```python
def say_hello():
    print("Hello, World!")

def main():
    say_hello()

if __name__ == "__main__":
    main()
```

5. Right-click inside the code window → choose **Run 'hello'**.
   You should see in the bottom window:

   ```
   Hello, World!
   ```

---

### Step 5: Commit and Push to GitHub

1. In PyCharm, go to the top menu: **Git → Commit…**.
2. Type a message:

   ```
   Add hello world program
   ```
3. Click **Commit and Push**.
4. PyCharm will push the file back to GitHub.

---

### Step 6: Verify on GitHub

1. Go to your GitHub repo page: [https://github.com/YourUserName/pycraft](https://github.com/YourUserName/pycraft).
2. You should now see:

   ```
   hello.py
   ```
3. Click it — you’ll see the code you wrote in PyCharm.

---

🎉 That’s it! You now have:

* A GitHub repo named **pycraft**.
* The repo cloned to her computer.
* A working Python file (`hello.py`).
* Code pushed back to GitHub.

---

