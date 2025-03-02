# GitHub Auto Updater

GitHub Auto Updater is a **Python script** that automatically modifies a specified line in a GitHub repository's file at regular intervals. The script fetches phrases from a text file and updates the target file with a new phrase on every iteration.

---

## 🚀 Features

✅ **Automated GitHub file updates** \
✅ **Randomized phrase selection from a text file** \
✅ **Customizable update interval** \
✅ **Automatic commit & push to GitHub** \
✅ **Fallback mechanism for local or remote file retrieval** \
✅ **Prioritize GitHub version if different**

---

## 📥 Installation

### **Prerequisites**
- **Python 3.x**
- **A GitHub personal access token** with `repo` permissions
- **A repository with a file to modify**

### **Clone the Repository**
```bash
git clone https://github.com/Taks-69/GitHub-Auto-Updater.git
cd GitHub-Auto-Updater
```

### **Install Required Libraries**
```bash
pip install requests
```

---

## 🛠 Configuration

Modify the following **configuration variables** in `main.py`:

```python
GITHUB_TOKEN = "your_github_token_here"  # GitHub Personal Access Token
REPO_OWNER = "your_github_username"      # Repository owner
REPO_NAME = "your_repository_name"       # Repository name
FILE_PATH = "README.md"                   # File to modify
BRANCH = "main"                           # Target branch
PHRASES_FILE = "phrases.txt"              # File containing phrases
LINE_TO_MODIFY = 3                         # Line number to modify (1-indexed)
INTERVAL_HOURS = 12                        # Update interval in hours
COMMIT_MESSAGE = "Automated update"       # Commit message
PREFERE_GITHUB = True                      # Prioritize GitHub version if different
```

---

## 🚀 Usage

### **Run the script**
```bash
python script.py
```
The script will automatically fetch a phrase, modify the target file, and commit & push the change to GitHub at the specified interval.

---

## 🔄 Workflow
1. Reads **phrases** from `phrases.txt`
2. Retrieves the current file content from **GitHub**
3. Checks if the local file differs from GitHub version
4. Replaces the specified line with a **random phrase**
5. Commits and pushes the updated file to **GitHub**
6. Waits for the next scheduled update

---

## 📜 Example Phrases
```
"The only limit to our realization of tomorrow is our doubts of today." – Franklin D. Roosevelt
"In the middle of every difficulty lies opportunity." – Albert Einstein
"Don't watch the clock; do what it does. Keep going." – Sam Levenson
"Dream big and dare to fail." – Norman Vaughan
"Success usually comes to those who are too busy to be looking for it." – Henry David Thoreau
```

---

## 🔐 Security Considerations

🔹 **Never share your GitHub token publicly**
🔹 **Ensure your GitHub token has only necessary permissions**

---

## 📚 License

This project is licensed under the **GNU General Public License v3.0**.

---

🔥 **Feel free to star ⭐ the repository if you find this project useful!** 🚀

