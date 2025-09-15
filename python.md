Perfect — staying **100% Windows-native** here, no Linux-y syntax. Let’s get Python 3.13 installed on Windows with the simplest steps:

---

# Install Python 3.13 on Windows

### 1. Download Python

1. Open your web browser.
2. Go to the official Python site: [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/).
3. Click **Download Python 3.13.x (Windows installer)**.

   * Choose **64-bit installer** unless you’re on an old machine.

---

### 2. Run the Installer

1. Double-click the downloaded file (e.g., `python-3.13.x-amd64.exe`).
2. On the first screen:

   * ✅ Check **Add Python 3.13 to PATH** (important!)
   * Then click **Install Now**.
3. Let it finish and click **Close**.

---

### 3. Verify Installation

Open **Windows PowerShell** and run:

```powershell
python --version
```

You should see:

```
Python 3.13.x
```

---

### 4. Upgrade pip (Optional but recommended)

Still in PowerShell:

```powershell
python -m pip install --upgrade pip
```

---

✅ That’s it. Python 3.13 is now installed and ready to use on Windows.

