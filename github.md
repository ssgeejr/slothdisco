# GitHub Setup on Windows (Step-by-Step)

### 1. Create a GitHub Account

1. Go to [https://github.com](https://github.com).
2. Click **Sign up**.
3. Choose a username, enter your email, and password.
4. Verify your email address when GitHub sends the confirmation.

---

### 2. Install Git for Windows

1. Download Git for Windows: [https://git-scm.com/download/win](https://git-scm.com/download/win).
2. Run the installer:

   * Keep most of the defaults.
   * Make sure **Git Bash** and **Git GUI** are selected (these will be installed).

---

### 3. Create SSH Keys (Windows PowerShell)

1. Open **Windows PowerShell** (Start → search → type `PowerShell`).
2. Run the following command (replace with your GitHub email):

   ```powershell
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```

   * When it asks for a location, press **Enter** to accept the default:

     ```
     C:\Users\<YourName>\.ssh\id_ed25519
     ```
   * When it asks for a passphrase, press **Enter** for none (or set one if you want extra security).

This creates two files in:

```
C:\Users\<YourName>\.ssh\
  ├── id_ed25519      (private key – keep safe, do NOT share)
  └── id_ed25519.pub  (public key – upload this to GitHub)
```

---

### 4. Configure SSH for GitHub

1. In File Explorer, open:

   ```
   C:\Users\<YourName>\.ssh\
   ```
2. Create a new file named `config` (no extension).
3. Edit it with Notepad and add:

   ```
   Host github.com
     HostName github.com
     User git
     IdentityFile C:/Users/<YourName>/.ssh/id_ed25519
   ```

   Save and close.

---

### 5. Add Your SSH Key to GitHub

1. Open PowerShell and type:

   ```powershell
   Get-Content C:\Users\<YourName>\.ssh\id_ed25519.pub
   ```

   Copy the whole line that appears.
2. Go to [GitHub SSH Keys page](https://github.com/settings/keys).
3. Click **New SSH Key**, give it a name (like *My Windows PC*), and paste in the key.
4. Save.

---

### 6. Set Git Identity (Your Name & Email)

In PowerShell, run:

```powershell
git config --global user.name "Your Full Name"
git config --global user.email "your_email@example.com"
```

---

### 7. Test the Connection

Run this in PowerShell:

```powershell
ssh -T git@github.com
```

You should see:

```
Hi <your-username>! You've successfully authenticated, but GitHub does not provide shell access.
```

---

✅ Done — GitHub is ready on Windows.

