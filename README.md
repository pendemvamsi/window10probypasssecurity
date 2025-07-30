# window10probypasssecurity Auto-Sync Script

## 📄 Description  
This is a one-click Bash script to fully automate pushing a local project directory to GitHub. It will:

1. Install required tooling (`pipx`, `git-filter-repo`) if missing  
2. Initialize a brand-new `git` repository (scrubbing any previous history)  
3. Generate a `.gitignore` and `README.md`  
4. Create the GitHub repository (if it doesn’t already exist) via the GitHub CLI (`gh`)  
5. Add an SSH remote and force-push your local files up to GitHub  

All you have to do is drop this script into your project folder, make it executable, and run it.

---

## ⚙️ Requirements

- **Bash** shell (Linux/macOS)  
- `git`  
- **GitHub CLI** (`gh`) authenticated via `gh auth login`  
- `pipx` (for safely installing Python apps)  

---

## 🛠️ Installation

1. **Install system dependencies** (once):
   ```bash
   sudo apt update
   sudo apt install -y git gh curl python3-pip pipx
   pipx ensurepath
