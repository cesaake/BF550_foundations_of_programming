

### ✅ One-Block `README.md` (fully copyable)

````markdown
# 🐍 Intro to Python Programming: Conda, Git, and Terminal Essentials

Welcome to the foundational Python programming course! This guide walks you through setting up your Python environment with Conda, managing packages with YAML files, interacting with GitHub, and using essential Unix terminal commands. This forms the base for a productive, reproducible, and efficient coding workflow.

---

## 📚 Course Description

This course introduces the fundamentals of Python programming and focuses on:

- Setting up isolated Conda environments for clean development
- Managing and sharing environments using YAML files
- Installing common data science packages
- Navigating your system using the Unix terminal
- Using GitHub for version control and collaboration

No prior programming experience is needed — just follow along!

---

## 🆚 Miniconda vs Anaconda Distribution

| Feature         | Miniconda              | Full Anaconda Distribution     |
|-----------------|------------------------|--------------------------------|
| Size            | ~50 MB                 | ~3–4 GB                        |
| Includes        | Only Conda + Python    | Conda + 250+ preinstalled packages |
| Flexibility     | Highly customizable    | Quick-start for data science  |
| Best for        | Custom lightweight setups | Beginners wanting everything pre-installed |

👉 Use **Miniconda** if you want a lean setup. Use **Anaconda** for plug-and-play data science.

---

## ⚙️ Conda Environment Setup

### ✅ Create an Environment

```bash
conda create -n TEZ python=3.10 numpy pandas matplotlib scikit-learn jupyterlab -y
````

* `TEZ`: Name of your environment
* Includes essential Python libraries for data science

### ✅ Activate / Deactivate

```bash
conda activate TEZ
conda deactivate
```

### ✅ Remove the Environment

```bash
conda env remove -n TEZ
```

---

## 📄 Using YAML Files with Conda

### ✅ Create a `environment.yml` file

```yaml
name: TEZ
channels:
  - conda-forge
  - defaults
dependencies:
  - python=3.10
  - numpy
  - pandas
  - matplotlib
  - scikit-learn
  - jupyterlab
```

### ✅ Create Environment from YAML

```bash
conda env create -f environment.yml
```

### ✅ Update Environment from YAML

```bash
conda env update -f environment.yml --prune
```

### ✅ Export Current Environment

```bash
conda env export --name TEZ > environment.yml
```

---

## 🧰 Basic Conda Commands

```bash
# List environments
conda env list

# List installed packages
conda list

# Export package list (not environment file)
conda list --export > requirements.txt

# Update Conda
conda update conda

# Clean cache
conda clean --all
```

---

## 🌐 Git & GitHub Essentials

### ✅ Full Flow to Push a Project to GitHub

```bash
# Initialize Git
git init

# Add GitHub repo as remote
git remote add origin https://github.com/yourusername/your-repo.git

# Add all files
git add .

# Commit changes
git commit -m "Initial commit"

# Push to main branch
git push -u origin main
```

> ✅ Replace `main` with `master` if your repo uses that.

---

### 🔁 Handle Divergent Branches (Pull Strategy)

Choose how Git pulls from remote:

```bash
# Merge (default, safe)
git config --global pull.rebase false

# Rebase (cleaner history)
git config --global pull.rebase true

# Fast-forward only (strict)
git config --global pull.ff only
```

---

### 🔑 Update GitHub Authentication on macOS

1. Generate a [GitHub Personal Access Token (PAT)](https://github.com/settings/tokens)
2. Remove old token from **Keychain Access**
3. Set credential helper:

```bash
git config --global credential.helper osxkeychain
```

---

## 🖥️ Basic Unix Terminal Commands for Students

### 🔍 Navigation

```bash
pwd           # Print current directory
ls            # List files
cd dir/       # Change directory
cd ..         # Move up
cd ~          # Home directory
```

### 📁 File & Folder Operations

```bash
mkdir name/           # Create directory
touch file.txt        # Create empty file
cp file1 file2        # Copy file
mv file1 newname      # Rename or move
rm file.txt           # Delete file
rm -r dir/            # Delete directory
```

### 📄 Viewing Files

```bash
cat file.txt          # View file contents
less file.txt         # View paged
head file.txt         # First 10 lines
tail file.txt         # Last 10 lines
```

### 🔍 Search & Find

```bash
find . -name "*.py"         # Find files
grep "term" file.txt        # Search inside files
```

### ⚙️ System Info

```bash
whoami         # Show username
uname -a       # System info
date           # Current date/time
```

### ⏱ Shortcuts

| Key Combo  | Action                 |
| ---------- | ---------------------- |
| `Ctrl + C` | Cancel running command |
| `Ctrl + L` | Clear screen           |
| `Tab`      | Autocomplete           |
| `Ctrl + D` | Exit terminal          |

---

## 📂 Suggested Repo Structure

```
your-project/
├── README.md
├── environment.yml
├── index.html               # For GitHub Pages (optional)
└── notebooks/               # Jupyter notebooks go here
```

---

## 🌍 Make HTML Render on GitHub Pages

1. Add an `index.html` file to your repo root
2. Go to **Settings > Pages**
3. Set source to `main` and root or `/docs`
4. GitHub gives you a live link:
   `https://yourusername.github.io/your-repo/`

---

## ✅ Final Tips

* Always run `git status` before commits
* Use `conda activate base` before updating Conda
* Use YAML to share environments with classmates
* Use `man <command>` to learn more about any terminal command

---

Happy coding! 🚀
*This guide is part of the "Intro to Python Programming" course materials.*

```


