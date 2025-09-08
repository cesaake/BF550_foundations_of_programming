# BF550_foundations_of_programming: 

##Intro to Python Programming: Environment & Workflow Setup

Welcome to the foundational Python programming course! This repository contains essential instructions and resources for setting up your Python environment using **Conda**, managing packages, and working efficiently with GitHub.

---

## 📚 Course Description

This course introduces you to the fundamentals of Python programming, focusing on building a strong foundation in coding practices, environment management, and reproducible workflows. You'll learn how to:

- Create and manage isolated Conda environments for your projects  
- Install and update essential Python packages used in data science and programming  
- Use YAML files to share and reproduce environments across systems  
- Interact with GitHub for version control, including managing authentication securely  

This setup guide ensures you have a reliable and consistent coding environment to focus on learning Python effectively.

---

## 🐍 Conda Environment Setup

### 1. Create a Conda environment with Python 3.10 and common packages:

```bash
conda create -n TEZ python=3.10 numpy pandas matplotlib scikit-learn jupyterlab -y


## Activate Environment
conda activate TEZ
conda deactivate


## Remove Environmet

conda env remove -n TEZ

## Using environemnt.yml
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

## Crete environment with YAML
conda env create -f environment.yml


## Basic Conda Commands:

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


## Github Essentials
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

